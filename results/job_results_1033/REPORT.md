---
title: "Risk Factor Analysis"
output: 
  html_document:
    keep_md: TRUE
    self_contained: true
required_packages:  ['github://HBGD-UCB/longbowRiskFactors','github://jeremyrcoyle/skimr@vector_types', 'github://tlverse/delayed']
params:
  roles:
    value:
      - exclude
      - strata
      - id
      - W
      - A
      - Y
  data: 
    value: 
      type: 'web'
      uri: 'https://raw.githubusercontent.com/HBGD-UCB/longbowRiskFactors/master/inst/sample_data/birthwt_data.rdata'
  nodes:
    value:
      strata: ['study_id', 'mrace']
      id: ['subjid']
      W: []
      A: ['parity_cat']
      Y: ['haz01']
  script_params:
    value:
      parallelize:
        input: checkbox
        value: FALSE
      baseline_level:
        input: 'character'
        value: "[1,2)"
  output_directory:
    value: ''

---







## Methods
## Outcome Variable

**Outcome Variable:** stunted

## Predictor Variables

**Intervention Variable:** hdlvry

**Adjustment Set:**

unadjusted

## Stratifying Variables

The analysis was stratified on these variable(s):

* agecat
* studyid
* country

## Data Summary

agecat      studyid                    country                        A        n     nA   nAY0   nAY1
----------  -------------------------  -----------------------------  ---  -----  -----  -----  -----
Birth       ki1000108-CMC-V-BCS-2002   INDIA                          0       90     90     74     16
Birth       ki1000108-CMC-V-BCS-2002   INDIA                          1       90      0      0      0
Birth       ki1000108-IRC              INDIA                          0      388    381    337     44
Birth       ki1000108-IRC              INDIA                          1      388      7      6      1
Birth       ki1000109-EE               PAKISTAN                       0        2      2      1      1
Birth       ki1000109-EE               PAKISTAN                       1        2      0      0      0
Birth       ki1017093c-NIH-Crypto      BANGLADESH                     0       27     22     18      4
Birth       ki1017093c-NIH-Crypto      BANGLADESH                     1       27      5      4      1
Birth       ki1135781-COHORTS          INDIA                          0     4694   2938   2613    325
Birth       ki1135781-COHORTS          INDIA                          1     4694   1756   1534    222
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          0      359    352    263     89
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          1      359      7      7      0
3 months    ki1000108-IRC              INDIA                          0      407    399    310     89
3 months    ki1000108-IRC              INDIA                          1      407      8      6      2
3 months    ki1000109-EE               PAKISTAN                       0      374    252    110    142
3 months    ki1000109-EE               PAKISTAN                       1      374    122     48     74
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          0       97     24     18      6
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          1       97     73     41     32
3 months    ki1017093b-PROVIDE         BANGLADESH                     0      645    482    431     51
3 months    ki1017093b-PROVIDE         BANGLADESH                     1      645    163    136     27
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     0      728    565    448    117
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     1      728    163    124     39
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0     2174   2136   2015    121
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1     2174     38     33      5
3 months    ki1113344-GMS-Nepal        NEPAL                          0      534    132    119     13
3 months    ki1113344-GMS-Nepal        NEPAL                          1      534    402    338     64
3 months    ki1135781-COHORTS          INDIA                          0     4848   2982   2590    392
3 months    ki1135781-COHORTS          INDIA                          1     4848   1866   1508    358
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          0      366    358    249    109
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          1      366      8      7      1
6 months    ki1000108-IRC              INDIA                          0      407    399    303     96
6 months    ki1000108-IRC              INDIA                          1      407      8      4      4
6 months    ki1000109-EE               PAKISTAN                       0      370    248    123    125
6 months    ki1000109-EE               PAKISTAN                       1      370    122     55     67
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          0       96     24     11     13
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          1       96     72     37     35
6 months    ki1017093b-PROVIDE         BANGLADESH                     0      583    433    364     69
6 months    ki1017093b-PROVIDE         BANGLADESH                     1      583    150    125     25
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     0      715    554    449    105
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     1      715    161    116     45
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0     1921   1889   1707    182
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1     1921     32     27      5
6 months    ki1113344-GMS-Nepal        NEPAL                          0      527    129    110     19
6 months    ki1113344-GMS-Nepal        NEPAL                          1      527    398    313     85
6 months    ki1135781-COHORTS          INDIA                          0     4699   2900   2457    443
6 months    ki1135781-COHORTS          INDIA                          1     4699   1799   1323    476
9 months    ki1000108-CMC-V-BCS-2002   INDIA                          0      363    355    223    132
9 months    ki1000108-CMC-V-BCS-2002   INDIA                          1      363      8      7      1
9 months    ki1000108-IRC              INDIA                          0      407    399    292    107
9 months    ki1000108-IRC              INDIA                          1      407      8      4      4
9 months    ki1000109-EE               PAKISTAN                       0      364    246    103    143
9 months    ki1000109-EE               PAKISTAN                       1      364    118     45     73
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          0       85     21      9     12
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          1       85     64     19     45
9 months    ki1017093b-PROVIDE         BANGLADESH                     0      605    450    362     88
9 months    ki1017093b-PROVIDE         BANGLADESH                     1      605    155    114     41
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     0      706    552    437    115
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     1      706    154    105     49
9 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0     1692   1666   1415    251
9 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1     1692     26     22      4
9 months    ki1113344-GMS-Nepal        NEPAL                          0      515    124     93     31
9 months    ki1113344-GMS-Nepal        NEPAL                          1      515    391    278    113
9 months    ki1135781-COHORTS          INDIA                          0     4092   2519   1978    541
9 months    ki1135781-COHORTS          INDIA                          1     4092   1573    986    587
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          0      365    357    179    178
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          1      365      8      6      2
12 months   ki1000108-IRC              INDIA                          0      406    398    284    114
12 months   ki1000108-IRC              INDIA                          1      406      8      3      5
12 months   ki1000109-EE               PAKISTAN                       0      355    242     74    168
12 months   ki1000109-EE               PAKISTAN                       1      355    113     27     86
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          0       92     24      5     19
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          1       92     68     14     54
12 months   ki1017093b-PROVIDE         BANGLADESH                     0      600    448    338    110
12 months   ki1017093b-PROVIDE         BANGLADESH                     1      600    152    105     47
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     0      706    548    428    120
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     1      706    158    107     51
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0     1371   1354   1130    224
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1     1371     17     14      3
12 months   ki1113344-GMS-Nepal        NEPAL                          0      521    126     88     38
12 months   ki1113344-GMS-Nepal        NEPAL                          1      521    395    255    140
12 months   ki1135781-COHORTS          INDIA                          0     3645   2268   1606    662
12 months   ki1135781-COHORTS          INDIA                          1     3645   1377    715    662
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          0      366    358    110    248
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          1      366      8      5      3
18 months   ki1000108-IRC              INDIA                          0      405    397    258    139
18 months   ki1000108-IRC              INDIA                          1      405      8      3      5
18 months   ki1000109-EE               PAKISTAN                       0      348    236     39    197
18 months   ki1000109-EE               PAKISTAN                       1      348    112     13     99
18 months   ki1000304b-SAS-FoodSuppl   INDIA                          0       84     23      4     19
18 months   ki1000304b-SAS-FoodSuppl   INDIA                          1       84     61      6     55
18 months   ki1017093b-PROVIDE         BANGLADESH                     0      552    413    264    149
18 months   ki1017093b-PROVIDE         BANGLADESH                     1      552    139     82     57
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     0      634    487    348    139
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     1      634    147     95     52
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0      927    918    694    224
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1      927      9      6      3
18 months   ki1113344-GMS-Nepal        NEPAL                          0      512    129     60     69
18 months   ki1113344-GMS-Nepal        NEPAL                          1      512    383    178    205
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          0      369    361    102    259
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          1      369      8      3      5
24 months   ki1000108-IRC              INDIA                          0      409    401    236    165
24 months   ki1000108-IRC              INDIA                          1      409      8      3      5
24 months   ki1017093b-PROVIDE         BANGLADESH                     0      577    432    294    138
24 months   ki1017093b-PROVIDE         BANGLADESH                     1      577    145     93     52
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     0      514    391    302     89
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     1      514    123     80     43
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0        6      6      5      1
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1        6      0      0      0
24 months   ki1113344-GMS-Nepal        NEPAL                          0      467    120     73     47
24 months   ki1113344-GMS-Nepal        NEPAL                          1      467    347    185    162
24 months   ki1135781-COHORTS          INDIA                          0     3559   2233   1324    909
24 months   ki1135781-COHORTS          INDIA                          1     3559   1326    468    858


