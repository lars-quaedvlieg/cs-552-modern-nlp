# CS-552: Modern Natural Language Processing

### Course Description
Natural language processing is ubiquitous in modern intelligent technologies, serving as a foundation for language translators, virtual assistants, search engines, and many more. In this course, we cover the foundations of modern methods for natural language processing, such as word embeddings, recurrent neural networks, transformers, and pretraining, and how they can be applied to important tasks in the field, such as machine translation and text classification. We also cover issues with these state-of-the-art approaches (such as robustness, interpretability, sensitivity), identify their failure modes in different NLP applications, and discuss analysis and mitigation techniques for these issues. 

#### Quick access links:
- [Platforms](#class)
- [Lecture Schedule](#lectures)
- [Exercise Schedule](#exercises)
- [Grading](#evaluation)
- [Contact](#contact)


<a name="class"></a>
## Class

| Platform           				| Where & when                                              																								   |
|:------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lectures           						| **Wednesdays: 11:15-13:00** [[STCC - Cloud C](https://plan.epfl.ch/?room=%3DSTCC%20-%20Cloud%20C&dim_floor=0&lang=en&dim_lang=en&tree_groups=centres_nevralgiques%2Cmobilite_acces_grp%2Censeignement%2Ccommerces_et_services&tree_group_layers_centres_nevralgiques=information_epfl%2Cguichet_etudiants&tree_group_layers_mobilite_acces_grp=metro&tree_group_layers_enseignement=&tree_group_layers_commerces_et_services=&baselayer_ref=grp_backgrounds&map_x=2532938&map_y=1152803&map_zoom=11)] & **Thursdays: 13:15-14:00** [[CE16](https://plan.epfl.ch/?room=%3DCE%201%206&dim_floor=1&lang=en&dim_lang=en&tree_groups=centres_nevralgiques%2Cmobilite_acces_grp%2Censeignement%2Ccommerces_et_services&tree_group_layers_centres_nevralgiques=information_epfl%2Cguichet_etudiants&tree_group_layers_mobilite_acces_grp=metro&tree_group_layers_enseignement=&tree_group_layers_commerces_et_services=&baselayer_ref=grp_backgrounds&map_x=2533400&map_y=1152502&map_zoom=13)]  |
| Exercises Session  						| **Thursdays: 14:15-16:00** [[CE11](https://plan.epfl.ch/?room=%3DCE%201%201&dim_floor=1&lang=en&dim_lang=en&tree_groups=centres_nevralgiques%2Cmobilite_acces_grp%2Censeignement%2Ccommerces_et_services&tree_group_layers_centres_nevralgiques=information_epfl%2Cguichet_etudiants&tree_group_layers_mobilite_acces_grp=metro&tree_group_layers_enseignement=&tree_group_layers_commerces_et_services=&baselayer_ref=grp_backgrounds&map_x=2533297&map_y=1152521&map_zoom=13)] 																				   |
| Project Assistance <br />(not every week) | **Wednesdays: 13:15-14:00** [[STCC - Cloud C](https://plan.epfl.ch/?room=%3DSTCC%20-%20Cloud%20C&dim_floor=0&lang=en&dim_lang=en&tree_groups=centres_nevralgiques%2Cmobilite_acces_grp%2Censeignement%2Ccommerces_et_services&tree_group_layers_centres_nevralgiques=information_epfl%2Cguichet_etudiants&tree_group_layers_mobilite_acces_grp=metro&tree_group_layers_enseignement=&tree_group_layers_commerces_et_services=&baselayer_ref=grp_backgrounds&map_x=2532938&map_y=1152803&map_zoom=11)] 													   						   |
| QA Forum & Annoucements       | Ed Forum [[link](https://edstem.org/eu/courses/1159/discussion/)]                                       													   | 
| Grades             						| Moodle [[link](https://moodle.epfl.ch/course/view.php?id=17143)]              																		   |

All lectures will be given in person and live streamed on Zoom. The link to the Zoom is available on the Ed Forum (pinned post). Beware that, in the event of a technical failure during the lecture, continuing to accompany the lecture live via zoom might not be possible.

Recording of the lectures will be made available on SwitchTube. We will reuse some of last year's recordings and we may record a few new lectures in case of different lecture contents.

<a name="lectures"></a>
## Lecture Schedule

<table>
    <tr>
        <td>Week</td>
        <td>Date</td>
        <td>Topic</td>
        <td>Suggested Reading</td>
        <td>Instructor</td>
    </tr>
    <tr>
        <td><strong>Week 1</strong></td>
        <td>21 Feb <br />22 Feb</td>
        <td>Introduction &#124; Building a simple neural classifier <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%201">[slides]</a> <br />Neural LMs: word embeddings <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%201">[slides]</a></td>
        <td>Suggested reading: <ul><li><a href="https://mitpress.mit.edu/9780262042840/introduction-to-natural-language-processing">Introduction to natural language processing, chapter 3.1 - 3.3 & chapter 14.5 - 14.6</a></li><li><a href="https://arxiv.org/abs/1301.3781">Efficient Estimation of Word Representations in Vector Space</a></li><li><a href="https://aclanthology.org/D14-1162">GloVe: Global Vectors for Word Representation</a></li><li><a href="https://aclanthology.org/Q17-1010">Enriching word vectors with subword information</a></li><li><a href="https://aclanthology.org/L18-1008">Advances in pre-training distributed word representations</a></li></ul></td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 2</strong></td>
        <td>Feb <br />29 Feb</td>
        <td>LM basics &#124; Neural LMs: Fixed Context Models <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%202">[slides]</a><br />Neural LMs: RNNs, Backpropagation, Vanishing Gradients; LSTMs <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%202">[slides]</a></td>
        <td>Suggested reading: <ul><li><a href="https://mitpress.mit.edu/9780262042840/introduction-to-natural-language-processing">Introduction to natural language processing, chapter 6.1-6.4</a></li><li><a href="http://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf">A Neural Probabilistic Language Model</a></li><li><a href="https://proceedings.mlr.press/v28/pascanu13.html">On the difficulty of training recurrent neural networks</a></li><li><a href="https://mitpress.mit.edu/9780262042840/introduction-to-natural-language-processing">Introduction to natural language processing, chapter 3.1 - 3.3 & chapter 18.3, 18.4</a></li></ul></td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 3</strong></td>
        <td>6 Mar <br />7 Mar</td>
        <td>Seq2seq + decoding + attention &#124; Transformers <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%203">[slides]</a> <br />Transformers + Greedy Decoding; GPT <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%203">[slides]</a></td>
        <td>Suggested reading: <ul><li><a href="https://arxiv.org/abs/1706.03762">Attention Is All You Need</a></li><li><a href="https://aclanthology.org/W18-2509">The Annotated Transformer</a></li><li><a href="https://jalammar.github.io/illustrated-transformer/">The illustrated transformer</a></li><li>GPT: <a href="https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf">Improving language understanding by generative pre-training</a></li><li>GPT2: <a href="https://d4mucfpksywv.cloudfront.net/better-language-models/language-models.pdf">Language Models are Unsupervised Multitask Learners</a></li></ul></td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 4</strong></td>
        <td>13 Mar <br />14 Mar</td>
        <td><strong>[Online only]</strong>Pretraining: ELMo, BERT, MLM, task generality &#124; Transfer Learning: Introduction <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%204">[slides]</a> <br /> Assignment 1 Q&A</td>
        <td>Suggested reading: <ul><li>Elmo: <a href="https://aclanthology.org/N18-1202">Deep Contextualized Word Representations</a></li><li>BERT: <a href="https://aclanthology.org/N19-1423">BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding</a></li><li>RoBERTa: <a href="https://arxiv.org/abs/1907.11692">RoBERTa: A Robustly Optimized BERT Pretraining Approach</a></li><li>ELECTRA: <a href="https://openreview.net/forum?id=r1xMH1BtvB">ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators</a></li><li><a href="https://www.ruder.io/state-of-transfer-learning-in-nlp/">Transfer Learning in Natural Language Processing</a></li><li>T5: <a href="https://arxiv.org/abs/1910.10683">Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer</a></li><li>BART: <a href="https://arxiv.org/abs/1910.13461">BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension</a></li></ul></td>
        <td>Antoine Bosselut  <br />  Simin Fan</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 5</strong></td>
        <td>20 Mar <br />21 Mar</td>
        <td>Transfer Learning: Dataset Biases <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%205">[slides]</a> <br />Generation: Task  <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%205">[slides]</a></td>
        <td>Suggested reading: -</td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 6</strong></td>
        <td>27 Mar <br />28 Mar</td>
        <td>Generation: Decoding and Training  <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%206">[slides]</a> <br />Generation: Evaluation <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%206">[slides]</a></td>
        <td>Suggested reading: <ul><li>Decoding: <a href="https://arxiv.org/abs/1503.03535">On Using Monolingual Corpora in Neural Machine Translation</a></li><li>Decoding: <a href="https://arxiv.org/abs/1609.08144">Google's Neural Machine Translation System: Bridging the Gap between Human and Machine Translation</a></li><li>Decoding: <a href="https://arxiv.org/abs/1604.01729">Improving LSTM-based Video Description with Linguistic Knowledge Mined from Text</a></li><li>Decoding: <a href="https://arxiv.org/abs/1510.03055">A Diversity-Promoting Objective Function for Neural Conversation Models</a></li><li>Decoding: <a href="https://arxiv.org/abs/1705.04304">A Deep Reinforced Model for Abstractive Summarization</a></li><li>Decoding: <a href="https://arxiv.org/abs/1803.10357">Deep Communicating Agents for Abstractive Summarization</a></li><li>Decoding: <a href="https://arxiv.org/abs/1805.06087">Learning to Write with Cooperative Discriminators</a></li><li>Decoding: <a href="https://arxiv.org/abs/1805.04833">Hierarchical Neural Story Generation</a></li><li>Decoding: <a href="https://arxiv.org/abs/1907.01272">Discourse Understanding and Factual Consistency in Abstractive Summarization</a></li><li>Decoding: <a href="https://arxiv.org/abs/1912.02164">Plug and Play Language Models: A Simple Approach to Controlled Text Generation</a></li><li>Decoding: <a href="https://arxiv.org/abs/1904.09751">The Curious Case of Neural Text Degeneration</a></li><li>Decoding: <a href="https://arxiv.org/abs/1911.00172">Generalization through Memorization: Nearest Neighbor Language Models</a></li><li>Training: <a href="https://arxiv.org/abs/1506.03099">Scheduled Sampling for Sequence Prediction with Recurrent Neural Networks</a></li><li>Training: <a href="https://arxiv.org/abs/1511.06732">Sequence Level Training with Recurrent Neural Networks</a></li><li>Training: <a href="https://arxiv.org/abs/1609.08144"> Google's Neural Machine Translation System: Bridging the Gap between Human and Machine Translation</a></li><li>Training: <a href="https://arxiv.org/abs/1704.03899">Deep Reinforcement Learning-based Image Captioning with Embedding Reward</a></li><li>Training: <a href="https://arxiv.org/abs/1612.00563">Self-critical Sequence Training for Image Captioning</a></li><li>Training: <a href="https://arxiv.org/abs/1612.00370">Improved Image Captioning via Policy Gradient Optimization of SPIDEr</a></li><li>Training: <a href="https://arxiv.org/abs/1703.10931">Sentence Simplification with Deep Reinforcement Learning</a></li><li>Training: <a href="https://arxiv.org/abs/1705.04304">A Deep Reinforced Model for Abstractive Summarization</a></li><li>Training: <a href="https://arxiv.org/abs/1803.10357">Deep Communicating Agents for Abstractive Summarization</a></li><li>Training: <a href="https://arxiv.org/abs/1805.03766">Discourse-Aware Neural Rewards for Coherent Text Generation</a></li><li>Training: <a href="https://arxiv.org/abs/1805.03162">Polite Dialogue Generation Without Parallel Data</a></li><li>Training: <a href="https://arxiv.org/abs/1711.00279">Paraphrase Generation with Deep Reinforcement Learning</a></li><li>Training: <a href="https://arxiv.org/abs/1904.09751">The Curious Case of Neural Text Degeneration</a></li></ul></td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td><strong>*EASTER BREAK*</strong></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 7</strong></td>
        <td>10 Apr <br />11 Apr</td>
        <td>In-context Learning - GPT-3 + Prompts &#124; Instruction Tuning <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%207">[slides]</a><br />Project Description</td>
        <td>Suggested reading: -</td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 8</strong></td>
        <td>17 Apr <br />18 Apr</td>
        <td><strong>[Online only]</strong>Scaling laws &#124; Model Compression <a href="https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Lectures/Week%208">[slides]</a><br /><strong>No class</strong></td>
        <td>Suggested reading: <ul><li><a href="https://arxiv.org/abs/2001.08361">Scaling laws for neural language models</a></li><li><a href="https://arxiv.org/abs/2203.15556">Training compute-optimal large language models</a></li></ul></td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 9</strong></td>
        <td>24 Apr <br />25 Apr</td>
        <td>Ethics in NLP: Bias / Fairness and Toxicity, Privacy, Disinformation <br /><strong>No class</strong> (Project work; A1 Grade Review Session)</td>
        <td>Suggested reading: -</td>
        <td>Anna Sotnikova</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 10</strong></td>
        <td>1 May <br />2 May</td>
        <td>Tokenization: BPE, WP, Char-based &#124; Multilingual LMs <br />Guest Lecture: Kayo Yin</td>
        <td>Suggested reading: <ul><li><a href="https://arxiv.org/abs/2112.10508">Between words and characters: A brief history of open-vocabulary modeling and tokenization in NLP</a></li><li><a href="https://arxiv.org/abs/2105.13626">Byt5: Towards a token-free future with pre-trained byte-to-byte models</a></li><li><a href="https://arxiv.org/abs/1508.07909">Neural machine translation of rare words with subword units</a></li><li><a href="https://arxiv.org/abs/1911.02116">Unsupervised cross-lingual representation learning at scale</a></li><li><a href="https://arxiv.org/abs/1911.01464">Emerging cross-lingual structure in pretrained language models</a></li><li><a href="https://arxiv.org/abs/2005.00052">Mad-x: An adapter-based framework for multi-task cross-lingual transfer</a></li><li><a href="https://arxiv.org/abs/2110.07560">Composable sparse fine-tuning for cross-lingual transfer</a></li><li><a href="https://www.ruder.io/state-of-multilingual-ai/">The State of Multilingual AI</a></li></ul></td>
        <td>Negar Foroutan <br /> Kayo Yin</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 11</strong></td>
        <td>8 May <br />9 May</td>
        <td>Syntactic and Semantic Tasks (NER) &#124; Interpretability: BERTology <br /><strong>No class</strong> (Project work; A2 Grade Review Session)</td>
        <td>Suggested reading: -</td>
        <td>Gail Weiss</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 12</strong></td>
        <td>15 May <br />16 May</td>
        <td>Reading Comprehension &#124; Retrieval-augmented LMs <br /><strong>No class</strong> (Project work; A2 Grade Review Session)</td>
        <td>Suggested reading: <ul><li><a href="https://arxiv.org/abs/1606.05250">Squad: 100,000+ questions for machine comprehension of text</a></li><li><a href="https://aclanthology.org/Q19-1026/">Natural questions: a benchmark for question answering research</a></li><li><a href="https://arxiv.org/abs/2004.04906">Dense passage retrieval for open-domain question answering</a></li><li><a href="https://proceedings.mlr.press/v119/guu20a.html">Retrieval augmented language model pre-training</a></li><li><a href="https://arxiv.org/abs/2005.11401">Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks</a></li><li><a href="https://arxiv.org/abs/2302.04761">Toolformer: Language models can teach themselves to use tools</a></li><li><a href="https://arxiv.org/abs/2210.03629">React: Synergizing reasoning and acting in language models</a></li><li><a href="https://arxiv.org/abs/2112.04426">Improving language models by retrieving from trillions of tokens</a></li><li><a href="https://arxiv.org/abs/2302.07842">Augmented language models: a survey</a></li></ul></td>
        <td>Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 13</strong></td>
        <td>22 May <br />23 May</td>
        <td>Multimodality: L & V <br />Looking forward</td>
        <td>Suggested reading: -</td>
        <td>Syrielle Montariol <br />Antoine Bosselut</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td><strong>Week 14</strong></td>
        <td>29 May <br />30 May</td>
        <td><strong>No class</strong> (Project work; A3 Grade Review Session)</td>
        <td></td>
        <td></td>
    </tr>
</table>


<a name="exercises"></a>
## Exercise Schedule

| Week  | Date   |  Topic                                                                                |  Instructor                                                         |
|:------------|:--------|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------:|
| **Week 1**  | 22 Feb  |  Setup + Word embeddings  [[code][1e]]                                                |  Mete Ismayilzada            |
|             |         |                                                                                       |                                                                     |
| **Week 2**  |  29 Feb  |  Word embeddings review <br /> Language and Sequence-to-sequence models [[code][2e]] |  Mete Ismayilzada <br />Badr AlKhamissi  |
|             |         |                                                                                       |                                                                     |
| **Week 3**  |  6 Mar  | Assignment 1 Q&A    | Mete Ismayilzada         |
| **Week 3**  |  7 Mar  | Language and Sequence-to-sequence models review <br /> Attention + Transformers [[code][3e]]   |  Badr AlKhamissi    |
|             |         |                                                                                       |                                                                     |
| **Week 4**  | 13 Mar  |  **\[Online only\]** Pretraining S2S: BART, T5 [[slides][4s]] | Antoine Bosselut   |
| **Week 4**  | 14 Mar  |  Attention + Transformers review <br />Pretraining and Transfer Learning Pt. 1 [[code][4e]] |  Badr AlKhamissi  <br /> Simin Fan    |
|             |         |                                                                                       |                                                                     |
| **Week 5**  | 20 Mar  |    No lecture     |       -          |
| **Week 5**  | 21 Mar  |  Pretraining and Transfer Learning Pt. 1 review <br />Transfer Learning Pt. 2    [[code][5e]] |  Simin Fan              |
|             |         |                                                                                       |                                                                     |
| **Week 6**  | 27 Mar  |  Assignment 2 Q&A    |  Simin Fan, Silin Gao    |
| **Week 6**  | 28 Mar  |  Transfer Learning Pt. 2 review <br />Text Generation & Assignment 2 Q&A  [[code][6e]]  |  Simin Fan <br />Deniz Bayazit, Silin Gao          |
|             |         |                                                                                       |                                                                     |
|  |   |  ***EASTER BREAK***                                                                   |                                                                     |  
|             |         |                                                                                       |                                                                     |
| **Week 7**  |  10 Apr  |  Assignment 3 Q&A                   |  Badr AlKhamissi <br /> Deniz Bayazit  |
| **Week 7**  |  11 Apr  |  Text Generation review <br />In-context Learning          [[code][7e]]    |  Deniz Bayazit <br /> Mete Ismayilzada  |
|             |         |                                                                                       |                                                                     |
| **Week 8**  | 17 Apr  | No lecture                                                 | - |
| **Week 8**  | 18 Apr  |  Assignment 3 Q&A  <br /> A1 Grade Review Session                |  Badr AlKhamissi <br /> Deniz Bayazit <br /> Mete Ismayilzada |                                                         |

| **Week 9** | 24 & 25 Apr  |  Project                                                               |  TA meetings on-demand                              |
|             |         |                                                                                       |                                                                     |
| **Week 10** |  1 & 2 May  |  Project                                                                             |  TA meetings on-demand                                              |
|             |         |                                                                                       |                                                                     |
| **Week 11** | 8 & 9 May  |  Project  <br /> Milestone 1 Feedback                                                |  TA meetings on-demand                              |
|             |         |                                                                                       |                                                                     |
| **Week 12** | 15 & 16 May  |  Project                                                                              |  TA meetings on-demand                                              |
|             |         |                                                                                       |                                                                     |
| **Week 13** | 22 May  |  A3 Grade Review Session                                                 |  Badr AlKhamissi <br /> Deniz Bayazit                           |
|             |         |                                                                                       |                                                                     |
| **Week 13** | 23 May  |  Project                                                 |  TA meetings on-demand                          |
|             |         |                                                                                       |                                                                     |
| **Week 14** | 30 May   |  Project <br /> Milestone 2 Feedback                                                                             |  TA meetings on-demand                                              |


### Exercises Session format:
- TAs will provide a small discussion over the **last week's exercises**, answering any questions and explaining the solutions. _(10-15mins)_
- TAs will present **this week's exercise**. _(5mins)_ 
- Students will be solving this week's exercises and TAs will provide answers and clarification if needed.

_**Note**: Please make sure you have already done the setup prerequisites to run the coding parts of the exercises. You can find the instructions [here][0e]._

<a name="evaluation"></a>
## Grading:
Your grade in the course will be computed according to the following guidelines.

### Submission Format
Assignment and project release annoucements will be on Ed. Your work will be submitted as a repository created by [GitHub classroom](https://classroom.github.com/). Clicking the assignment link (announced on its release date) will automatically create a repository under your username (ensure it matches the one on the CS-552 GitHub registration form). Your last push to the repository will be considered as your final submission, with its timestamp determining any late days (see below for the policy).

All large files such as model checkpoints need to be pushed to the repository with [Git LFS](https://git-lfs.com/). Large files can take time to upload, therefore please avoid last-minute uploads that can create potential submission delays. We also propose to use [Colab](https://colab.research.google.com/) as a free GPU resource. You can find tutorials on all of these resources [here][0t].

### Late Days Policy
All assignments and milestones are due at 23:59 on their due date. As we understand that circumstances can make it challenging to abide by these due dates, you will receive 7 late days over the course of the semester to be allocated to the assignments and project milestones as you see fit. No further extensions will be granted. The only exception to this rule is for the final report, code, and data. No extensions will be granted beyond June 14th. We will automatically calculate the late days according to your last commit; hence you don’t have to inform us. For group projects, when everyone has some late days, we will deduct individually from everyone. In the scenario where one person has no more late days, that student will lose points for the late submission. The other students in the team will continue to use their late days (i.e. no points will be deducted from them).

### Assignments (40%):
There will be three assignments throughout the course. They will be released and due according to the following schedule:

#### Assignment 1 (10%)
<!-- Link for the assignment [here][1a]. -->
- Released: 28 February 2024
- Due: 17 March 2024
- Grade released: 14 April 2024
- Grade review sessions: 18 and 25 April 2024

#### Assignment 2 (15%)
<!-- Link for the assignment [here][2a]. -->
- Released: 20 March 2024
- Due: 7 April 2024
- Grade released: 5 May 2024
- Grade review sessions: 9 and 16 May 2024

#### Assignment 3 (15%)
<!-- Link for the assignment [here][3a]. -->
- Released: 3 April 2024
- Due: 21 April 2024
- Grade released: 19 May 2024
- Grade review sessions: 29 and 30 May 2024

### Project (60%):
The project will be divided into 2 milestones and a final submission. Each milestone will be worth 15% of the final grade with the remaining 30% being allocated to the final report. Each team will be supervised by one of the course TAs or AEs. 

More details on the content of the project and the deliverables of each milestone will be released at a later date.
<!-- Registration details can be found in the announcement [here][1p]. -->

#### Milestone 1:
<!-- - Milestone 1 parameters can be found in the [project description][2p]. -->
- Due: 5 May 2024

#### Milestone 2:
<!-- - Milestone 2 parameters can be found in the [project description][2p]. -->
- Due: 26 May 2024

#### Final Deliverable:
- The final report, code, and date will be due on June 14th. Students are welcome to turn in their materials ahead of time, as soon as the semester ends.
<!-- - More details can be found in the [project description][2p]. -->
- Due: 14 June 2024


<a name="contact"></a>
## Contacts

Please email us at **nlp-cs552-spring2024-ta-team [at] groupes [dot] epfl [dot] ch** for any administrative questions, rather than emailing TAs individually. All course content questions need to be asked via [Ed](https://edstem.org/eu/courses/1159/discussion/).

**Lecturer**: [Antoine Bosselut](https://people.epfl.ch/antoine.bosselut)

**Teaching assistants**: [Negar Foroutan Eghlidi](https://people.epfl.ch/negar.foroutan), [Badr AlKhamissi](https://people.epfl.ch/badr.alkhamissi), [Deniz Bayazit](https://people.epfl.ch/deniz.bayazit?lang=en), [Beatriz Borges](https://people.epfl.ch/beatriz.borges), [Zeming (Eric) Chen](https://people.epfl.ch/zeming.chen?lang=en), [Simin Fan](https://people.epfl.ch/simin.fan?lang=en), [Silin Gao](https://people.epfl.ch/silin.gao?lang=en), [Mete Ismayilzada](https://people.epfl.ch/mahammad.ismayilzada)


[0t]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/tutorials.md
[0e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Setup
[1e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Week%201%20-%20Word%20Embeddings
[2e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Week%202%20-%20N-gram%20%26%20Neural%20Language%20Models
[3e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Week%203%20-%20RNNs
[4e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Week%204%20-%20Pretraining%20%26%20Finetuning
[5e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Week%205%20-%20Biases%20%26%20Prompting
[6e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Week%206%20-%20Text%20Generation
[7e]:https://github.com/epfl-nlp/cs-552-modern-nlp/tree/main/Exercises/Week%207%20-%20In-context%20Learning
