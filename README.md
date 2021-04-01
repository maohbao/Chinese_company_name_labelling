# PyTorch implementation of sequence labelling for Chinese company name using BERT+CRF
 
Parse Chinese company name to different parts correctly. For example, the name `大连泰和道农业发展有限公司` will be parsed to `大连 / 泰和道 / 农业发展 / 有限公司` with label `LOC / NAME / INDU / ORG`.

The predict result is as follows:

```
[武汉]【翔海】{水处理}<有限公司>
[漯河市]【天利】{白瓜籽加工}<有限责任公司>
[大连]【泰和道】{农业发展}<有限公司>
[天津]【大致】【和堂】{医药}<有限公司>【延年】{中药}<店>
```

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