The following strata were considered:

* agecat: 12 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 12 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 12 months, studyid: ki1000109-EE, country: PAKISTAN
* agecat: 12 months, studyid: ki1000304b-SAS-FoodSuppl, country: INDIA
* agecat: 12 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 12 months, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: 12 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 12 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 12 months, studyid: ki1135781-COHORTS, country: INDIA
* agecat: 18 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 18 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 18 months, studyid: ki1000109-EE, country: PAKISTAN
* agecat: 18 months, studyid: ki1000304b-SAS-FoodSuppl, country: INDIA
* agecat: 18 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 18 months, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: 18 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 18 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 24 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 24 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 24 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 24 months, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: 24 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 24 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 24 months, studyid: ki1135781-COHORTS, country: INDIA
* agecat: 3 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 3 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 3 months, studyid: ki1000109-EE, country: PAKISTAN
* agecat: 3 months, studyid: ki1000304b-SAS-FoodSuppl, country: INDIA
* agecat: 3 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 3 months, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: 3 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 3 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 3 months, studyid: ki1135781-COHORTS, country: INDIA
* agecat: 6 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 6 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 6 months, studyid: ki1000109-EE, country: PAKISTAN
* agecat: 6 months, studyid: ki1000304b-SAS-FoodSuppl, country: INDIA
* agecat: 6 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 6 months, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: 6 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 6 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 6 months, studyid: ki1135781-COHORTS, country: INDIA
* agecat: 9 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 9 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 9 months, studyid: ki1000109-EE, country: PAKISTAN
* agecat: 9 months, studyid: ki1000304b-SAS-FoodSuppl, country: INDIA
* agecat: 9 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 9 months, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: 9 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 9 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 9 months, studyid: ki1135781-COHORTS, country: INDIA
* agecat: Birth, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: Birth, studyid: ki1000108-IRC, country: INDIA
* agecat: Birth, studyid: ki1000109-EE, country: PAKISTAN
* agecat: Birth, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: Birth, studyid: ki1135781-COHORTS, country: INDIA

