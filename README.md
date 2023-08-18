# Ru-GoEmotions

## Descriptinon

A translated version of Google [GoEmotions](https://github.com/google-research/google-research/tree/master/goemotions) emotion classification dataset. All features are the same, except new column `ru_text` being added with translated text. I used [deepl translator]() with gogle engine to translate. In this repository I include translation script `ru-go-emotions-creation.ipynb`.

Hugging Face links:

- [Translated](https://huggingface.co/datasets/seara/ru_go_emotions)
- [Original](https://huggingface.co/datasets/go_emotions)

## Downloading

Use Hugging Face [datasets](https://github.com/huggingface/datasets) library or [pandas](https://github.com/pandas-dev/pandas).

### Hugging Face

```python
from datasets import load_dataset

ru_go_emotions_simplified = load_dataset("seara/ru_go_emotions", name="simplified")
ru_go_emotions_raw = load_dataset("seara/ru_go_emotions", name="raw")
```

### Github

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

My models trained on simplified version:

-
-

## Id to Russian label

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
