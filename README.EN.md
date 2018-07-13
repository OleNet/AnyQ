# AnyQ

AnyQ(ANswer Your Questions) is a configurable & plugable FAQ-based Question Answering framework. SimNet, a Semantic Matching Framework developed by Baidu-NLP, is also shipped with AnyQ. 

In our FAQ-based QA framework, which is designed to be configurable and plugable, all the processes or functions are plugins. Developers can easily designed their own processes and add to our framework, so they can quickly build QA system for their own application.  

SimNet, first designed in 2013 by Baidu-NLP, is a flexiable semantic matching framework which is widely used in many applications in Baidu. SimNet consists of the neural network structure BOW、CNN、RNN and MM-DNN. Meanwhile, we have implemented more state-of-the-art structures such as MatchPyramid、MV-LSTM、K-NRM. SimNet has a unified interface, implemented with PaddleFluid and Tensorflow. Models trained using SimNet can be easily added into our AnyQ framework, through which we can improve our semantic matching ability.

## Details

### **FAQ Framework**
AnyQ is constitued of modules including Question Analysis, Retrieval, Matching, Re-Rank. All of those is plugable. AnyQ has 20+ plugins available for now, for instance, chinease wordseg, inverted index, semantic indexing，Jaccard/SimNet feature in matching module.

With the help of plugin design, developers can build and upgrade customized FAQ system quickly.

The achitecture of AnyQ:

<center>
<img src="./docs/images/AnyQ-Framework.png" width="80%" height="80%" />
</center>

AnyQ系统的配置化、插件化设计有助于开发者快速构建、快速定制适用于特定业务场景的FAQ问答系统，加速迭代和升级。

#### Configuration

The plugins can be switched on and off by configurations. To be specific, we list the functions for retrieval and text similarity matching: 

* Retrieval:
    * Inverted index：Based on Solr, shiped with Baidu open source word seg tool；
    * Semantic indexing：Based on SimNet semantic representations，using ANNOY to retrieval；
    * Human intervention：accurate matching；
* Matching:
    *  Literal matching similarity: after word segging, calculating literal matching features
        * Cosine similarity
        * Jaccard similarity
        * BM25
    *  Semantic matching similarity:
        * SimNet matching：Using the model of SimNet, semantic similarity is calculated.


any features you may miss from other text editors are likely to exist in the Sublime plugin repository.

The AutoFileName plugin for example allows you to quickly insert the ‘src’ of an img tag, or insert the file path in a stylesheet link with just a few key strokes.

Furthermore, the vast majority of plugins are open source and can be installed in a matter of seconds through the Sublime Package Manager. Conversely, Dreamweaver plugins are largely paid for and have to be installed via the separate extension manager program.

Checkout my ‘Top Sublime Text plugins‘ article for a better idea of some great plugins available.