### Dropped Strata

Some strata were dropped due to rare outcomes:

* agecat: Birth, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: Birth, studyid: ki1000108-IRC, country: INDIA
* agecat: Birth, studyid: ki1000109-EE, country: PAKISTAN
* agecat: Birth, studyid: ki1017093c-NIH-Crypto, country: BANGLADESH
* agecat: 3 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 3 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 6 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 6 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 9 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 9 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 9 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 12 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 12 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 12 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 18 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 18 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 18 months, studyid: ki1000304b-SAS-FoodSuppl, country: INDIA
* agecat: 18 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 24 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 24 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 24 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF

## Methods Detail

We're interested in the causal parameters $E[Y_a]$ for all values of $a \in \mathcal{A}$. These parameters represent the mean outcome if, possibly contrary to fact, we intervened to set all units to have $A=a$. Under the randomization and positivity assumptions, these are identified by the statistical parameters $\psi_a=E_W[E_{Y|A,W}(Y|A=a,W)]$.  In addition, we're interested in the mean of $Y$, $E[Y]$ under no intervention (the observed mean). We will estimate these parameters by using SuperLearner to fit the relevant likelihood factors -- $E_{Y|A,W}(Y|A=a,W)$ and $p(A=a|W)$, and then updating our likelihood fit using a joint TMLE.

For unadjusted analyses ($W=\{\}$), initial likelihoods were estimated using Lrnr_glm to estimate the simple $E(Y|A)$ and Lrnr_mean to estimate $p(A)$. For adjusted analyses, a small library containing Lrnr_glmnet, Lrnr_xgboost, and Lrnr_mean was used.

Having estimated these parameters, we will then use the delta method to estimate relative risks and attributable risks relative to a prespecified baseline level of $A$.

todo: add detail about dropping strata with rare outcomes, handling missingness







# Results Detail

## Results Plots
![](/tmp/33b596cf-e5b4-4013-84eb-939078abe445/REPORT_files/figure-html/plot_tsm-1.png)<!-- -->


```
## Warning: Removed 35 rows containing missing values (geom_errorbar).
```

![](/tmp/33b596cf-e5b4-4013-84eb-939078abe445/REPORT_files/figure-html/plot_rr-1.png)<!-- -->

