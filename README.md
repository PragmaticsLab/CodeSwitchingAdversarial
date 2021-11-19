# Call Larisa Ivanovna: Code-Switching Fools Multilingual NLU Models

[arXiv link](https://arxiv.org/abs/2109.14350)

Practical needs of developing task-oriented dialogue assistants require the ability to understand many languages. Novel benchmarks for multilingual natural language understanding (NLU) include monolingual sentences in several languages, annotated with intents and slots. In such setup models for cross-lingual transfer show remarkable performance in joint intent recognition and slot filling. However, existing benchmarks lack of code-switched utterances, which are difficult to gather and label due to complexity in the grammatical structure. The evaluation of NLU models seems biased and limited, since code-switching is being left out of scope. 

Our work adopts recognized methods to generate plausible and naturally-sounding code-switched utterances and uses them to create a synthetic code-switched test set. Based on experiments, we report that the state-of-the-art NLU models are unable to handle code-switching. At worst, the performance, evaluated by semantic accuracy, drops as low as 15% from 80% across languages. Further we show, that pre-training on synthetic code-mixed data helps to maintain performance on the proposed test set at a comparable level with monolingual data. Finally, we analyze different language pairs and show that the closer the languages are, the better the NLU model handles their alternation. This is in line with the common understanding of how multilingual models conduct transferring  between languages.

Keywords - intent recognition, slot filling, code-mixing, code-switching, multilingual models.

## Usage examples

First you need to get the [dataset](https://catalog.ldc.upenn.edu/LDC2021T04) and put it into the `code/data/atis` folder. Otherwise, you can use cached versions of it prepared by us.

To create translations run `code/make_translations.ipynb`.
To create alignments run `code/make_alignments.ipynb`.
To create adversarial dataset run `code/make_adversarial_dataset.ipynb`.

One can run `code/run_m-bert.ipynb` and `code/run_xlm-r.ipynb` to train and attack different models described in the paper.

To analyze results you can check either `code/results` folder or run `code/analyze_results.ipynb`.
