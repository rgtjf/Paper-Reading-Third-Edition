
# Paper-Reading-Third-Edition

eg: 0-ACL16-Ng-Paper_title.pdf
- Abstract
  - Overview:
  - Advantage:
  - Disadvantage:
  - What can I do? / Can I employ its idea?
- Experiments
  - DataSet:
  - Toolkit:
  - Baseline:
  - Result:


## 1-ICML16-Socher-Ask Me Anything Dynamic Memory Networks for Natural Language Processing
  [PDF](https://arxiv.org/abs/1506.07285),
  [!Bib](http://dblp.uni-trier.de/rec/bibtex/journals/corr/KumarISBEPOGS15)
  [Implement Blog](https://yerevann.github.io/2016/02/05/implementing-dynamic-memory-networks/)
  - [**Experiment Tasks and Datasets**]
    - Reading Comprehension (**bAbI**)
    - Sentiment Classification (**Stanford Sentiment TreeBank**)
    - Sequence Modeling - POS tagging (**WSJ-PTB**)
  - [**Model**]
    - **Input Module**
    - **Question Module**
    - **Episodic Memory Module**
    - **Answer Module**
   <img src="figs/1a.png" title="Dynamic Memory Networks V.S. Memory Networks" width=80%/>
  - [**Dynamic Memory Networks V.S. Memory Networks**]
    1. Sentence Encoding: RNN, Position-Encoding
    2. Dynamic: Episodic Memory Module(When attention probbility is in the <EOS> position), Multi-Hops
  - [**Motivation for Memory Module**]:
    > **Episodic Memory Module**: Given a collection of input representations, the episodic memory module chooses which parts of the inputs to focus on through the attention mechanism. It then produces a ”memory” vector representation taking into account the question as well as the previous memory. Each iteration provides the module with newly relevant information about the input. In other words, the module has the ability to retrieve new information, in the form of input representations, which were thought to be irrelevant in previous iterations. 
  - [**Motivation for Dynamic Part**]:
    >**Need for Multiple Episodes**: The iterative nature of this module allows it to attend to different inputs during each pass. It also allows for a type of transitive inference, since the first pass may uncover the need to retrieve additional facts. For instance, in the example in Fig. 3, we are asked Where is the football? In the first iteration, the model ought attend to sentence 7 (John put down the football.), as the question asks about the football. Only once the model sees that John is relevant can it reason that the second iteration should retrieve where John was. Similarly, a second pass may help for sentiment analysis as we show in the experiments section below.
 
## 2-ICLR15-Facebook-MEMORY NETWORKS
  [PDF](https://arxiv.org/abs/1410.3916),
  [!Bib](http://dblp.uni-trier.de/rec/bibtex/journals/corr/WestonCB14)
  [ppt](/files/2-icml2016-memnn-tutorial.pptx)