![](/tmp/33b596cf-e5b4-4013-84eb-939078abe445/REPORT_files/figure-html/plot_paf-1.png)<!-- -->

![](/tmp/33b596cf-e5b4-4013-84eb-939078abe445/REPORT_files/figure-html/plot_par-1.png)<!-- -->

## Results Table

### Parameter: TSM


agecat      studyid                    country                        intervention_level   baseline_level     estimate    ci_lower    ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  ----------  ----------  ----------
Birth       ki1135781-COHORTS          INDIA                          0                    NA                0.1106195   0.0992765   0.1219625
Birth       ki1135781-COHORTS          INDIA                          1                    NA                0.1264237   0.1108785   0.1419689
3 months    ki1000109-EE               PAKISTAN                       0                    NA                0.5634921   0.5021767   0.6248074
3 months    ki1000109-EE               PAKISTAN                       1                    NA                0.6065574   0.5197561   0.6933587
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                0.2500000   0.0758621   0.4241379
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          1                    NA                0.4383562   0.3239417   0.5527706
3 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                0.1058091   0.0783278   0.1332905
3 months    ki1017093b-PROVIDE         BANGLADESH                     1                    NA                0.1656442   0.1085285   0.2227598
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                0.2070796   0.1736443   0.2405150
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     1                    NA                0.2392638   0.1737235   0.3048041
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    NA                0.0566479   0.0468423   0.0664536
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1                    NA                0.1315789   0.0240774   0.2390805
3 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                0.0984849   0.0476058   0.1493639
3 months    ki1113344-GMS-Nepal        NEPAL                          1                    NA                0.1592040   0.1234055   0.1950024
3 months    ki1135781-COHORTS          INDIA                          0                    NA                0.1314554   0.1193264   0.1435844
3 months    ki1135781-COHORTS          INDIA                          1                    NA                0.1918542   0.1739866   0.2097219
6 months    ki1000109-EE               PAKISTAN                       0                    NA                0.5040323   0.4417211   0.5663434
6 months    ki1000109-EE               PAKISTAN                       1                    NA                0.5491803   0.4607676   0.6375931
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                0.5416667   0.3412780   0.7420553
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          1                    NA                0.4861111   0.3700577   0.6021646
6 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                0.1593533   0.1248498   0.1938569
6 months    ki1017093b-PROVIDE         BANGLADESH                     1                    NA                0.1666667   0.1069756   0.2263577
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                0.1895307   0.1568715   0.2221899
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     1                    NA                0.2795031   0.2101368   0.3488694
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    NA                0.0963473   0.0830377   0.1096569
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1                    NA                0.1562500   0.0304145   0.2820855
6 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                0.1472868   0.0860731   0.2085006
6 months    ki1113344-GMS-Nepal        NEPAL                          1                    NA                0.2135678   0.1732667   0.2538690
6 months    ki1135781-COHORTS          INDIA                          0                    NA                0.1527586   0.1396637   0.1658535
6 months    ki1135781-COHORTS          INDIA                          1                    NA                0.2645914   0.2442055   0.2849774
9 months    ki1000109-EE               PAKISTAN                       0                    NA                0.5813008   0.5195661   0.6430355
9 months    ki1000109-EE               PAKISTAN                       1                    NA                0.6186441   0.5308854   0.7064028
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                0.5714286   0.3585162   0.7843409
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          1                    NA                0.7031250   0.5905269   0.8157231
9 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                0.1955556   0.1588794   0.2322317
9 months    ki1017093b-PROVIDE         BANGLADESH                     1                    NA                0.2645161   0.1950210   0.3340112
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                0.2083333   0.1744304   0.2422362
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     1                    NA                0.3181818   0.2445666   0.3917970
9 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                0.2500000   0.1737113   0.3262887
9 months    ki1113344-GMS-Nepal        NEPAL                          1                    NA                0.2890026   0.2440280   0.3339771
9 months    ki1135781-COHORTS          INDIA                          0                    NA                0.2147678   0.1987290   0.2308065
9 months    ki1135781-COHORTS          INDIA                          1                    NA                0.3731723   0.3492686   0.3970760
12 months   ki1000109-EE               PAKISTAN                       0                    NA                0.6942149   0.6360838   0.7523459
12 months   ki1000109-EE               PAKISTAN                       1                    NA                0.7610619   0.6823258   0.8397981
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                0.7916667   0.6282989   0.9550344
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          1                    NA                0.7941176   0.6974861   0.8907492
12 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                0.2455357   0.2056472   0.2854242
12 months   ki1017093b-PROVIDE         BANGLADESH                     1                    NA                0.3092105   0.2356765   0.3827446
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                0.2189781   0.1843286   0.2536276
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     1                    NA                0.3227848   0.2498311   0.3957385
12 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                0.3015873   0.2213747   0.3817999
12 months   ki1113344-GMS-Nepal        NEPAL                          1                    NA                0.3544304   0.3072128   0.4016480
12 months   ki1135781-COHORTS          INDIA                          0                    NA                0.2918871   0.2731741   0.3106002
12 months   ki1135781-COHORTS          INDIA                          1                    NA                0.4807553   0.4543623   0.5071483
18 months   ki1000109-EE               PAKISTAN                       0                    NA                0.8347458   0.7872920   0.8821995
18 months   ki1000109-EE               PAKISTAN                       1                    NA                0.8839286   0.8245219   0.9433352
18 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                0.3607748   0.3144182   0.4071314
18 months   ki1017093b-PROVIDE         BANGLADESH                     1                    NA                0.4100719   0.3282323   0.4919116
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                0.2854209   0.2452794   0.3255625
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     1                    NA                0.3537415   0.2763883   0.4310947
18 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                0.5348837   0.4487272   0.6210403
18 months   ki1113344-GMS-Nepal        NEPAL                          1                    NA                0.5352480   0.4852490   0.5852471
24 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                0.3194444   0.2754384   0.3634505
24 months   ki1017093b-PROVIDE         BANGLADESH                     1                    NA                0.3586207   0.2804910   0.4367503
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                0.2276215   0.1860204   0.2692225
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     1                    NA                0.3495935   0.2652421   0.4339449
24 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                0.3916667   0.3042384   0.4790950
24 months   ki1113344-GMS-Nepal        NEPAL                          1                    NA                0.4668588   0.4143100   0.5194076
24 months   ki1135781-COHORTS          INDIA                          0                    NA                0.4070757   0.3866958   0.4274556
24 months   ki1135781-COHORTS          INDIA                          1                    NA                0.6470588   0.6213335   0.6727841


