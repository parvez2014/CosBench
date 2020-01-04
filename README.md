
Cosbench = Codebase + QAset + Metrics

# Codebase
We provided two versions of our Codebase.

## origin version
The Codebase could be downloaded from [google drive](https://drive.google.com/file/d/1ADAP8-04o_EA-HOvQPwucudtufexLan5/view?usp=sharing).

This .tar.gz package contains 4,199,769 java snippets which are not processed.
It is in TXT format, one code snippet per line.

## processed version
The Codebase could be downloaded from [google drive](https://drive.google.com/file/d/1I5gimDYK7WaiGbSGnBO9jwT3txR1dHlY/view?usp=sharing).

This .tar.gz package contains 4,199,769 java snippets which are processed.
It is in Json format. Each code snippet corresponds to：

```
[   
    {
        "methbody" : "xxx",
        "apiseq"   : "xxx",
        "tokens"   : "xxx",
        "methname" : "xxx",
        "id"       : "xxx"
    },
    ...
]
```

where `methbody` represents the field that stores the body of source code snippet (using 'method' as minimum storage unit), `apiseq` contains the API sequence that appear in the code, `methname` refers to the method name of the source code, `id` indicates the globally unique id(UUID) for each code snippet.

# QAset
The current QAset could be downloaded from [google drive](https://drive.google.com/open?id=15umo6V56Rm-RuxQo1ZDxPtgg9FtSKPbp)

This Json file contains 52 queries and corresponding answers.
Each QA item corresponds to：


```
[ 
    {
        "id"            :"xxx",
        "query"         :"xxx",
        "intention"     :"xxx",
        "representation":"xxx",
        "answerList"    :["xxx","xxx"...]
    },
    ...
]
```

where "id" is the query ID, "query" is the query content, "answerList" is a array which contains the id of snippet answer. 

Since the QAset is incomplete, We will update the QAset when more potential answers found.

# Metrics
CosBench takes four metrics: Precision@k, MAP@k, MRR@k, and Frank.

The evaluation code could be found at this [code link](https://github.com/BASE-LAB-SJTU/CSES_IR/tree/master/src/main/java/CS/evaluation).

# Methods
We reproduced 6 code search methods. They can be classified into two mainstreams: IR (Information Retrieval)-
based methods and DL (Deep Learning)-based ones. The project reproduced IR-based methods could be seen in [there](https://github.com/BASE-LAB-SJTU/CSES_IR),  and the project reproduced DL-based methods could be seen in [there](https://github.com/BASE-LAB-SJTU/CSES_DL).

# Evaluation
Information about the experiment is [here](https://github.com/BASE-LAB-SJTU/CosBench/wiki/Experiments).

# Other Code Search Dataset
Code Search Dataset from FaceBook: H. Li, S. Kim, and S. Chandra, “Neural code search evaluation dataset,” ArXiv, vol. abs/1908.09804, 2019, https://github.com/facebookresearch/Neural-Code-Search-Evaluation-Dataset.

Code Search Dataset from Github & Microsoft: H. Husain, H.-H. Wu, T. Gazit, M. Allamanis, and M. Brockschmidt, “Codesearchnet challenge: Evaluating the state of semantic code search,” ArXiv, vol. abs/1909.09436, 2019, https://github.com/github/codesearchnet.

