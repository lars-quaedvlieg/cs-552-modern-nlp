# Tutorials

In this class, we have 3 primary resources (1) GitHub classroom and (2) Git LFS to submit assignments, and (3) Colab to run GPU-requiring assignments. We encourage you to read the following tutorials prior to using these resources.

### Quick access links
1. [GitHub Classroom](#github-classroom)
2. [Colab](#colab)
3. [Git LFS](#git-lfs)


## GitHub Classroom
<a name="github-classroom"></a>

Your work will be submitted as a repository created by [GitHub classroom](https://classroom.github.com/).  Clicking the assignment link (announced on its release date) will automatically create a repository under your username (ensure it matches the one on the CS-552 GitHub registration form). Your last push to the repository will be considered as your final submission, with its timestamp determining any late days (see the Late Days Policy on the website). All large files such as model checkpoints need to be pushed to this repository with [Git LFS](https://git-lfs.com/) (tutorial below). Large files can take time to upload, therefore please avoid last-minute uploads that can create potential submission delays.


## Colab
<a name="colab"></a>

For assignments requiring GPUs, [Colab](https://colab.research.google.com/) is the best free GPU resource available. Colab is not available through EPFL Google accounts, therefore you will need to use or create a personal Google account. You can only use 1 GPU at a time with Colab.

### Suggested Pipeline
Past students have emphasized that implementing the assignments first locally with a CPU and then using Colab to train the final model with a GPU was the best setup. In this setting, they would:

1. First develop their work on a subset of the datasets, with a small batchsize and short epoch, and train the model locally on CPU.
2. Then upload their code to Drive and use Colab to train the model on a complete dataset, higher batchsize, and full epoch.
3. Finally push all the progress back to GitHub.

This can also be helpful as there are daily limits to Colab GPU usage.

### How to upload your repository to Colab

To load a repository to Colab, you can simply upload the repository folder to your Google Drive. Then all you need to do is open your assignment notebook with the Colab interface and specifiy the path where your repository resides in your Drive (the cell to do this action will always be included in your assignment templates).

To use the free GPU, depending on whether you have used Colab before, you may need to click on `Connect` > `Change Runtime Type` > `T4 GPU`. Set this to `CPU` if you want to switch back to CPU.

### How to push Colab progress back to GitHub

There is no way to push the whole repository to GitHub directly from Colab (without creating other problems / privacy concerns). Therefore we suggest simply to:
1. Download your repository folder located in your drive (after saving your files).
2. Copy its contents into your cloned local repository.
3. Commit and push the updates.


## Git LFS
<a name="git-lfs"></a>

You will be using [Git Large File Storage](https://git-lfs.com/) (Git LFS) system to push your models to your submission repository.
Git LFS is an extension for GitHub to version large files.
In practice, large files such as models and datasets cannot be pushed to repositories.
Instead of storing large files directly in your Git repository, Git LFS stores a reference (or pointer) to these files in the repository, while the actual files are stored on a separate server.
This way your repository is easy to clone and pull from without needing to transfer the large files each time.
Moreover, it feels just like using Git, with similar commands.

### 1. Install Git LFS
There are 2 ways you can install Git LFS:

1. Install it using your favorite system package manager. git-lfs packages are available for Homebrew, MacPorts, dnf, and packagecloud
    - **Linux:** Debian and RPM packages are available from packagecloud
    - **Mac OS:** With Homebrew by doing `brew install git-lfs`
    - **Windows:** Git LFS is included in the distribution of Git for Windows. You can also install a recent version of Git LFS from the Chocolatey package manager.

2. Or download the binary and install Git LFS from [the extension's website](https://git-lfs.com/).


### 2. Git LFS Usage
1. Go to your repository's root and link Git LFS:
    ```shell
    cd your-repository-path
    git lfs install
    ```

2. Create a `.gitattributes` file by tracking certain files or folders. Ensure not to track everything but only the necessary checkpoints (e.g., the best-performing ones). Remember that this is a generic tutorial rather than a specific solution for a specific assignment. For example, the following commands will automatically create and append to a `.gitattributes` file:
    ```shell
    # an example to track all large files in the "models" folder, `**` tracks the directory content recursively
    git lfs track "models/**"
    ```

3. Commit the `.gitattributes` file first.
    ```shell
    git add .gitattributes
    git commit -m "Add attributes file"
    git push
    ```

4. Then, commit and push the content of the folders you started tracking with Git LFS, as you would typically do with other small files. For this part after tracking, we suggest pushing each model individually to GitHub to reduce the upload time:
    ```shell
    git add "models/" # or instead add "models/specific_model.pt" or "models/specific_model.safetensors"
    git commit -m "Add large files"
    git push
    ```

You can find more information on [the extension's website](https://git-lfs.com/) and [this Atlassian tutorial](https://www.atlassian.com/git/tutorials/git-lfs#installing-git-lfs).

### 3. Possible Problems

1. To make sure you are committing the files to Git LFS and not to your GitHub repository directly (which will give you an error and stop the process), do either of the following after the last `git commit`:
    - run `git lfs status` and ensure the file(s) in question appear under Git LFS objects to be committed (that they have the LFS value in parenthesis) 
    - run `git lfs ls-files` and ensure the file(s) in question appear in this output.

    More on this in [this stackoverflow post](https://stackoverflow.com/questions/54451856/how-can-i-tell-if-a-file-will-be-uploaded-to-git-lfs-correctly).

2. If you run into a problem where `git lfs status` is not listing the tracked files after the commit and before pushing, we found that depending on the system you are using, you may need to track the *complete relative path from the repo's root to the file* rather than a pattern (*i.e.*, `"models/mymodel.pt"` instead of `"*.pt"`).

3. If you are on Windows, you may need to use forward slashes `\` instead of back `/` when specifying paths.