### Parameter: E(Y)


agecat      studyid                    country                        intervention_level   baseline_level     estimate    ci_lower    ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  ----------  ----------  ----------
Birth       ki1135781-COHORTS          INDIA                          NA                   NA                0.1165317   0.1163129   0.1167505
3 months    ki1000109-EE               PAKISTAN                       NA                   NA                0.5775401   0.5754912   0.5795890
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          NA                   NA                0.3917526   0.3754938   0.4080113
3 months    ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.1209302   0.1189220   0.1229385
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     NA                   NA                0.2142857   0.2133105   0.2152610
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   NA                   NA                0.0579577   0.0575448   0.0583706
3 months    ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.1441948   0.1419711   0.1464184
3 months    ki1135781-COHORTS          INDIA                          NA                   NA                0.1547030   0.1538756   0.1555303
6 months    ki1000109-EE               PAKISTAN                       NA                   NA                0.5189189   0.5167533   0.5210845
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          NA                   NA                0.5000000   0.4951626   0.5048374
6 months    ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.1612350   0.1609753   0.1614947
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     NA                   NA                0.2097902   0.2070336   0.2125468
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   NA                   NA                0.0973451   0.0970022   0.0976881
6 months    ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.1973435   0.1949081   0.1997789
6 months    ki1135781-COHORTS          INDIA                          NA                   NA                0.1955735   0.1940191   0.1971280
9 months    ki1000109-EE               PAKISTAN                       NA                   NA                0.5934066   0.5916085   0.5952047
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          NA                   NA                0.6705882   0.6584414   0.6827351
9 months    ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.2132231   0.2108224   0.2156239
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     NA                   NA                0.2322946   0.2289459   0.2356433
9 months    ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.2796117   0.2781700   0.2810533
9 months    ki1135781-COHORTS          INDIA                          NA                   NA                0.2756598   0.2732986   0.2780211
12 months   ki1000109-EE               PAKISTAN                       NA                   NA                0.7154930   0.7122492   0.7187367
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          NA                   NA                0.7934783   0.7932571   0.7936994
12 months   ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.2616667   0.2594489   0.2638844
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     NA                   NA                0.2422096   0.2390159   0.2454033
12 months   ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.3416507   0.3397058   0.3435955
12 months   ki1135781-COHORTS          INDIA                          NA                   NA                0.3632373   0.3602642   0.3662104
18 months   ki1000109-EE               PAKISTAN                       NA                   NA                0.8505747   0.8481571   0.8529923
18 months   ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.3731884   0.3714018   0.3749750
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     NA                   NA                0.3012618   0.2990157   0.3035079
18 months   ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.5351562   0.5351425   0.5351700
24 months   ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.3292894   0.3279017   0.3306772
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     NA                   NA                0.2568093   0.2523061   0.2613126
24 months   ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.4475375   0.4445544   0.4505206
24 months   ki1135781-COHORTS          INDIA                          NA                   NA                0.4964878   0.4926752   0.5003003


