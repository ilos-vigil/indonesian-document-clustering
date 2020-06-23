# Indonesian News and Article Clustering with K-Means++

* Stopwords obtained from https://github.com/masdevid/ID-Stopwords
* Dataset comes from private source

## Guide

1. Install necessary library
2. Run `preprocess.ipynb`
3. Run `01.ipynb`, `02.ipynb`, `03.ipynb` & `04.ipynb`

## Word Representation Parameter

| Notebook | Word represenatation | min_df | norm (TF-IDF) | sublinear (TF-IDF) |
| -------- | -------------------- | ------ | ------------- | ------------------ |
| 01.ipynb | Bag Of Words (BOW)   | 100    | -             | -                  |
| 02.ipynb | TF-IDF               | 25     | l1            | False              |
| 03.ipynb | TF-IDF               | 25     | l2            | False              |
| 04.ipynb | TF-IDF               | 5      | l2            | True               |

## Supervised Benchmark Result

| Notebook | Adjusted Rand       | Homogeneity         | Completeness       | V Measure (Beta: 1.0) | Fowlkes-Mallows    |
| -------- | ------------------- | ------------------- | ------------------ | --------------------- | ------------------ |
| 01.ipynb | 0.16832494978963927 | 0.3867110347229015  | 0.5536117350784411 | 0.42753439777044283   | 0.4217245815042002 |
| 02.ipynb | 0.3583653763786496  | 0.48606249528892637 | 0.8130287205170411 | 0.6083988003735386    | 0.6210833495522297 |
| 03.ipynb | 0.6217382880435744  | 0.717235296227637   | 0.7380120740605376 | 0.7274753686083797    | 0.7136882030375186 |
| 04.ipynb | 0.9313637522720699  | 0.9170386227916734  | 0.9167906937890842 | 0.9169146415306973    | 0.9474406310870145 |

## Unsupervised Benchmark Result

| Notebook | Lowest inertia in training | Calinski-Harabasz  | Silhouette (Sample Size 20% doc.) | Davies Bouldin    |
| -------- | -------------------------- | ------------------ | --------------------------------- | ----------------- |
| 01.ipynb | 13412085.957               | 676.2524626345348  | 0.04580253760601429               | 5.378978998734258 |
| 02.ipynb | 957.967                    | 669.9463630311741  | 0.028479348370840964              | 5.508398316924348 |
| 03.ipynb | 39233.847                  | 454.4597438515346  | 0.02209624498094567               | 7.831057435168252 |
| 04.ipynb | 39628.660                  | 349.04195674478404 | 0.01835547854087986               | 8.14052446235942  |
