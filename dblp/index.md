experiments on the dataset https://blog.dblp.org/2022/03/02/dblp-in-rdf/

# dump from 2024-10-01

| description   | all        | publication | creator   | +% both | +% pub | +% creator |
| ------------- | ---------- | ----------- | --------- | ------- | ------ | ---------- |
| indexing time | 837s       | 462s        | 99s       | 33%     | 44.8%  | 88.2%      |
| strings count | 11,150,828 | 7,516,516   | 3,625,322 | 0.1%    | 32.6%  | 67.5%      |
| index size    | 2.35GB     | 1.39GB      | 0.23GB    | 30.9%   | 40.9%  | 90.1%      |

## Queries

Three common names for French, English and German. For the record, Pierre, Barry and Hans weren't giving enough results

### Michel

| Type        | Nb rows | Single Index | Multi Index | -%    |
| ----------- | ------- | ------------ | ----------- | ----- |
| Publication | 8505    | 4465ms       | **2434ms**  | 45.5% |
| Creator     | 2521    | 2959ms       | **1386ms**  | 53.2% |

### John

| Type        | Nb rows | Single Index | Multi Index | -%    |
| ----------- | ------- | ------------ | ----------- | ----- |
| Publication | 49788   | 5251ms       | **3357ms**  | 36.1% |
| Creator     | 17009   | 5345ms       | **1308ms**  | 75.5% |

### Hans

| Type        | Nb rows | Single Index | Multi Index | -%    |
| ----------- | ------- | ------------ | ----------- | ----- |
| Publication | 11327   | 2507ms       | **1521ms**  | 39.3% |
| Creator     | 3317    | 2352ms       | **866ms**   | 63.2% |