### Parameter: RR


agecat      studyid                    country                        intervention_level   baseline_level     estimate    ci_lower   ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  ----------  ----------  ---------
Birth       ki1135781-COHORTS          INDIA                          0                    0                 1.0000000   1.0000000   1.000000
Birth       ki1135781-COHORTS          INDIA                          1                    0                 1.1428702   0.9737860   1.341313
3 months    ki1000109-EE               PAKISTAN                       0                    0                 1.0000000   1.0000000   1.000000
3 months    ki1000109-EE               PAKISTAN                       1                    0                 1.0764258   0.8993081   1.288427
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    0                 1.0000000   1.0000000   1.000000
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          1                    0                 1.7534247   0.8333705   3.689233
3 months    ki1017093b-PROVIDE         BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
3 months    ki1017093b-PROVIDE         BANGLADESH                     1                    0                 1.5654998   1.0166587   2.410632
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     1                    0                 1.1554192   0.8407120   1.587932
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    0                 1.0000000   1.0000000   1.000000
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1                    0                 2.3227490   1.0076333   5.354292
3 months    ki1113344-GMS-Nepal        NEPAL                          0                    0                 1.0000000   1.0000000   1.000000
3 months    ki1113344-GMS-Nepal        NEPAL                          1                    0                 1.6165327   0.9202140   2.839750
3 months    ki1135781-COHORTS          INDIA                          0                    0                 1.0000000   1.0000000   1.000000
3 months    ki1135781-COHORTS          INDIA                          1                    0                 1.4594626   1.2801413   1.663903
6 months    ki1000109-EE               PAKISTAN                       0                    0                 1.0000000   1.0000000   1.000000
6 months    ki1000109-EE               PAKISTAN                       1                    0                 1.0895738   0.8894126   1.334781
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    0                 1.0000000   1.0000000   1.000000
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          1                    0                 0.8974359   0.5778122   1.393863
6 months    ki1017093b-PROVIDE         BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
6 months    ki1017093b-PROVIDE         BANGLADESH                     1                    0                 1.0458937   0.6882258   1.589440
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     1                    0                 1.4747116   1.0901648   1.994904
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    0                 1.0000000   1.0000000   1.000000
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   1                    0                 1.6217376   0.7163325   3.671525
6 months    ki1113344-GMS-Nepal        NEPAL                          0                    0                 1.0000000   1.0000000   1.000000
6 months    ki1113344-GMS-Nepal        NEPAL                          1                    0                 1.4500132   0.9186313   2.288773
6 months    ki1135781-COHORTS          INDIA                          0                    0                 1.0000000   1.0000000   1.000000
6 months    ki1135781-COHORTS          INDIA                          1                    0                 1.7320884   1.5435253   1.943687
9 months    ki1000109-EE               PAKISTAN                       0                    0                 1.0000000   1.0000000   1.000000
9 months    ki1000109-EE               PAKISTAN                       1                    0                 1.0642408   0.8914159   1.270573
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    0                 1.0000000   1.0000000   1.000000
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          1                    0                 1.2304687   0.8202408   1.845865
9 months    ki1017093b-PROVIDE         BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
9 months    ki1017093b-PROVIDE         BANGLADESH                     1                    0                 1.3526393   0.9794725   1.867978
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     1                    0                 1.5272727   1.1509894   2.026571
9 months    ki1113344-GMS-Nepal        NEPAL                          0                    0                 1.0000000   1.0000000   1.000000
9 months    ki1113344-GMS-Nepal        NEPAL                          1                    0                 1.1560102   0.8207226   1.628272
9 months    ki1135781-COHORTS          INDIA                          0                    0                 1.0000000   1.0000000   1.000000
9 months    ki1135781-COHORTS          INDIA                          1                    0                 1.7375619   1.5747480   1.917209
12 months   ki1000109-EE               PAKISTAN                       0                    0                 1.0000000   1.0000000   1.000000
12 months   ki1000109-EE               PAKISTAN                       1                    0                 1.0962916   0.9596718   1.252361
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          0                    0                 1.0000000   1.0000000   1.000000
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          1                    0                 1.0030960   0.7894069   1.274630
12 months   ki1017093b-PROVIDE         BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
12 months   ki1017093b-PROVIDE         BANGLADESH                     1                    0                 1.2593301   0.9441936   1.679648
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     1                    0                 1.4740506   1.1186428   1.942376
12 months   ki1113344-GMS-Nepal        NEPAL                          0                    0                 1.0000000   1.0000000   1.000000
12 months   ki1113344-GMS-Nepal        NEPAL                          1                    0                 1.1752165   0.8728295   1.582364
12 months   ki1135781-COHORTS          INDIA                          0                    0                 1.0000000   1.0000000   1.000000
12 months   ki1135781-COHORTS          INDIA                          1                    0                 1.6470588   1.5137453   1.792113
18 months   ki1000109-EE               PAKISTAN                       0                    0                 1.0000000   1.0000000   1.000000
18 months   ki1000109-EE               PAKISTAN                       1                    0                 1.0589195   0.9696919   1.156357
18 months   ki1017093b-PROVIDE         BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
18 months   ki1017093b-PROVIDE         BANGLADESH                     1                    0                 1.1366424   0.8964778   1.441147
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     1                    0                 1.2393677   0.9556222   1.607363
18 months   ki1113344-GMS-Nepal        NEPAL                          0                    0                 1.0000000   1.0000000   1.000000
18 months   ki1113344-GMS-Nepal        NEPAL                          1                    0                 1.0006811   0.8306713   1.205486
24 months   ki1017093b-PROVIDE         BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
24 months   ki1017093b-PROVIDE         BANGLADESH                     1                    0                 1.1226387   0.8675523   1.452728
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    0                 1.0000000   1.0000000   1.000000
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     1                    0                 1.5358546   1.1347332   2.078770
24 months   ki1113344-GMS-Nepal        NEPAL                          0                    0                 1.0000000   1.0000000   1.000000
24 months   ki1113344-GMS-Nepal        NEPAL                          1                    0                 1.1919799   0.9283203   1.530523
24 months   ki1135781-COHORTS          INDIA                          0                    0                 1.0000000   1.0000000   1.000000
24 months   ki1135781-COHORTS          INDIA                          1                    0                 1.5895295   1.4910909   1.694467


