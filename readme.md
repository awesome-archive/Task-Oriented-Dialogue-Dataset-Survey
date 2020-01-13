<link rel="stylesheet" type="text/css" href="auto-number-title.css" />

# Task-Oriented Dialogue Dataset Survey

### Content
- ##### [Introduction](#intro)
- ##### [Call for Contribution](#call)
- ##### [Leader Boards](#leader)
- ##### [Datasets Introduction](#detail)
- ##### [Acknowledgement](#acknowledgement)



## <a name="intro"></a>Introduction
This repo is a dataset survey for Task-oriented Dialogue.

We investigated most existing dialogue datasets and summarize their basic information, such download link and size.

We also include leader boards of some dataset to present research progress in the task oriented dialogue fields.

A Chinese intro & news for this project is available [here](https://mp.weixin.qq.com/s?__biz=MzIxMjAzNDY5Mg==&mid=2650793618&idx=1&sn=dc5e592c5d8b451531383350af76e254&chksm=8f477379b830fa6fb0b5909f6d6a3f85dae44e8a37aa0ab9763df354cabcc9224c211075f127&mpshare=1&scene=1&srcid=#rd)

## <a name="call"></a> Call for Contributions
Contributions are welcomed, you are encouraged to:
- Directly pull request
- Send me new dataset info
- Send me new experiment results from published paper.

## <a name="leader"></a> Leader Boards

The ranking is depended on published results of related papers. We are trying to keep it up-to-date. The ranking may be unfair because features used and train/dev set splitting in those papers may be different. However it shows a trend of research, and would be helpful for someone to start a project about task-oriented dialogue.

### NLU: Slot Filling
Slot filling task aims to recognize key entity of user utterance, such position and time.

#### ATIS

| Model           | F1  |  Paper / Source |
|:-------------:|:-----:|:-----:|
| Bi-model with a decoder (Wang et al., 2018) | 96.89 | [A Bi-model based RNN Semantic Frame Parsing Model for Intent Detection and Slot Filling](https://aclweb.org/anthology/N18-2050) |
| Intent Gating & self-attention (Li et al., 2018) | 96.52 | [A Self-Attentive Model with Gate Mechanism for Spoken Language Understanding](http://aclweb.org/anthology/D18-1417) |
| Stack-Propagation + BERT (Qin et al., 2019) | 96.10 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| Joint BERT (Chen et al., 2019) | 96.1 | [BERT for Joint Intent Classification and Slot Filling](https://arxiv.org/pdf/1902.10909.pdf) |
| Atomic concept (Su Zhu and Kai Yu, 2018) | 96.08 | [Concept Transfer Learning for Adaptive Language Understanding](http://aclweb.org/anthology/W18-5047) |
| Atten.-Base+Delexicalization (Shin et al., 2018) | 96.08 | [Slot Filling with Delexicalized Sentence Generation](https://www.isca-speech.org/archive/Interspeech_2018/pdfs/1808.pdf) |
| Atten.-Based (Liu and Lane, 2016) | 95.98 |  [Attention-based recurrent neural network models for joint intent detection and slot fillin](https://arxiv.org/pdf/1609.01454.pdf) |
| Stack-Propagation (Qin et al., 2019) | 95.90 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| Encoder-decoder-pointer  (Zhai et al., 2017) | 95.86 |  [Neural Models for Sequence Chunking](https://arxiv.org/pdf/1701.04027.pdf) |
| ELMo + BLSTM-CRF (Siddhant et al., 2018) | 95.62 |  [Unsupervised Transfer Learning for Spoken Language Understanding in Intelligent Agents](https://arxiv.org/pdf/1811.05370.pdf) |
| Capsule Neural Networks (Zhang et al., 2018) | 95.2 | [Joint Slot Filling and Intent Detection via Capsule Neural Networks](https://arxiv.org/pdf/1812.09471.pdf) |
| Slot-Gated (Intent Atten.) (Goo et al., 2018) | 95.2 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |
| Slot-Gated (Full Atten.) (Goo et al., 2018) | 94.8 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |


#### Snips


| Model           | F1  |  Paper / Source |
| ------------- | :-----:| :-----:|
| Enc-dec (focus) + BERT | 97.17 | [Code](https://github.com/sz128/slot_filling_and_intent_detection_of_SLU) |
| Stack-Propagation + BERT (Qin et al., 2019) | 97.0 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| Joint BERT (Chen et al., 2019) | 97.0 | [BERT for Joint Intent Classification and Slot Filling](https://arxiv.org/pdf/1902.10909.pdf) |
| BLSTM-CRF + ELMo word embedding | 96.92 | [Code](https://github.com/sz128/slot_filling_and_intent_detection_of_SLU) |
| Stack-Propagation (Qin et al., 2019) | 94.2 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| ELMo + BLSTM-CRF (Siddhant et al., 2018) | 93.90 |  [Unsupervised Transfer Learning for Spoken Language Understanding in Intelligent Agents](https://arxiv.org/pdf/1811.05370.pdf) |
| Capsule Neural Networks (Zhang et al., 2018) | 91.8 | [Joint Slot Filling and Intent Detection via Capsule Neural Networks](https://arxiv.org/pdf/1812.09471.pdf) |
| Slot-Gated (Full Atten.) (Goo et al., 2018) | 88.8 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |
| BLSTM-CRF (Siddhant et al., 2018) | 88.78 |  [Unsupervised Transfer Learning for Spoken Language Understanding in Intelligent Agents](https://arxiv.org/pdf/1811.05370.pdf) |
| Slot-Gated (Intent Atten.) (Goo et al., 2018) | 88.3 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |

### NLU: Intent Detection
Slot filling task aims to classify user utterance into different domain.

#### ATIS

| Model           | Acc.  |  Paper / Source |
| ------------- | :-----:| :-----:|
| BLSTM + BERT | 99.10 | [Code](https://github.com/sz128/slot_filling_and_intent_detection_of_SLU) |
| Bi-model with a decoder (Wang et al., 2018) | 98.99 | [A Bi-model based RNN Semantic Frame Parsing Model for Intent Detection and Slot Filling](https://aclweb.org/anthology/N18-2050) |
| Intent Gating & self-attention (Li et al., 2018) | 98.77 | [A Self-Attentive Model with Gate Mechanism for Spoken Language Understanding](http://aclweb.org/anthology/D18-1417) |
| Atten.-Based (Liu and Lane, 2016) | 98.43 |  [Attention-based recurrent neural network models for joint intent detection and slot filling](https://arxiv.org/pdf/1609.01454.pdf) |
| BLSTM (Zhang et al., 2016) | 98.10 | [A Joint Model of Intent Determination and Slot Filling for Spoken Language Understanding](https://www.ijcai.org/Proceedings/16/Papers/425.pdf) |
| Joint BERT (Chen et al., 2019) | 97.9 | [BERT for Joint Intent Classification and Slot Filling](https://arxiv.org/pdf/1902.10909.pdf) |
| Stack-Propagation + BERT (Qin et al., 2019) | 97.5 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| Stack-Propagation (Qin et al., 2019) | 96.9 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| Capsule Neural Networks (Zhang et al., 2018) | 95.0 | [Joint Slot Filling and Intent Detection via Capsule Neural Networks](https://arxiv.org/pdf/1812.09471.pdf) |
| Slot-Gated (Intent Atten.) (Goo et al., 2018) | 94.1 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |
| Slot-Gated (Full Atten.) (Goo et al., 2018) | 93.6 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |


#### Snips

| Model           | Acc.  |  Paper / Source |
| ------------- | :-----:| :-----:|
| ELMo + BLSTM-CRF (Siddhant et al., 2018) | 99.29 |  [Unsupervised Transfer Learning for Spoken Language Understanding in Intelligent Agents](https://arxiv.org/pdf/1811.05370.pdf) |
| Enc-dec (focus) + ELMo | 99.14 | [Code](https://github.com/sz128/slot_filling_and_intent_detection_of_SLU) |
| Stack-Propagation + BERT (Qin et al., 2019) | 99.0 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| Joint BERT (Chen et al., 2019) | 98.6 | [BERT for Joint Intent Classification and Slot Filling](https://arxiv.org/pdf/1902.10909.pdf) |
| Stack-Propagation (Qin et al., 2019) | 98.0 | [A Stack-Propagation Framework with Token-level Intent Detection for Spoken Language Understanding](https://www.aclweb.org/anthology/D19-1214/) |
| Capsule Neural Networks (Zhang et al., 2018) | 97.7 | [Joint Slot Filling and Intent Detection via Capsule Neural Networks](https://arxiv.org/pdf/1812.09471.pdf) |
| Slot-Gated (Full Atten.) (Goo et al., 2018) | 97.0 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |
| Slot-Gated (Intent Atten.) (Goo et al., 2018) | 96.8 | [Slot-Gated Modeling for Joint Slot Filling and Intent Prediction](http://www.aclweb.org/anthology/N18-2118) |


### Dialogue State Tracking
Dialogue state tacking task aims to predict or give representation of dialogue state,
which usually contains a goal constraint, a set of requested slots, and the user's dialogue act.

### DSTC2
Clarification of dataset types:

The main results we list here are obtained from pure DSTC2 dataset (ASR n-best).

However, we don't list other kinds of DSTC2 data source results such as **DSTC2-text**
(It formulates the dialog state tracking as a machine reading problem
which read the dialog transcriptions multiple times and answer the questions
about each of the slot,
for more info please refer to [paper](https://aaai.org/ocs/index.php/WS/AAAIW18/paper/view/17447/15652))
and **DSTC-cleaned**
(It is used by the NBT paper and fixes ASR noise and typo during training and include ASR noise during testing,
The cleaned version is available at [here](mi.eng.cam.ac.uk/˜nm480/dstc2-clean)),


| Model           | Area  |  Food  |  Price  |  Joint  |  Paper / Source |
| ------------- | :-----:| :-----:| :-----:| :-----:| --- |
| Liu et al. (2018) | 90 | 84 | 92 | 72 | [Dialogue Learning with Human Teaching and Feedback in End-to-End Trainable Task-Oriented Dialogue Systems](https://arxiv.org/abs/1804.06512) |
| Neural belief tracker (Mrkšić et al., 2017) | 90 | 84 | 94 | 72 | [Neural Belief Tracker: Data-Driven Dialogue State Tracking](https://arxiv.org/abs/1606.03777) |
| RNN (Henderson et al., 2014) |﻿92 | 86 | 86 | 69 | [Robust dialog state tracking using delexicalised recurrent neural networks and unsupervised gate](http://svr-ftp.eng.cam.ac.uk/~sjy/papers/htyo14.pdf) |


## <a name="detail"></a> Dataset Introductions
See the data details Here or in [Excel File](https://github.com/AtmaHou/Task-Oriented-Dialogue-Dataset-Survey/blob/master/Atma'sDatasetSurvey.xlsx?raw=true)

Following information is included for each dataset:
- Name
- Introduction
- Link (Download & Paper)
- Multi or single turn
- Task
- Task detail
- Whether Public Accessible
- Size & Stats
- Included Label
- Missing Label


 | Name                                | Introduction                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Links                                                                                                                                                         | Multi/Single Turn | Task          | Task Detail                                                                     | Public Accessible | Size & Stats                                                                                                                                                                                         | Included Label                                                                                                                                                                            | Missing Label                                                                                                                                                                            |
 |-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|---------------|---------------------------------------------------------------------------------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
 | MultiWOZ   2.0                      | 1. Proposed by EMNLP 2018 best   paper.     2. Largest by now &   contain multi-domains.     3. Human2human     4. goal changes are encouraged                                                                                                                                                                                                                                                                                                                                   | Download:     http://dialogue.mi.eng.cam.ac.uk/index.php/corpus/     Paper:     https://arxiv.org/pdf/1810.00278.pdf                                          | M                 | Task Oriented | 7 domains     Attraction, Hospital,     Police, Hotel, Restaurant, Taxi, Train. | Yes               | Total 10438   dialogues     average number of turns are 8.93 and 15.39 for single and multi-domain   dialogues respectively.     115, 434 turns in total.                                            | Belief state     User Act(inform, request slots)     Agent Act(inform, request slots)                                                                                                     | NLU(Intent, Slots)                                                                                                                                                                       |
 | Medical   DS                        | 1. Our dataset is collected from   the pediatric department in a Chinese online healthcare community     2. Task-oriented Dialogue System for Automatic   Diagnosis                                                                                                                                                                                                                                                                                                              | Download:     http://www.sdspeople.fudan.edu.cn/zywei/data/acl2018-mds.zip     Paper:      http://www.sdspeople.fudan.edu.cn/zywei/paper/liu-acl2018.pdf      | M                 | Task Oriented | Automatic Diagnosis                                                             | Yes               | 4 Disease     67 symptoms                                                                                                                                                                            | Slot     Action                                                                                                                                                                           |                                                                                                                                                                                          |
 | Snips                               | 1. Collected by Snips for model   evaluation.     2. For natural language understanding     3. Homepage:   https://medium.com/snips-ai/benchmarking-natural-language-understanding-systems-google-facebook-microsoft-and-snips-2b8ddcf9fb19                                                                                                                                                                                                                                      | Download:     https://github.com/snipsco/     nlu-benchmark/tree/master/ 2017-06-custom-intent-engines                                                        | S                 | Task Oriented | 7 task:     Weather,play music, search, add to list, book, moive                | Yes               | Train:13,084      Test:700     7 intent 72 slot labels                                                                                                                                               | Intent     Slots                                                                                                                                                                          |                                                                                                                                                                                          |
 | MIT   Restaurant Corpus             | 1. The MIT Restaurant Corpus is   a semantically tagged training and test corpus in BIO format.     2.  For natural   language understanding                                                                                                                                                                                                                                                                                                                                     | Download:     https://groups.csail.mit.edu/sls/downloads/restaurant/                                                                                          | S                 | Task Oriented | Resaurant                                                                       | Yes               | Train, Dev, Test     6,894 766 1,521                                                                                                                                                                 | Slot                                                                                                                                                                                      | Intent                                                                                                                                                                                   |
 | MIT   Movie Corpus                  | 1. The MIT Movie Corpus is a   semantically tagged training and test corpus in BIO format. The eng corpus   are simple queries, and the trivia10k13 corpus are more complex   queries.     2. For natural language understanding                                                                                                                                                                                                                                                 | Download:     https://groups.csail.mit.edu/sls/downloads/movie/                                                                                               | S                 | Task Oriented | Movie                                                                          | Yes               | Train, Dev, Test     MIT Movie Eng 8,798 977 2,443     MIT Movie Trivia 7,035 781 1,953     Refer to: Data Augmentation for Spoken Language Understanding via Joint   Variational Generation         | Slot                                                                                                                                                                                      | Intent                                                                                                                                                                                   |
 | ATIS                                | 1. The ATIS (Airline Travel   Information Systems) dataset (Tur et al., 2010) is widely used in SLU   research     2.  For natural   language understanding                                                                                                                                                                                                                                                                                                                      | Download:     1. https://github.com/AtmaHou/Bi-LSTM_PosTagger/tree/master/data     2.https://github.com/yvchen/JointSLU/tree/master/data                      | S                 | Task Oriented | Airline Travel Information                                                      | Yes               | Train: 4478     Test: 893     120 slot and 21 intent                                                                                                                                                 | Intent     Slots                                                                                                                                                                          |                                                                                                                                                                                          |
 | Microsoft   Dialogue Challenge      | 1. Containing human-annotated   conversational data in three domains    an      2. Experiment platform with built-in simulators in each domain, for training and evaluation purposes.                                                                                                                                                                                                                                                                                            | Download:    https://github.com/xiul-msr/e2e_dialog_challenge/tree/master/data  Paper：     https://arxiv.org/pdf/1807.11125.pdf                                                                                                              | M                 | Task Oriented | Movie-Ticket Booking     Restaurant Reservation     Taxi Ordering               | Yes               | Task Intents Slots   Dialogues     Movie-Ticket Booking 11 29 2890     Restaurant Reservation 11 30 4103     Taxi Ordering 11 29 3094                                                                | Intent     Slots                                                                                                                                                                          | Database     API-call                                                                                                                                                                    |
 | CamRest676                          | CamRest676 Human2Human   dataset contains the following three json   files:     1. CamRest676.json: the woz dialogue dataset, which contains the conversion   from users and wizards, as well as a set of coarse labels for each user   turn.     2. CamRestDB.json: the Cambridge restaurant database file, containing   restaurants in the Cambridge UK area and a set of attributes.     3. The ontology file, specific all the values the three informable slots   can take. | Download:     https://www.repository.cam.ac.uk/handle/1810/260970     Paper:     https://arxiv.org/abs/1604.04562                                             | M                 | Task Oriented | Booking  restaurant                                                             | Yes               | Total 676 Dialogues     Total 1500 Turns     Train:Dev:Test 3:1:1 (Test set not given)                                                                                                               | Slot     User Act(inform, request slots)     Agent Act(inform, request slots)                                                                                                             | Intent     API call     Database                                                                                                                                                         |
 | Frames | 1. Maluuba reased a travel   booking dataset     2. Design for new task: frame tracking (allow comparing between history   entities)     3. Homepage: https://datasets.maluuba.com/Frames     4. Human2Human                                                                                                                                                                                                                                                                     | Download:     https://datasets.maluuba.com/Frames/dl     Paper:     https://arxiv.org/abs/1706.01690     https://1drv.ms/b/s!Aqj1OvgfsHB7dsg42yp2BzDUK6U      | M                 | Task Oriented | Travel Booking                                                                  | Yes               | Dialogues 1369     Turns 19986     Average user satisfaction (from 1-5) 4.58                                                                                                                         | Frame     User agenda     User Act(inform, request slots)     Agent Act(inform, request slots)     API Call     User's satisfaction     Task successful     Database     Entity reference | Intent                                                                                                                                                                                   |
 | Dialog   bAbI tasks data            | 1. Facebook's 6 task-oriented   dialogues data set consist of 6 different tasks.     2. Dataset for task 1-5 is constucted automaticly from bots' chat(Bot2Bot). And dataset for task 6 is   simply reformated dstc2 dataset.     3. A Shared database is included.     4. This is the only task-oriented dataset among bAbI tasks.     5. The goal of it is to evaluate end2end tasks, so there is not intents and   slots.                                                     | Download:     https://research.fb.com/downloads/babi/     Paper:     http://arxiv.org/abs/1605.07683                                                          | M                 | Task Oriented | Book a table at a restaurant                                                    | Yes               | For each task,       training 1000      develop 1000     test 1000           For tasks 1-5,      second test set (with suffix -OOV.txt) that contains dialogs including   entities not present.      | API call     Full Database                                                                                                                                                                | Slot     Intent     User Act     Agent Act                                                                                                                                               |
 | Stanford   Dialog Dataset           | 1. Standford NLP group's data of   car autopilot agent.     2. Human2Human     3. A quick intro http://m.sohu.com/n/499803391/                                                                                                                                                                                                                                                                                                                                                   | Download:     http://nlp.stanford.edu/projects/kvret/kvret_dataset_public.zip     Paper:     https://arxiv.org/abs/1705.05414                                 | M                 | Task Oriented | car autopilot agent: schedule,   weather, navigation                            | Yes               | Training Dialogues 2,425     Validation Dialogues 302     Test Dialogues 304     Avg. # of Utterances Per Dialogue 5.25                                                                              | Dialogue level database     User Act(inform, request slots)     Agent Act(inform, request slots)                                                                                          | API call     Intent     Slot                                                                                                                                                             |
 | Stanford   Dialog Dataset LU        | 1. Stanford data labeled by HIT,   relabel slot & intent     2. Human2Human     3. A quick intro http://m.sohu.com/n/499803391/ to stanford data     4. Annotation handbook:   https://docs.google.com/document/d/1ROARKf8AJNnG2_nPINe1Xm5Rza7V0jPnQV8io09hcFY/edit                                                                                                                                                                                                              | N/A                                                                                                                                                           | M                 | Task Oriented | car autopilot agent: schedule,   weather, navigation                            | No                | Training Dialogues 2,425     Validation Dialogues 302     Test Dialogues 304     Avg. # of Utterances Per Dialogue 5.25                                                                              | Slot     Intent                                                                                                                                                                           | API call          Need to do sample alignment to get the following:     Dialogue level database     User Act(inform, request slots)     Agent Act(inform, request slots)     Agent Reply |
 | DSTC-2                              | 1. Human2Bot restaurant booking dataset     2. For usage refer to:   http://camdial.org/~mh521/dstc/downloads/handbook.pdf     3. Each dialofue is stored in different folder, which contains log and   label.                                                                                                                                                                                                                                                                   | http://camdial.org/~mh521/dstc/                                                                                                                               | M                 | Task Oriented | Booking  restaurant                                                             | Yes               | Train 1612 calls     Dev 506 calls     Test 1117 dialogs                                                                                                                                             | Slot     User Act(inform, request slots)     Agent Act(inform, request slots)                                                                                                             | Intent     API call     Database                                                                                                                                                         |
 | DSTC4                               | 1. Data name as TourSG consists   of 35 dialog sessions on touristic information for Singapore collected from   Skype calls between three tour guides and 35 tourists     2. All the recorded dialogs with the total length of 21 hours have been   manually transcribed and annotated with speech act and semantic labels for   each turn level.     3. Homepage: http://www.colips.org/workshop/dstc4/data.html     4. Human2Human                                             | N/A                                                                                                                                                           | M                 | Task Oriented | Query touristic information                                                    | No                | Train 20 dialogs     Test 15 dialogs                                                                                                                                                                 | speech act (User &   Agent)     semantic labels(Intent? User & Agent)     topic for turn (Intent?)                                                                                        | N/A                                                                                                                                                                                      |
 | Movie   Booking Dataset             | 1. (Microsoft) Raw   conversational data collected via Amazon Mechanical Turk, with annotations   provided by domain experts.     2. Human2Human                                                                                                                                                                                                                                                                                                                                 | Download:     https://github.com/MiuLab/TC-Bot#data     Paper:     TC-bot                                                                                     | M                 | Task Oriented | Booking Movie                                                                   | Yes               | 280 dialogues     turns per dialogue is approximately 11                                                                                                                                             | User Act(inform, request   slots)     Agent Act(inform, request slots)     Intent     Slots                                                                                               | Database     API-call                                                                                                                                                                    |
 | Lingxi                              | 1. The data is all single round   user input divided into good words. There is more noise.     2. Completed part of speech tagging and slot labeling     3. Language: Chinese                                                                                                                                                                                                                                                                                                    | N/A                                                                                                                                                           | S                 | Task Oriented | conversational robot service   user log                                         | No                | Utterance: 5132                                                                                                                                                                                      | Slot     POS                                                                                                                                                                              | Agent reply     Intent     API call     Database                                                                                                                                         |
 | TOP semantic parsing                              | 1. (Facebook) A hierarchical semantic representation for task oriented dialog systems that can model compositional and nested queries. (hierarchical intent and slot) 2. For natural language understanding 3. Human2bot | Download: http://fb.me/semanticparsingdialog ; Paper: https://arxiv.org/pdf/1810.07942.pdf                                                                                                                                                         | S                 | Task Oriented | Navigation and event                                         | Yes                | Train 31279 utterances; Dev 4462 utterances; Test 9042 utterances                                                                                                                                                                                      | Hierarchical intents; Slots                                                                                                                                                                             |                                                                                                                                          |
 | Facebook Multilingual Task Oriented Dataset | 1. (Faceboook)  We release a dataset of around 57k annotated utterances in English (43k), Spanish (8.6k) and Thai (5k) for three task oriented domains … ALARM, REMINDER, and WEATHER. 2. For cross-lingual natural language understanding | Download: https://fb.me/multilingual_task_oriented_data Paper: https://arxiv.org/pdf/1810.13327.pdf | S | Task Oriented | 3 Domains: Alarm, Reminder, Weather and 3 Languages: English, Spanish, Thai | Yes | English Train: 30,521; English Dev: 4,181; English Test: 8,621; Spanish Train: 3,617; Spanish Dev: 1,983; Spanish Test: 3,043; Thai Train: 2,156; Thai Dev: 1,235; Thai Test:  1,692 | Slot    Intent |


## <a name="acknowledgment"></a>Acknowledgment

Thanks for supports from my adviser [Wanxiang Che](http://ir.hit.edu.cn/~car/english.htm).

Thanks for **public contributions** from:

[JiAnge](https://github.com/linjian93),
[Su Zhu](https://github.com/sz128),
[seeledu](https://github.com/seeledu),
[Tony Lin](https://github.com/tnlin),
[Jason Krone](https://github.com/jasonkrone),
[Libo Qin](https://github.com/yizhen20133868)
.
