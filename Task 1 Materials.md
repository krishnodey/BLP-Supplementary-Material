# BLP Task 2: Supplimentary Documents

Provided by the Organizers. Conbination of MUBASE and SentNoB


## [Code](./code)

Code folder includes all the scripts that we used for our experiments. To run the scripts, please follow the bellow commands:


To run BERT-m:

```
!python scripts/run_glue_v1.py \
  --model_name_or_path bert-base-multilingual-cased\
  --train_file ./data/tokenized/blp23_sentiment_train.csv \
  --validation_file ./data/tokenized/blp23_sentiment_dev.csv \
  --test_file ./data/tokenized/blp23_sentiment_test.csv \
  --do_train \
  --do_eval \
  --do_predict \
  --max_seq_length 128 \
  --per_device_train_batch_size 32 \
  --learning_rate 2e-5 \
  --num_train_epochs 5 \
  --output_dir ./output_m-bert/ \
  --overwrite_output_dir
```

To run XLM-RoBERTa base:

```
!python scripts/run_glue_v1.py \
  --model_name_or_path xlm-roberta-base\
  --train_file ./data/tokenized/blp23_sentiment_train.csv \
  --validation_file ./data/tokenized/blp23_sentiment_dev.csv \
  --test_file ./data/tokenized/blp23_sentiment_test.csv \
  --do_train \
  --do_eval \
  --do_predict \
  --max_seq_length 128 \
  --per_device_train_batch_size 32 \
  --learning_rate 2e-5 \
  --num_train_epochs 5 \
  --output_dir ./output_xlm-roberta-base/ \
  --overwrite_output_dir
```
To run XLM-RoBERTa large:

```
!python scripts/run_glue_v1.py \
  --model_name_or_path xlm-roberta-large\
  --train_file ./data/tokenized/blp23_sentiment_train.csv \
  --validation_file ./data/tokenized/blp23_sentiment_dev.csv \
  --test_file ./data/tokenized/blp23_sentiment_test.csv \
  --do_train \
  --do_eval \
  --do_predict \
  --max_seq_length 128 \
  --per_device_train_batch_size 16 \
  --learning_rate 2e-5 \
  --num_train_epochs 5 \
  --output_dir ./output_xlm-roberta-large/ \
  --overwrite_output_dir
```

To run BanglishBERT:

```
python code/run_glue_v1.py \
  --model_name_or_path csebuetnlp/banglishbert \
  --train_file ./Dataset/MUBASE_train.csv \
  --validation_file ./Dataset/MUBASE_dev.csv \
  --test_file ./Dataset/MUBASE_test.csv \
  --do_predict \
  --max_seq_length 256 \
  --per_device_train_batch_size 16 \
  --learning_rate 2e-5 \
  --num_train_epochs 5\
  --output_dir ./output_banglishBert/ \
  --do_eval \
  --do_train \
  --overwrite_output_dir
```

To run BanglaBERT Small:




To run BanglaBERT:

```
!python scripts/run_glue_v1.py \
  --model_name_or_path csebuetnlp/banglabert\
  --train_file ./data/tokenized/blp23_sentiment_train.csv \
  --validation_file ./data/tokenized/blp23_sentiment_dev.csv \
  --test_file ./data/tokenized/blp23_sentiment_test.csv \
  --do_train \
  --do_eval \
  --do_predict \
  --max_seq_length 128 \
  --per_device_train_batch_size 32 \
  --learning_rate 2e-5 \
  --num_train_epochs 3 \
  --output_dir ./output_bangla_bert/ \
  --overwrite_output_dir
```

To run BanglaBERT Large:

```
!python scripts/run_glue_v1.py \
  --model_name_or_path csebuetnlp/banglabert_large\
  --train_file ./data/tokenized/blp23_sentiment_train.csv \
  --validation_file ./data/tokenized/blp23_sentiment_dev.csv \
  --test_file ./data/tokenized/blp23_sentiment_test.csv \
  --do_train \
  --do_eval \
  --do_predict \
  --max_seq_length 128 \
  --per_device_train_batch_size 32 \
  --learning_rate 2e-5 \
  --num_train_epochs 3 \
  --output_dir ./output_bangla_bert_large/ \
  --overwrite_output_dir
```