### Parameter: PAR


agecat      studyid                    country                        intervention_level   baseline_level      estimate     ci_lower    ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  -----------  -----------  ----------
Birth       ki1135781-COHORTS          INDIA                          0                    NA                 0.0059123   -0.0054328   0.0172574
3 months    ki1000109-EE               PAKISTAN                       0                    NA                 0.0140480   -0.0473015   0.0753976
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                 0.1417526   -0.0331427   0.3166479
3 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0151211   -0.0124335   0.0426757
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0072061   -0.0262435   0.0406556
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    NA                 0.0013097   -0.0085046   0.0111241
3 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.0457099   -0.0052178   0.0966376
3 months    ki1135781-COHORTS          INDIA                          0                    NA                 0.0232476    0.0110904   0.0354047
6 months    ki1000109-EE               PAKISTAN                       0                    NA                 0.0148867   -0.0474621   0.0772354
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                -0.0416667   -0.2421137   0.1587803
6 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0018816   -0.0326229   0.0363862
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0202595   -0.0125158   0.0530348
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    NA                 0.0009979   -0.0123162   0.0143119
6 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.0500566   -0.0112056   0.1113188
6 months    ki1135781-COHORTS          INDIA                          0                    NA                 0.0428149    0.0296281   0.0560017
9 months    ki1000109-EE               PAKISTAN                       0                    NA                 0.0121058   -0.0496551   0.0738667
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                 0.0991597   -0.1140989   0.3124182
9 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0176676   -0.0190871   0.0544223
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0239613   -0.0101066   0.0580292
9 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.0296117   -0.0466906   0.1059139
9 months    ki1135781-COHORTS          INDIA                          0                    NA                 0.0608921    0.0446804   0.0771037
12 months   ki1000109-EE               PAKISTAN                       0                    NA                 0.0212781   -0.0369434   0.0794996
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                 0.0018116   -0.1615563   0.1651795
12 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0161310   -0.0238192   0.0560811
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0232315   -0.0115649   0.0580279
12 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.0400634   -0.0401728   0.1202995
12 months   ki1135781-COHORTS          INDIA                          0                    NA                 0.0713502    0.0524024   0.0902980
18 months   ki1000109-EE               PAKISTAN                       0                    NA                 0.0158289   -0.0316863   0.0633442
18 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0124136   -0.0339775   0.0588046
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0158409   -0.0243635   0.0560453
18 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.0002725   -0.0858840   0.0864291
24 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0098450   -0.0341829   0.0538729
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0291879   -0.0126562   0.0710319
24 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.0558708   -0.0316084   0.1433500
24 months   ki1135781-COHORTS          INDIA                          0                    NA                 0.0894121    0.0686787   0.1101455


