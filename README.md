# Complex Vs transformers

## Fb15k
### Complex:
(MRR: 0.2234 , hits@1: 0.1601, hits@10: 0.3503 )\
### Transformers (trainMode: score, ValMaskMode: sr?):  
(MRR: 0.1989 , hits@1: 0.1488, hits@10: 0.3225 )\
### Transformers (trainMode: mlm, ValMaskMode: ?ro):    
(MRR: 0.2352 , hits@1: 0.1456, hits@10: 0.3791 )\

## WN18RR
### Complex:   
(MRR: 0.3822 , hits@1: 0.2161, hits@10: 0.3841 )\
### Transformers (trainMode: score, ValMaskMode: sr?):  
(MRR: 0.3273 , hits@1: 0.2271, hits@10: 0.3767 )\
### Transformers (trainMode: mlm, ValMaskMode: ?ro):    
(MRR: 0.3710 , hits@1: 0.1902, hits@10: 0.3694 )\

## Methodology
Encoder only model inspired from BERT
For every query in dataset, negative samples were introduced by replacing the s/o in the query with random entities from data. If the negatives were also present in test dataset, then they were assigned a gold label of 1.