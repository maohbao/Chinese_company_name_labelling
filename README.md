# PyTorch implementation of sequence labelling for Chinese company name using BERT+CRF

With `bert-base-chinese`, the result is as follows on `test` set:

```
              precision    recall  f1-score   support

        INDU       0.98      0.98      0.98       200
         LOC       1.00      0.99      1.00       199
        NAME       1.00      1.00      1.00       204
         ORG       0.98      0.99      0.98       201

   micro avg       0.99      0.99      0.99       804
   macro avg       0.99      0.99      0.99       804
weighted avg       0.99      0.99      0.99       804
```

To reproduce:
```
 sequence_labeling_company_train.ipynb
```

To predict:
```
 sequence_labeling_company_predict.ipynb
```


Key ideas to get this working are due to [this github](https://github.com/chnsh/BERT-NER-CoNLL).