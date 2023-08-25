# ru-goemotions

## Description

This dataset is a translation of the Google [GoEmotions](https://github.com/google-research/google-research/tree/master/goemotions) emotion classification dataset. All features remain unchanged, except for the addition of a new `ru_text` column containing the translated text in Russian. For the translation process, I used the [Deep translator](https://github.com/nidhaloff/deep-translator) with the Google engine. You can find all the details in the `ru-go-emotions-creation.ipynb` script.

Hugging Face links:

- [Translated](https://huggingface.co/datasets/seara/ru_go_emotions)
- [Original](https://huggingface.co/datasets/go_emotions)

## Downloading

Use Hugging Face [datasets](https://github.com/huggingface/datasets) library or [pandas](https://github.com/pandas-dev/pandas).

### From Hugging Face

```python
from datasets import load_dataset

ru_go_emotions_simplified = load_dataset("seara/ru_go_emotions", name="simplified")
ru_go_emotions_raw = load_dataset("seara/ru_go_emotions", name="raw")
```

### From Github

```python
from datasets import load_dataset

ru_go_emotions_simplified = load_dataset(
    "csv",
    data_files={
        "train": "dataset/ru-go-emotions-simplified-train.csv",
        "validation": "dataset/ru-go-emotions-simplified-validation.csv",
        "test": "dataset/ru-go-emotions-simplified-test.csv",
    },
)

ru_go_emotions_raw = load_dataset(
    "csv", data_files={"train": "dataset/ru-go-emotions-raw.csv"}
)
```

## Models

My models trained on the __simplified__ version:

- [rubert-tiny2-ru-go-emotions](https://huggingface.co/seara/rubert-tiny2-ru-go-emotions)
- [rubert-base-cased-ru-go-emotions](https://huggingface.co/seara/rubert-base-cased-ru-go-emotions)

## Id to label

```yaml
0: admiration
1: amusement
2: anger
3: annoyance
4: approval
5: caring
6: confusion
7: curiosity
8: desire
9: disappointment
10: disapproval
11: disgust
12: embarrassment
13: excitement
14: fear
15: gratitude
16: grief
17: joy
18: love
19: nervousness
20: optimism
21: pride
22: realization
23: relief
24: remorse
25: sadness
26: surprise
27: neutral
```

## Label to Russian label

```yaml
admiration: восхищение
amusement: веселье
anger: злость
annoyance: раздражение
approval: одобрение
caring: забота
confusion: непонимание
curiosity: любопытство
desire: желание
disappointment: разочарование
disapproval: неодобрение
disgust: отвращение
embarrassment: смущение
excitement: возбуждение
fear: страх
gratitude: признательность
grief: горе
joy: радость
love: любовь
nervousness: нервозность
optimism: оптимизм
pride: гордость
realization: осознание
relief: облегчение
remorse: раскаяние
sadness: грусть
surprise: удивление
neutral: нейтральность
```