### Parameter: PAF


agecat      studyid                    country                        intervention_level   baseline_level      estimate     ci_lower    ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  -----------  -----------  ----------
Birth       ki1135781-COHORTS          INDIA                          0                    NA                 0.0507353   -0.0517867   0.1432641
3 months    ki1000109-EE               PAKISTAN                       0                    NA                 0.0243239   -0.0878968   0.1249687
3 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                 0.3618421   -0.2822514   0.6823981
3 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.1250399   -0.1350528   0.3255334
3 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0336283   -0.1357789   0.1777676
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    NA                 0.0225982   -0.1622841   0.1780717
3 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.3170012   -0.1452082   0.5926615
3 months    ki1135781-COHORTS          INDIA                          0                    NA                 0.1502723    0.0679954   0.2252858
6 months    ki1000109-EE               PAKISTAN                       0                    NA                 0.0286878   -0.0992063   0.1417013
6 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                -0.0833333   -0.5684963   0.2517604
6 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0116702   -0.2272669   0.2040885
6 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0965704   -0.0738595   0.2399517
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   0                    NA                 0.0102507   -0.1364205   0.1379920
6 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.2536524   -0.1311430   0.5075470
6 months    ki1135781-COHORTS          INDIA                          0                    NA                 0.2189197    0.1486968   0.2833501
9 months    ki1000109-EE               PAKISTAN                       0                    NA                 0.0204005   -0.0894062   0.1191392
9 months    ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                 0.1478697   -0.2374104   0.4131890
9 months    ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0828596   -0.1067100   0.2399576
9 months    ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.1031504   -0.0560168   0.2383273
9 months    ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.1059028   -0.2131950   0.3410706
9 months    ki1135781-COHORTS          INDIA                          0                    NA                 0.2208957    0.1600737   0.2773133
12 months   ki1000109-EE               PAKISTAN                       0                    NA                 0.0297391   -0.0551351   0.1077860
12 months   ki1000304b-SAS-FoodSuppl   INDIA                          0                    NA                 0.0022831   -0.2263885   0.1883168
12 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0616470   -0.1041182   0.2025252
12 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0959150   -0.0596615   0.2286501
12 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.1172641   -0.1517698   0.3234563
12 months   ki1135781-COHORTS          INDIA                          0                    NA                 0.1964286    0.1427779   0.2467214
18 months   ki1000109-EE               PAKISTAN                       0                    NA                 0.0186097   -0.0388705   0.0729096
18 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0332636   -0.0993857   0.1499078
18 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.0525818   -0.0907033   0.1770436
18 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.0005093   -0.1741751   0.1492055
24 months   ki1017093b-PROVIDE         BANGLADESH                     0                    NA                 0.0298977   -0.1134561   0.1547951
24 months   ki1017093c-NIH-Crypto      BANGLADESH                     0                    NA                 0.1136557   -0.0649774   0.2623260
24 months   ki1113344-GMS-Nepal        NEPAL                          0                    NA                 0.1248405   -0.0941432   0.2999964
24 months   ki1135781-COHORTS          INDIA                          0                    NA                 0.1800892    0.1374914   0.2205832