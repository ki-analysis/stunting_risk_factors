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

**Outcome Variable:** ever_stunted

## Predictor Variables

**Intervention Variable:** hhwealth_quart

**Adjustment Set:**

unadjusted

## Stratifying Variables

The analysis was stratified on these variable(s):

* agecat
* studyid
* country

## Data Summary

agecat      studyid                    country                        A               n    nA   nAY0   nAY1
----------  -------------------------  -----------------------------  ----------  -----  ----  -----  -----
3 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q4      82    26     22      4
3 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q1      82     4      2      2
3 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q2      82    15     12      3
3 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q3      82    37     23     14
3 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q4       3     2      0      2
3 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q1       3     0      0      0
3 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q2       3     1      0      1
3 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q3       3     0      0      0
3 months    ki0047075b-MAL-ED          INDIA                          Wealth Q4      71    29     21      8
3 months    ki0047075b-MAL-ED          INDIA                          Wealth Q1      71     1      1      0
3 months    ki0047075b-MAL-ED          INDIA                          Wealth Q2      71    10      7      3
3 months    ki0047075b-MAL-ED          INDIA                          Wealth Q3      71    31     22      9
3 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q4      42    21     15      6
3 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q1      42    11      9      2
3 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q2      42     6      5      1
3 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q3      42     4      3      1
3 months    ki0047075b-MAL-ED          PERU                           Wealth Q4      37     1      1      0
3 months    ki0047075b-MAL-ED          PERU                           Wealth Q1      37    24     15      9
3 months    ki0047075b-MAL-ED          PERU                           Wealth Q2      37    11      6      5
3 months    ki0047075b-MAL-ED          PERU                           Wealth Q3      37     1      1      0
3 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4      68    13     10      3
3 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q1      68    12     10      2
3 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q2      68    24     22      2
3 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q3      68    19     11      8
3 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q4      60     0      0      0
3 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q1      60    39     30      9
3 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q2      60    21     15      6
3 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q3      60     0      0      0
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4     362    92     47     45
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1     362    90     71     19
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2     362    91     60     31
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3     362    89     59     30
3 months    ki1000108-IRC              INDIA                          Wealth Q4     410   100     71     29
3 months    ki1000108-IRC              INDIA                          Wealth Q1     410   105     69     36
3 months    ki1000108-IRC              INDIA                          Wealth Q2     410   102     66     36
3 months    ki1000108-IRC              INDIA                          Wealth Q3     410   103     74     29
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4     698   175    149     26
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1     698   180    136     44
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2     698   169    141     28
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3     698   174    142     32
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4    2381   591    511     80
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1    2381   718    652     66
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2    2381   483    434     49
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3    2381   589    541     48
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4     593   146    125     21
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q1     593   150    123     27
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q2     593   148    125     23
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q3     593   149    126     23
3 months    ki1114097-CONTENT          PERU                           Wealth Q4     215    52     42     10
3 months    ki1114097-CONTENT          PERU                           Wealth Q1     215    59     50      9
3 months    ki1114097-CONTENT          PERU                           Wealth Q2     215    52     43      9
3 months    ki1114097-CONTENT          PERU                           Wealth Q3     215    52     45      7
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4     482   186    141     45
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q1     482   107     78     29
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q2     482    87     62     25
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q3     482   102     70     32
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4    3055   843    757     86
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q1    3055   687    574    113
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q2    3055   541    443     98
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q3    3055   984    839    145
6 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q4      82    26     22      4
6 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q1      82     4      2      2
6 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q2      82    15     10      5
6 months    ki0047075b-MAL-ED          BANGLADESH                     Wealth Q3      82    37     22     15
6 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q4       3     2      0      2
6 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q1       3     0      0      0
6 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q2       3     1      0      1
6 months    ki0047075b-MAL-ED          BRAZIL                         Wealth Q3       3     0      0      0
6 months    ki0047075b-MAL-ED          INDIA                          Wealth Q4      71    29     18     11
6 months    ki0047075b-MAL-ED          INDIA                          Wealth Q1      71     1      1      0
6 months    ki0047075b-MAL-ED          INDIA                          Wealth Q2      71    10      7      3
6 months    ki0047075b-MAL-ED          INDIA                          Wealth Q3      71    31     20     11
6 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q4      42    21     14      7
6 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q1      42    11      9      2
6 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q2      42     6      5      1
6 months    ki0047075b-MAL-ED          NEPAL                          Wealth Q3      42     4      3      1
6 months    ki0047075b-MAL-ED          PERU                           Wealth Q4      36     1      0      1
6 months    ki0047075b-MAL-ED          PERU                           Wealth Q1      36    23     12     11
6 months    ki0047075b-MAL-ED          PERU                           Wealth Q2      36    11      5      6
6 months    ki0047075b-MAL-ED          PERU                           Wealth Q3      36     1      1      0
6 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4      68    13      9      4
6 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q1      68    12      8      4
6 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q2      68    24     21      3
6 months    ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q3      68    19      9     10
6 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q4      60     0      0      0
6 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q1      60    39     27     12
6 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q2      60    21     12      9
6 months    ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q3      60     0      0      0
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4     367    95     31     64
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1     367    90     55     35
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2     367    92     45     47
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3     367    90     48     42
6 months    ki1000108-IRC              INDIA                          Wealth Q4     408   100     60     40
6 months    ki1000108-IRC              INDIA                          Wealth Q1     408   105     61     44
6 months    ki1000108-IRC              INDIA                          Wealth Q2     408   101     51     50
6 months    ki1000108-IRC              INDIA                          Wealth Q3     408   102     63     39
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4     638   167    132     35
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1     638   156    102     54
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2     638   155    117     38
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3     638   160    124     36
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4    2225   551    413    138
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1    2225   672    556    116
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2    2225   445    350     95
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3    2225   557    461     96
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4     567   142    106     36
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q1     567   145     99     46
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q2     567   143    103     40
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q3     567   137     97     40
6 months    ki1114097-CONTENT          PERU                           Wealth Q4     215    52     40     12
6 months    ki1114097-CONTENT          PERU                           Wealth Q1     215    59     45     14
6 months    ki1114097-CONTENT          PERU                           Wealth Q2     215    52     40     12
6 months    ki1114097-CONTENT          PERU                           Wealth Q3     215    52     42     10
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4     136    51     33     18
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q1     136    38     22     16
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q2     136    22     16      6
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q3     136    25     16      9
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4    2805   770    623    147
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q1    2805   604    433    171
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q2    2805   502    365    137
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q3    2805   929    683    246
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q4     269    73     50     23
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q1     269    68     45     23
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q2     269    64     39     25
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q3     269    64     40     24
12 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q4      81    26     16     10
12 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q1      81     4      1      3
12 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q2      81    15      8      7
12 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q3      81    36     19     17
12 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q4       3     2      0      2
12 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q1       3     0      0      0
12 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q2       3     1      0      1
12 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q3       3     0      0      0
12 months   ki0047075b-MAL-ED          INDIA                          Wealth Q4      71    29     15     14
12 months   ki0047075b-MAL-ED          INDIA                          Wealth Q1      71     1      1      0
12 months   ki0047075b-MAL-ED          INDIA                          Wealth Q2      71    10      7      3
12 months   ki0047075b-MAL-ED          INDIA                          Wealth Q3      71    31     17     14
12 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q4      42    21     14      7
12 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q1      42    11      9      2
12 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q2      42     6      4      2
12 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q3      42     4      3      1
12 months   ki0047075b-MAL-ED          PERU                           Wealth Q4      36     1      0      1
12 months   ki0047075b-MAL-ED          PERU                           Wealth Q1      36    23      7     16
12 months   ki0047075b-MAL-ED          PERU                           Wealth Q2      36    11      5      6
12 months   ki0047075b-MAL-ED          PERU                           Wealth Q3      36     1      1      0
12 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4      68    13      9      4
12 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q1      68    12      8      4
12 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q2      68    24     17      7
12 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q3      68    19      8     11
12 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q4      60     0      0      0
12 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q1      60    39     14     25
12 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q2      60    21      5     16
12 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q3      60     0      0      0
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4     372    96     21     75
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1     372    90     32     58
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2     372    95     27     68
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3     372    91     32     59
12 months   ki1000108-IRC              INDIA                          Wealth Q4     408    99     53     46
12 months   ki1000108-IRC              INDIA                          Wealth Q1     408   105     48     57
12 months   ki1000108-IRC              INDIA                          Wealth Q2     408   101     43     58
12 months   ki1000108-IRC              INDIA                          Wealth Q3     408   103     57     46
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4     607   160    120     40
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1     607   145     76     69
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2     607   148    100     48
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3     607   154    109     45
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4    1988   484    303    181
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1    1988   606    436    170
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2    1988   400    264    136
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3    1988   498    354    144
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4     582   146     79     67
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1     582   148     74     74
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2     582   146     83     63
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3     582   142     81     61
12 months   ki1114097-CONTENT          PERU                           Wealth Q4     215    52     40     12
12 months   ki1114097-CONTENT          PERU                           Wealth Q1     215    59     43     16
12 months   ki1114097-CONTENT          PERU                           Wealth Q2     215    52     39     13
12 months   ki1114097-CONTENT          PERU                           Wealth Q3     215    52     39     13
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4     525   212     66    146
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q1     525   112     22     90
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q2     525   100     21     79
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q3     525   101     36     65
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4    2762   757    501    256
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1    2762   588    293    295
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2    2762   496    269    227
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3    2762   921    487    434
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4     794   214    118     96
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1     794   192     95     97
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2     794   193    107     86
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3     794   195    100     95
18 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q4      80    26     12     14
18 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q1      80     4      1      3
18 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q2      80    15      5     10
18 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q3      80    35     15     20
18 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q4       3     2      0      2
18 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q1       3     0      0      0
18 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q2       3     1      0      1
18 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q3       3     0      0      0
18 months   ki0047075b-MAL-ED          INDIA                          Wealth Q4      71    29     12     17
18 months   ki0047075b-MAL-ED          INDIA                          Wealth Q1      71     1      1      0
18 months   ki0047075b-MAL-ED          INDIA                          Wealth Q2      71    10      5      5
18 months   ki0047075b-MAL-ED          INDIA                          Wealth Q3      71    31     13     18
18 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q4      42    21     12      9
18 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q1      42    11      5      6
18 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q2      42     6      3      3
18 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q3      42     4      2      2
18 months   ki0047075b-MAL-ED          PERU                           Wealth Q4      36     1      0      1
18 months   ki0047075b-MAL-ED          PERU                           Wealth Q1      36    23      5     18
18 months   ki0047075b-MAL-ED          PERU                           Wealth Q2      36    11      2      9
18 months   ki0047075b-MAL-ED          PERU                           Wealth Q3      36     1      1      0
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4      68    13      7      6
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q1      68    12      7      5
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q2      68    24     13     11
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q3      68    19      7     12
18 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q4      60     0      0      0
18 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q1      60    39      9     30
18 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q2      60    21      2     19
18 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q3      60     0      0      0
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4     373    96      9     87
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1     373    91     19     72
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2     373    95     16     79
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3     373    91     13     78
18 months   ki1000108-IRC              INDIA                          Wealth Q4     409    99     52     47
18 months   ki1000108-IRC              INDIA                          Wealth Q1     409   105     42     63
18 months   ki1000108-IRC              INDIA                          Wealth Q2     409   102     40     62
18 months   ki1000108-IRC              INDIA                          Wealth Q3     409   103     45     58
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4     603   161    112     49
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1     603   143     60     83
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2     603   146     83     63
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3     603   153     97     56
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4    1448   352    198    154
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1    1448   441    274    167
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2    1448   298    179    119
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3    1448   357    210    147
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4     574   147     57     90
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1     574   144     49     95
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2     574   144     53     91
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3     574   139     57     82
18 months   ki1114097-CONTENT          PERU                           Wealth Q4     214    51     36     15
18 months   ki1114097-CONTENT          PERU                           Wealth Q1     214    59     40     19
18 months   ki1114097-CONTENT          PERU                           Wealth Q2     214    52     39     13
18 months   ki1114097-CONTENT          PERU                           Wealth Q3     214    52     39     13
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4     431   179     40    139
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q1     431    92      5     87
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q2     431    85      9     76
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q3     431    75     17     58
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4    2632   738    383    355
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1    2632   542    157    385
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2    2632   466    174    292
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3    2632   886    295    591
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4     672   183     82    101
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1     672   160     76     84
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2     672   165     71     94
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3     672   164     71     93
24 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q4      78    26     11     15
24 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q1      78     4      1      3
24 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q2      78    15      3     12
24 months   ki0047075b-MAL-ED          BANGLADESH                     Wealth Q3      78    33     13     20
24 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q4       3     2      0      2
24 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q1       3     0      0      0
24 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q2       3     1      0      1
24 months   ki0047075b-MAL-ED          BRAZIL                         Wealth Q3       3     0      0      0
24 months   ki0047075b-MAL-ED          INDIA                          Wealth Q4      71    29     12     17
24 months   ki0047075b-MAL-ED          INDIA                          Wealth Q1      71     1      1      0
24 months   ki0047075b-MAL-ED          INDIA                          Wealth Q2      71    10      4      6
24 months   ki0047075b-MAL-ED          INDIA                          Wealth Q3      71    31     12     19
24 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q4      42    21     11     10
24 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q1      42    11      4      7
24 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q2      42     6      3      3
24 months   ki0047075b-MAL-ED          NEPAL                          Wealth Q3      42     4      2      2
24 months   ki0047075b-MAL-ED          PERU                           Wealth Q4      32     1      0      1
24 months   ki0047075b-MAL-ED          PERU                           Wealth Q1      32    21      3     18
24 months   ki0047075b-MAL-ED          PERU                           Wealth Q2      32     9      1      8
24 months   ki0047075b-MAL-ED          PERU                           Wealth Q3      32     1      1      0
24 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4      67    13      7      6
24 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q1      67    12      7      5
24 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q2      67    24     10     14
24 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q3      67    18      4     14
24 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q4      60     0      0      0
24 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q1      60    39      5     34
24 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q2      60    21      2     19
24 months   ki0047075b-MAL-ED          TANZANIA, UNITED REPUBLIC OF   Wealth Q3      60     0      0      0
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4     373    96      6     90
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1     373    91      6     85
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2     373    95      8     87
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3     373    91      8     83
24 months   ki1000108-IRC              INDIA                          Wealth Q4     410   100     48     52
24 months   ki1000108-IRC              INDIA                          Wealth Q1     410   105     34     71
24 months   ki1000108-IRC              INDIA                          Wealth Q2     410   102     32     70
24 months   ki1000108-IRC              INDIA                          Wealth Q3     410   103     33     70
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4     581   153    100     53
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1     581   135     46     89
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2     581   143     73     70
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3     581   150     83     67
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4     958   230    129    101
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1     958   297    182    115
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2     958   196    104     92
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3     958   235    127    108
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4     568   147     50     97
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1     568   144     40    104
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2     568   143     40    103
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3     568   134     46     88
24 months   ki1114097-CONTENT          PERU                           Wealth Q4     197    46     32     14
24 months   ki1114097-CONTENT          PERU                           Wealth Q1     197    54     36     18
24 months   ki1114097-CONTENT          PERU                           Wealth Q2     197    47     34     13
24 months   ki1114097-CONTENT          PERU                           Wealth Q3     197    50     38     12
24 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4     456   191     27    164
24 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q1     456    95      3     92
24 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q2     456    89      8     81
24 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q3     456    81      9     72
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4    2562   728    277    451
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1    2562   522     88    434
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2    2562   445    105    340
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3    2562   867    164    703
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4     720   199     74    125
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1     720   171     61    110
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2     720   178     64    114
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3     720   172     52    120


The following strata were considered:

* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 12 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 12 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 12 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 12 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 12 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 12 months, studyid: ki1114097-CONTENT, country: PERU
* agecat: 12 months, studyid: ki1135781-COHORTS, country: GUATEMALA
* agecat: 12 months, studyid: ki1135781-COHORTS, country: PHILIPPINES
* agecat: 12 months, studyid: ki1148112-LCNI-5, country: MALAWI
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 18 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 18 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 18 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 18 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 18 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 18 months, studyid: ki1114097-CONTENT, country: PERU
* agecat: 18 months, studyid: ki1135781-COHORTS, country: GUATEMALA
* agecat: 18 months, studyid: ki1135781-COHORTS, country: PHILIPPINES
* agecat: 18 months, studyid: ki1148112-LCNI-5, country: MALAWI
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 24 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 24 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 24 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 24 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 24 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 24 months, studyid: ki1114097-CONTENT, country: PERU
* agecat: 24 months, studyid: ki1135781-COHORTS, country: GUATEMALA
* agecat: 24 months, studyid: ki1135781-COHORTS, country: PHILIPPINES
* agecat: 24 months, studyid: ki1148112-LCNI-5, country: MALAWI
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 3 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 3 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 3 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 3 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 3 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 3 months, studyid: ki1114097-CONTENT, country: PERU
* agecat: 3 months, studyid: ki1135781-COHORTS, country: GUATEMALA
* agecat: 3 months, studyid: ki1135781-COHORTS, country: PHILIPPINES
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 6 months, studyid: ki1000108-CMC-V-BCS-2002, country: INDIA
* agecat: 6 months, studyid: ki1000108-IRC, country: INDIA
* agecat: 6 months, studyid: ki1017093b-PROVIDE, country: BANGLADESH
* agecat: 6 months, studyid: ki1066203-TanzaniaChild2, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 6 months, studyid: ki1113344-GMS-Nepal, country: NEPAL
* agecat: 6 months, studyid: ki1114097-CONTENT, country: PERU
* agecat: 6 months, studyid: ki1135781-COHORTS, country: GUATEMALA
* agecat: 6 months, studyid: ki1135781-COHORTS, country: PHILIPPINES
* agecat: 6 months, studyid: ki1148112-LCNI-5, country: MALAWI

### Dropped Strata

Some strata were dropped due to rare outcomes:

* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 3 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 6 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 12 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 18 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: BANGLADESH
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: BRAZIL
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: INDIA
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: NEPAL
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: PERU
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: SOUTH AFRICA
* agecat: 24 months, studyid: ki0047075b-MAL-ED, country: TANZANIA, UNITED REPUBLIC OF
* agecat: 24 months, studyid: ki1135781-COHORTS, country: GUATEMALA

## Methods Detail

We're interested in the causal parameters $E[Y_a]$ for all values of $a \in \mathcal{A}$. These parameters represent the mean outcome if, possibly contrary to fact, we intervened to set all units to have $A=a$. Under the randomization and positivity assumptions, these are identified by the statistical parameters $\psi_a=E_W[E_{Y|A,W}(Y|A=a,W)]$.  In addition, we're interested in the mean of $Y$, $E[Y]$ under no intervention (the observed mean). We will estimate these parameters by using SuperLearner to fit the relevant likelihood factors -- $E_{Y|A,W}(Y|A=a,W)$ and $p(A=a|W)$, and then updating our likelihood fit using a joint TMLE.

For unadjusted analyses ($W=\{\}$), initial likelihoods were estimated using Lrnr_glm to estimate the simple $E(Y|A)$ and Lrnr_mean to estimate $p(A)$. For adjusted analyses, a small library containing Lrnr_glmnet, Lrnr_xgboost, and Lrnr_mean was used.

Having estimated these parameters, we will then use the delta method to estimate relative risks and attributable risks relative to a prespecified baseline level of $A$.

todo: add detail about dropping strata with rare outcomes, handling missingness







# Results Detail

## Results Plots
![](/tmp/390c6127-5036-4ae6-970d-637fb3575bd3/REPORT_files/figure-html/plot_tsm-1.png)<!-- -->


```
## Warning: Removed 44 rows containing missing values (geom_errorbar).
```

![](/tmp/390c6127-5036-4ae6-970d-637fb3575bd3/REPORT_files/figure-html/plot_rr-1.png)<!-- -->

![](/tmp/390c6127-5036-4ae6-970d-637fb3575bd3/REPORT_files/figure-html/plot_paf-1.png)<!-- -->

![](/tmp/390c6127-5036-4ae6-970d-637fb3575bd3/REPORT_files/figure-html/plot_par-1.png)<!-- -->

## Results Table

### Parameter: TSM


agecat      studyid                    country                        intervention_level   baseline_level     estimate    ci_lower    ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  ----------  ----------  ----------
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                0.4891304   0.3868430   0.5914179
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            NA                0.2111111   0.1266822   0.2955400
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            NA                0.3406593   0.2431507   0.4381680
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            NA                0.3370787   0.2387341   0.4354232
3 months    ki1000108-IRC              INDIA                          Wealth Q4            NA                0.2900000   0.2009556   0.3790444
3 months    ki1000108-IRC              INDIA                          Wealth Q1            NA                0.3428571   0.2519558   0.4337585
3 months    ki1000108-IRC              INDIA                          Wealth Q2            NA                0.3529412   0.2600870   0.4457953
3 months    ki1000108-IRC              INDIA                          Wealth Q3            NA                0.2815534   0.1945898   0.3685170
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                0.1485714   0.0958385   0.2013044
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            NA                0.2444444   0.1816174   0.3072715
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            NA                0.1656805   0.1095863   0.2217747
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            NA                0.1839080   0.1263038   0.2415123
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                0.1353638   0.1077762   0.1629514
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            NA                0.0919220   0.0707848   0.1130593
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            NA                0.1014493   0.0745177   0.1283808
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            NA                0.0814941   0.0593944   0.1035937
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                0.1438356   0.0868651   0.2008061
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            NA                0.1800000   0.1184664   0.2415336
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            NA                0.1554054   0.0969882   0.2138226
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            NA                0.1543624   0.0963014   0.2124234
3 months    ki1114097-CONTENT          PERU                           Wealth Q4            NA                0.1923077   0.0849384   0.2996770
3 months    ki1114097-CONTENT          PERU                           Wealth Q1            NA                0.1525424   0.0605846   0.2445002
3 months    ki1114097-CONTENT          PERU                           Wealth Q2            NA                0.1730769   0.0700120   0.2761419
3 months    ki1114097-CONTENT          PERU                           Wealth Q3            NA                0.1346154   0.0416309   0.2275999
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                0.2419355   0.1803263   0.3035447
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q1            NA                0.2710280   0.1867199   0.3553362
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q2            NA                0.2873563   0.1921675   0.3825452
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q3            NA                0.3137255   0.2235844   0.4038666
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                0.1020166   0.0815816   0.1224516
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            NA                0.1644833   0.1367578   0.1922088
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            NA                0.1811460   0.1486868   0.2136053
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            NA                0.1473577   0.1252068   0.1695086
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                0.6736842   0.5792725   0.7680960
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            NA                0.3888889   0.2880351   0.4897427
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            NA                0.5108696   0.4085841   0.6131551
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            NA                0.4666667   0.3634566   0.5698767
6 months    ki1000108-IRC              INDIA                          Wealth Q4            NA                0.4000000   0.3038639   0.4961361
6 months    ki1000108-IRC              INDIA                          Wealth Q1            NA                0.4190476   0.3245571   0.5135381
6 months    ki1000108-IRC              INDIA                          Wealth Q2            NA                0.4950495   0.3974227   0.5926763
6 months    ki1000108-IRC              INDIA                          Wealth Q3            NA                0.3823529   0.2879287   0.4767771
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                0.2095808   0.1478027   0.2713590
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            NA                0.3461538   0.2714404   0.4208673
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            NA                0.2451613   0.1773853   0.3129373
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            NA                0.2250000   0.1602454   0.2897546
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                0.2504537   0.2142684   0.2866391
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            NA                0.1726190   0.1440393   0.2011988
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            NA                0.2134831   0.1754027   0.2515635
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            NA                0.1723519   0.1409794   0.2037244
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                0.2535211   0.1819063   0.3251360
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            NA                0.3172414   0.2414228   0.3930600
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            NA                0.2797203   0.2060867   0.3533539
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            NA                0.2919708   0.2157688   0.3681728
6 months    ki1114097-CONTENT          PERU                           Wealth Q4            NA                0.2307692   0.1159866   0.3455518
6 months    ki1114097-CONTENT          PERU                           Wealth Q1            NA                0.2372881   0.1284822   0.3460941
6 months    ki1114097-CONTENT          PERU                           Wealth Q2            NA                0.2307692   0.1159866   0.3455518
6 months    ki1114097-CONTENT          PERU                           Wealth Q3            NA                0.1923077   0.0849384   0.2996770
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                0.3529412   0.2213010   0.4845814
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q1            NA                0.4210526   0.2634924   0.5786129
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q2            NA                0.2727273   0.0859379   0.4595167
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q3            NA                0.3600000   0.1711479   0.5488521
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                0.1909091   0.1631444   0.2186737
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            NA                0.2831126   0.2471780   0.3190471
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            NA                0.2729084   0.2339342   0.3118825
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            NA                0.2648009   0.2364230   0.2931787
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                0.3150685   0.2083053   0.4218317
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q1            NA                0.3382353   0.2255769   0.4508937
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q2            NA                0.3906250   0.2708712   0.5103788
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q3            NA                0.3750000   0.2561710   0.4938290
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                0.7812500   0.6984432   0.8640568
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            NA                0.6444444   0.5454165   0.7434724
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            NA                0.7157895   0.6249690   0.8066099
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            NA                0.6483516   0.5501155   0.7465878
12 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                0.4646465   0.3662805   0.5630125
12 months   ki1000108-IRC              INDIA                          Wealth Q1            NA                0.5428571   0.4474557   0.6382586
12 months   ki1000108-IRC              INDIA                          Wealth Q2            NA                0.5742574   0.4777086   0.6708063
12 months   ki1000108-IRC              INDIA                          Wealth Q3            NA                0.4466019   0.3504758   0.5427281
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                0.2500000   0.1828499   0.3171501
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            NA                0.4758621   0.3945068   0.5572173
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            NA                0.3243243   0.2488439   0.3998047
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            NA                0.2922078   0.2203218   0.3640938
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                0.3739669   0.3308498   0.4170841
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            NA                0.2805281   0.2447500   0.3163061
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            NA                0.3400000   0.2935657   0.3864343
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            NA                0.2891566   0.2493279   0.3289853
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                0.4589041   0.3780051   0.5398031
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            NA                0.5000000   0.4193767   0.5806233
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            NA                0.4315069   0.3510984   0.5119153
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            NA                0.4295775   0.3480889   0.5110660
12 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                0.2307692   0.1159866   0.3455518
12 months   ki1114097-CONTENT          PERU                           Wealth Q1            NA                0.2711864   0.1574822   0.3848907
12 months   ki1114097-CONTENT          PERU                           Wealth Q2            NA                0.2500000   0.1320333   0.3679667
12 months   ki1114097-CONTENT          PERU                           Wealth Q3            NA                0.2500000   0.1320333   0.3679667
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                0.6886792   0.6262904   0.7510681
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q1            NA                0.8035714   0.7299223   0.8772206
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q2            NA                0.7900000   0.7100929   0.8699071
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q3            NA                0.6435644   0.5500694   0.7370593
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                0.3381770   0.3044699   0.3718841
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            NA                0.5017007   0.4612798   0.5421215
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            NA                0.4576613   0.4138089   0.5015137
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            NA                0.4712269   0.4389831   0.5034708
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                0.4485981   0.3819209   0.5152754
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1            NA                0.5052083   0.4344435   0.5759732
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2            NA                0.4455959   0.3754298   0.5157619
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3            NA                0.4871795   0.4169804   0.5573786
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4            NA                0.4615385   0.1885308   0.7345461
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q1            NA                0.4166667   0.1356531   0.6976802
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q2            NA                0.4583333   0.2575090   0.6591577
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q3            NA                0.6315789   0.4130674   0.8500905
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                0.9062500   0.8478645   0.9646355
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            NA                0.7912088   0.7075884   0.8748291
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            NA                0.8315789   0.7562227   0.9069352
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            NA                0.8571429   0.7851502   0.9291355
18 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                0.4747475   0.3762608   0.5732341
18 months   ki1000108-IRC              INDIA                          Wealth Q1            NA                0.6000000   0.5061810   0.6938190
18 months   ki1000108-IRC              INDIA                          Wealth Q2            NA                0.6078431   0.5129783   0.7027080
18 months   ki1000108-IRC              INDIA                          Wealth Q3            NA                0.5631068   0.4672012   0.6590124
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                0.3043478   0.2332139   0.3754817
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            NA                0.5804196   0.4994692   0.6613700
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            NA                0.4315068   0.3511008   0.5119129
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            NA                0.3660131   0.2896205   0.4424057
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                0.4375000   0.3856586   0.4893414
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            NA                0.3786848   0.3333978   0.4239718
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            NA                0.3993289   0.3437034   0.4549543
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            NA                0.4117647   0.3606949   0.4628345
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                0.6122449   0.5334117   0.6910781
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            NA                0.6597222   0.5822684   0.7371760
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            NA                0.6319444   0.5531054   0.7107835
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            NA                0.5899281   0.5080912   0.6717649
18 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                0.2941176   0.1687727   0.4194626
18 months   ki1114097-CONTENT          PERU                           Wealth Q1            NA                0.3220339   0.2025267   0.4415411
18 months   ki1114097-CONTENT          PERU                           Wealth Q2            NA                0.2500000   0.1320320   0.3679680
18 months   ki1114097-CONTENT          PERU                           Wealth Q3            NA                0.2500000   0.1320320   0.3679680
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                0.7765363   0.7154407   0.8376320
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q1            NA                0.9456522   0.8992738   0.9920305
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q2            NA                0.8941176   0.8286311   0.9596042
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q3            NA                0.7733333   0.6784699   0.8681968
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                0.4810298   0.4449753   0.5170843
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            NA                0.7103321   0.6721366   0.7485276
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            NA                0.6266094   0.5826838   0.6705351
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            NA                0.6670429   0.6360055   0.6980802
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                0.5519126   0.4798081   0.6240171
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1            NA                0.5250000   0.4475649   0.6024351
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2            NA                0.5696970   0.4940940   0.6452999
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3            NA                0.5670732   0.4911846   0.6429617
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                0.9375000   0.8890135   0.9859865
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            NA                0.9340659   0.8830091   0.9851228
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            NA                0.9157895   0.8598717   0.9717073
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            NA                0.9120879   0.8538303   0.9703456
24 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                0.5200000   0.4219606   0.6180394
24 months   ki1000108-IRC              INDIA                          Wealth Q1            NA                0.6761905   0.5865791   0.7658018
24 months   ki1000108-IRC              INDIA                          Wealth Q2            NA                0.6862745   0.5961170   0.7764321
24 months   ki1000108-IRC              INDIA                          Wealth Q3            NA                0.6796117   0.5893863   0.7698370
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                0.3464052   0.2709442   0.4218663
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            NA                0.6592593   0.5792398   0.7392787
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            NA                0.4895105   0.4075077   0.5715133
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            NA                0.4466667   0.3670394   0.5262939
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                0.4391304   0.3749595   0.5033014
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            NA                0.3872054   0.3317779   0.4426328
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            NA                0.4693878   0.3994839   0.5392916
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            NA                0.4595745   0.3958235   0.5233254
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                0.6598639   0.5832116   0.7365163
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            NA                0.7222222   0.6490016   0.7954429
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            NA                0.7202797   0.6466462   0.7939132
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            NA                0.6567164   0.5762539   0.7371790
24 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                0.3043478   0.1710401   0.4376556
24 months   ki1114097-CONTENT          PERU                           Wealth Q1            NA                0.3333333   0.2072812   0.4593854
24 months   ki1114097-CONTENT          PERU                           Wealth Q2            NA                0.2765957   0.1483870   0.4048045
24 months   ki1114097-CONTENT          PERU                           Wealth Q3            NA                0.2400000   0.1213192   0.3586808
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                0.6195055   0.5842307   0.6547802
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            NA                0.8314176   0.7992948   0.8635404
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            NA                0.7640449   0.7245877   0.8035022
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            NA                0.8108420   0.7847682   0.8369158
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                0.6281407   0.5609451   0.6953364
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1            NA                0.6432749   0.5714265   0.7151232
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2            NA                0.6404494   0.5699051   0.7109938
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3            NA                0.6976744   0.6289914   0.7663575


### Parameter: E(Y)


agecat      studyid                    country                        intervention_level   baseline_level     estimate    ci_lower    ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  ----------  ----------  ----------
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          NA                   NA                0.3453039   0.3351147   0.3554930
3 months    ki1000108-IRC              INDIA                          NA                   NA                0.3170732   0.3140300   0.3201164
3 months    ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.1862464   0.1835359   0.1889570
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   NA                   NA                0.1020580   0.1012435   0.1028724
3 months    ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.1585160   0.1574456   0.1595864
3 months    ki1114097-CONTENT          PERU                           NA                   NA                0.1627907   0.1599261   0.1656553
3 months    ki1135781-COHORTS          GUATEMALA                      NA                   NA                0.2717842   0.2693206   0.2742478
3 months    ki1135781-COHORTS          PHILIPPINES                    NA                   NA                0.1446809   0.1436602   0.1457015
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          NA                   NA                0.5122616   0.5015225   0.5230007
6 months    ki1000108-IRC              INDIA                          NA                   NA                0.4240196   0.4198628   0.4281765
6 months    ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.2554859   0.2513616   0.2596102
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   NA                   NA                0.2000000   0.1986313   0.2013687
6 months    ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.2857143   0.2838136   0.2876149
6 months    ki1114097-CONTENT          PERU                           NA                   NA                0.2232558   0.2208855   0.2256261
6 months    ki1135781-COHORTS          GUATEMALA                      NA                   NA                0.3602941   0.3522180   0.3683703
6 months    ki1135781-COHORTS          PHILIPPINES                    NA                   NA                0.2499109   0.2485453   0.2512764
6 months    ki1148112-LCNI-5           MALAWI                         NA                   NA                0.3531599   0.3495731   0.3567466
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          NA                   NA                0.6989247   0.6931997   0.7046497
12 months   ki1000108-IRC              INDIA                          NA                   NA                0.5073529   0.5022060   0.5124999
12 months   ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.3327842   0.3260604   0.3395079
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   NA                   NA                0.3174044   0.3157037   0.3191051
12 months   ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.4553265   0.4530054   0.4576475
12 months   ki1114097-CONTENT          PERU                           NA                   NA                0.2511628   0.2492154   0.2531102
12 months   ki1135781-COHORTS          GUATEMALA                      NA                   NA                0.7238095   0.7184427   0.7291763
12 months   ki1135781-COHORTS          PHILIPPINES                    NA                   NA                0.4388125   0.4364440   0.4411809
12 months   ki1148112-LCNI-5           MALAWI                         NA                   NA                0.4710327   0.4692728   0.4727927
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   NA                   NA                0.5000000   0.4800258   0.5199742
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          NA                   NA                0.8471850   0.8429357   0.8514343
18 months   ki1000108-IRC              INDIA                          NA                   NA                0.5623472   0.5572701   0.5674243
18 months   ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.4162521   0.4080933   0.4244109
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   NA                   NA                0.4053867   0.4042515   0.4065219
18 months   ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.6236934   0.6216021   0.6257847
18 months   ki1114097-CONTENT          PERU                           NA                   NA                0.2803738   0.2761872   0.2845604
18 months   ki1135781-COHORTS          GUATEMALA                      NA                   NA                0.8352668   0.8283315   0.8422021
18 months   ki1135781-COHORTS          PHILIPPINES                    NA                   NA                0.6166413   0.6132587   0.6200240
18 months   ki1148112-LCNI-5           MALAWI                         NA                   NA                0.5535714   0.5522534   0.5548895
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          NA                   NA                0.9249330   0.9238081   0.9260579
24 months   ki1000108-IRC              INDIA                          NA                   NA                0.6414634   0.6347684   0.6481585
24 months   ki1017093b-PROVIDE         BANGLADESH                     NA                   NA                0.4802065   0.4711165   0.4892966
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   NA                   NA                0.4342380   0.4321350   0.4363410
24 months   ki1113344-GMS-Nepal        NEPAL                          NA                   NA                0.6901408   0.6875504   0.6927312
24 months   ki1114097-CONTENT          PERU                           NA                   NA                0.2893401   0.2844108   0.2942694
24 months   ki1135781-COHORTS          PHILIPPINES                    NA                   NA                0.7525371   0.7491897   0.7558844
24 months   ki1148112-LCNI-5           MALAWI                         NA                   NA                0.6513889   0.6494462   0.6533316


### Parameter: RR


agecat      studyid                    country                        intervention_level   baseline_level     estimate    ci_lower    ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  ----------  ----------  ----------
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            Wealth Q4         0.4316049   0.2748457   0.6777725
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            Wealth Q4         0.6964591   0.4885885   0.9927686
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            Wealth Q4         0.6891386   0.4812956   0.9867367
3 months    ki1000108-IRC              INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1000108-IRC              INDIA                          Wealth Q1            Wealth Q4         1.1822660   0.7880114   1.7737725
3 months    ki1000108-IRC              INDIA                          Wealth Q2            Wealth Q4         1.2170385   0.8122691   1.8235124
3 months    ki1000108-IRC              INDIA                          Wealth Q3            Wealth Q4         0.9708738   0.6280836   1.5007492
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            Wealth Q4         1.6452991   1.0615204   2.5501247
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            Wealth Q4         1.1151570   0.6828219   1.8212292
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            Wealth Q4         1.2378426   0.7710456   1.9872421
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            Wealth Q4         0.6790738   0.4994288   0.9233373
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            Wealth Q4         0.7494565   0.5362876   1.0473579
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            Wealth Q4         0.6020374   0.4288436   0.8451774
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            Wealth Q4         1.2514286   0.7416193   2.1116945
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            Wealth Q4         1.0804376   0.6258187   1.8653091
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            Wealth Q4         1.0731863   0.6215193   1.8530863
3 months    ki1114097-CONTENT          PERU                           Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1114097-CONTENT          PERU                           Wealth Q1            Wealth Q4         0.7932203   0.3487786   1.8040053
3 months    ki1114097-CONTENT          PERU                           Wealth Q2            Wealth Q4         0.9000000   0.3978628   2.0358778
3 months    ki1114097-CONTENT          PERU                           Wealth Q3            Wealth Q4         0.7000000   0.2879855   1.7014746
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q1            Wealth Q4         1.1202492   0.7494190   1.6745751
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q2            Wealth Q4         1.1877395   0.7820988   1.8037682
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q3            Wealth Q4         1.2967320   0.8833061   1.9036593
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            Wealth Q4         1.6123185   1.2409497   2.0948236
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            Wealth Q4         1.7756523   1.3571763   2.3231625
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            Wealth Q4         1.4444484   1.1244416   1.8555264
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            Wealth Q4         0.5772569   0.4298799   0.7751598
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            Wealth Q4         0.7583220   0.5939032   0.9682592
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            Wealth Q4         0.6927083   0.5331387   0.9000375
6 months    ki1000108-IRC              INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1000108-IRC              INDIA                          Wealth Q1            Wealth Q4         1.0476190   0.7534910   1.4565611
6 months    ki1000108-IRC              INDIA                          Wealth Q2            Wealth Q4         1.2376238   0.9069222   1.6889128
6 months    ki1000108-IRC              INDIA                          Wealth Q3            Wealth Q4         0.9558824   0.6772448   1.3491591
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            Wealth Q4         1.6516484   1.1461751   2.3800398
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            Wealth Q4         1.1697696   0.7808926   1.7523037
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            Wealth Q4         1.0735714   0.7110755   1.6208626
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            Wealth Q4         0.6892253   0.5532595   0.8586053
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            Wealth Q4         0.8523856   0.6775549   1.0723281
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            Wealth Q4         0.6881586   0.5454570   0.8681937
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            Wealth Q4         1.2513410   0.8643287   1.8116422
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            Wealth Q4         1.1033411   0.7499267   1.6233073
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            Wealth Q4         1.1516626   0.7839682   1.6918120
6 months    ki1114097-CONTENT          PERU                           Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1114097-CONTENT          PERU                           Wealth Q1            Wealth Q4         1.0282486   0.5227530   2.0225519
6 months    ki1114097-CONTENT          PERU                           Wealth Q2            Wealth Q4         1.0000000   0.4948911   2.0206464
6 months    ki1114097-CONTENT          PERU                           Wealth Q3            Wealth Q4         0.8333333   0.3945282   1.7601894
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q1            Wealth Q4         1.1929825   0.7033612   2.0234370
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q2            Wealth Q4         0.7727273   0.3542694   1.6854616
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q3            Wealth Q4         1.0200000   0.5358691   1.9415189
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            Wealth Q4         1.4829707   1.2226433   1.7987273
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            Wealth Q4         1.4295200   1.1659204   1.7527161
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            Wealth Q4         1.3870521   1.1578063   1.6616887
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q1            Wealth Q4         1.0735294   0.6675140   1.7265038
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q2            Wealth Q4         1.2398098   0.7850575   1.9579818
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q3            Wealth Q4         1.1902174   0.7484142   1.8928254
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            Wealth Q4         0.8248889   0.6844222   0.9941842
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            Wealth Q4         0.9162105   0.7765943   1.0809269
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            Wealth Q4         0.8298901   0.6897871   0.9984495
12 months   ki1000108-IRC              INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1000108-IRC              INDIA                          Wealth Q1            Wealth Q4         1.1683230   0.8873020   1.5383472
12 months   ki1000108-IRC              INDIA                          Wealth Q2            Wealth Q4         1.2359018   0.9431404   1.6195398
12 months   ki1000108-IRC              INDIA                          Wealth Q3            Wealth Q4         0.9611650   0.7106953   1.2999076
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            Wealth Q4         1.9034483   1.3844084   2.6170855
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            Wealth Q4         1.2972973   0.9092655   1.8509228
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            Wealth Q4         1.1688312   0.8120196   1.6824301
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            Wealth Q4         0.7501413   0.6316488   0.8908622
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            Wealth Q4         0.9091713   0.7603673   1.0870962
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            Wealth Q4         0.7732144   0.6460839   0.9253606
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            Wealth Q4         1.0895522   0.8580073   1.3835827
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            Wealth Q4         0.9402985   0.7275481   1.2152615
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            Wealth Q4         0.9360942   0.7225266   1.2127891
12 months   ki1114097-CONTENT          PERU                           Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1114097-CONTENT          PERU                           Wealth Q1            Wealth Q4         1.1751412   0.6131486   2.2522385
12 months   ki1114097-CONTENT          PERU                           Wealth Q2            Wealth Q4         1.0833333   0.5457666   2.1503900
12 months   ki1114097-CONTENT          PERU                           Wealth Q3            Wealth Q4         1.0833333   0.5457666   2.1503900
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q1            Wealth Q4         1.1668297   1.0257480   1.3273159
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q2            Wealth Q4         1.1471233   1.0014723   1.3139573
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q3            Wealth Q4         0.9344907   0.7874450   1.1089954
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            Wealth Q4         1.4835446   1.3050884   1.6864026
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            Wealth Q4         1.3533187   1.1785675   1.5539811
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            Wealth Q4         1.3934327   1.2347526   1.5725051
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1            Wealth Q4         1.1261936   0.9181524   1.3813741
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2            Wealth Q4         0.9933074   0.7999142   1.2334568
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3            Wealth Q4         1.0860043   0.8829299   1.3357858
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q1            Wealth Q4         0.9027778   0.3681157   2.2139989
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q2            Wealth Q4         0.9930556   0.4756409   2.0733276
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q3            Wealth Q4         1.3684211   0.6896232   2.7153615
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            Wealth Q4         0.8730580   0.7714151   0.9880935
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            Wealth Q4         0.9176044   0.8210471   1.0255170
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            Wealth Q4         0.9458128   0.8508111   1.0514224
18 months   ki1000108-IRC              INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1000108-IRC              INDIA                          Wealth Q1            Wealth Q4         1.2638298   0.9746921   1.6387387
18 months   ki1000108-IRC              INDIA                          Wealth Q2            Wealth Q4         1.2803504   0.9876096   1.6598635
18 months   ki1000108-IRC              INDIA                          Wealth Q3            Wealth Q4         1.1861186   0.9069009   1.5513020
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            Wealth Q4         1.9070929   1.4526725   2.5036636
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            Wealth Q4         1.4178082   1.0514796   1.9117633
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            Wealth Q4         1.2026144   0.8791016   1.6451811
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            Wealth Q4         0.8655653   0.7314505   1.0242707
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            Wealth Q4         0.9127517   0.7602024   1.0959129
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            Wealth Q4         0.9411765   0.7928211   1.1172927
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            Wealth Q4         1.0775463   0.9052326   1.2826604
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            Wealth Q4         1.0321759   0.8627614   1.2348572
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            Wealth Q4         0.9635492   0.7973967   1.1643225
18 months   ki1114097-CONTENT          PERU                           Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1114097-CONTENT          PERU                           Wealth Q1            Wealth Q4         1.0949153   0.6222432   1.9266411
18 months   ki1114097-CONTENT          PERU                           Wealth Q2            Wealth Q4         0.8500000   0.4500691   1.6053089
18 months   ki1114097-CONTENT          PERU                           Wealth Q3            Wealth Q4         0.8500000   0.4500691   1.6053089
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q1            Wealth Q4         1.2177823   1.1099557   1.3360837
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q2            Wealth Q4         1.1514177   1.0340700   1.2820821
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q3            Wealth Q4         0.9958753   0.8608246   1.1521135
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            Wealth Q4         1.4766904   1.3465660   1.6193892
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            Wealth Q4         1.3026416   1.1755883   1.4434263
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            Wealth Q4         1.3866976   1.2696029   1.5145919
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1            Wealth Q4         0.9512376   0.7811197   1.1584050
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2            Wealth Q4         1.0322232   0.8568359   1.2435108
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3            Wealth Q4         1.0274692   0.8522092   1.2387721
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q1            Wealth Q4         0.9963370   0.9241135   1.0742051
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q2            Wealth Q4         0.9768421   0.9017212   1.0582212
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q3            Wealth Q4         0.9728938   0.8961328   1.0562300
24 months   ki1000108-IRC              INDIA                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1000108-IRC              INDIA                          Wealth Q1            Wealth Q4         1.3003663   1.0327161   1.6373837
24 months   ki1000108-IRC              INDIA                          Wealth Q2            Wealth Q4         1.3197587   1.0488092   1.6607052
24 months   ki1000108-IRC              INDIA                          Wealth Q3            Wealth Q4         1.3069455   1.0378000   1.6458918
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q1            Wealth Q4         1.9031447   1.4830998   2.4421550
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q2            Wealth Q4         1.4131152   1.0735730   1.8600454
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q3            Wealth Q4         1.2894340   0.9730857   1.7086265
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q1            Wealth Q4         0.8817548   0.7186337   1.0819025
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q2            Wealth Q4         1.0689028   0.8676092   1.3168984
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q3            Wealth Q4         1.0465557   0.8555741   1.2801684
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q1            Wealth Q4         1.0945017   0.9381138   1.2769602
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q2            Wealth Q4         1.0915579   0.9350688   1.2742364
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q3            Wealth Q4         0.9952300   0.8406179   1.1782795
24 months   ki1114097-CONTENT          PERU                           Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1114097-CONTENT          PERU                           Wealth Q1            Wealth Q4         1.0952381   0.6140397   1.9535323
24 months   ki1114097-CONTENT          PERU                           Wealth Q2            Wealth Q4         0.9088146   0.4802969   1.7196530
24 months   ki1114097-CONTENT          PERU                           Wealth Q3            Wealth Q4         0.7885714   0.4073312   1.5266320
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q1            Wealth Q4         1.3420666   1.2528235   1.4376668
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q2            Wealth Q4         1.2333142   1.1420605   1.3318594
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q3            Wealth Q4         1.3088536   1.2260024   1.3973037
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            Wealth Q4         1.0000000   1.0000000   1.0000000
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q1            Wealth Q4         1.0240936   0.8773502   1.1953808
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q2            Wealth Q4         1.0195955   0.8744676   1.1888090
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q3            Wealth Q4         1.1106977   0.9604134   1.2844983


### Parameter: PAR


agecat      studyid                    country                        intervention_level   baseline_level      estimate     ci_lower     ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  -----------  -----------  -----------
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.1438266   -0.2466202   -0.0410329
3 months    ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.0270732   -0.0620232    0.1161695
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.0376750   -0.0151276    0.0904776
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.0333058   -0.0609054   -0.0057062
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.0146804   -0.0423001    0.0716609
3 months    ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.0295170   -0.1369245    0.0778905
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.0298487   -0.0318097    0.0915072
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.0426642    0.0222038    0.0631247
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.1614226   -0.2564432   -0.0664021
6 months    ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.0240196   -0.0722063    0.1202456
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.0459051   -0.0160106    0.1078207
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.0504537   -0.0866650   -0.0142425
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.0321932   -0.0394469    0.1038332
6 months    ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.0075134   -0.1223205    0.1072936
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.0073529   -0.1245348    0.1392407
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.0590018    0.0312036    0.0868000
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.0380914   -0.0687320    0.1449148
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.0823253   -0.1653297    0.0006792
12 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.0427065   -0.0557941    0.1412070
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.0827842    0.0152983    0.1502701
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.0565625   -0.0997132   -0.0134119
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                -0.0035776   -0.0845099    0.0773546
12 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                 0.0203936   -0.0944056    0.1351927
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.0351303   -0.0274889    0.0977495
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.1006354    0.0668452    0.1344257
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.0224346   -0.0442659    0.0891351
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4            NA                 0.0384615   -0.2352758    0.3121989
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.0590650   -0.1176049   -0.0005251
18 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.0875997   -0.0110177    0.1862172
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.1119042    0.0403040    0.1835045
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.0321133   -0.0839671    0.0197406
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.0114485   -0.0674125    0.0903095
18 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.0137438   -0.1391586    0.1116710
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.0587305   -0.0027575    0.1202185
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.1356115    0.0993987    0.1718244
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.0016589   -0.0704577    0.0737754
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.0125670   -0.0610666    0.0359325
24 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.1214634    0.0231957    0.2197312
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.1338013    0.0577947    0.2098079
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.0048924   -0.0690979    0.0593130
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.0302769   -0.0464192    0.1069730
24 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.0150077   -0.1484066    0.1183911
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.1330316    0.0975984    0.1684648
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.0232482   -0.0439755    0.0904719


### Parameter: PAF


agecat      studyid                    country                        intervention_level   baseline_level      estimate     ci_lower     ci_upper
----------  -------------------------  -----------------------------  -------------------  ---------------  -----------  -----------  -----------
3 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.4165217   -0.7496170   -0.1468418
3 months    ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.0853846   -0.2435223    0.3272969
3 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.2022857   -0.1379482    0.4407935
3 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.3263423   -0.6264251   -0.0816262
3 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.0926115   -0.3484470    0.3894058
3 months    ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.1813187   -1.0652037    0.3242730
3 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.1098252   -0.1485212    0.3100595
3 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.2948852    0.1383962    0.4229518
6 months    ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.3151176   -0.5153218   -0.1413643
6 months    ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.0566474   -0.1998841    0.2583333
6 months    ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.1796775   -0.1020302    0.3893733
6 months    ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.2522686   -0.4471527   -0.0836290
6 months    ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.1126761   -0.1770531    0.3310890
6 months    ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.0336538   -0.6999596    0.3714908
6 months    ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.0204082   -0.4233800    0.3258299
6 months    ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.2360913    0.1164174    0.3395563
6 months    ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.1078587   -0.2521705    0.3643708
12 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.1177885   -0.2431654   -0.0050561
12 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.0841751   -0.1320313    0.2590882
12 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.2487624    0.0165357    0.4261531
12 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.1782033   -0.3223517   -0.0497684
12 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                -0.0078573   -0.2022414    0.1550978
12 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                 0.0811966   -0.5109953    0.4412956
12 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.0485353   -0.0420003    0.1312045
12 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.2293359    0.1484385    0.3025481
12 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.0476286   -0.1050400    0.1792049
18 months   ki0047075b-MAL-ED          SOUTH AFRICA                   Wealth Q4            NA                 0.0769231   -0.6699960    0.4897766
18 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.0697191   -0.1411271   -0.0027796
18 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.1557751   -0.0390539    0.3140726
18 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.2688377    0.0755660    0.4217020
18 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.0792164   -0.2150230    0.0414108
18 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.0183559   -0.1165886    0.1369918
18 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.0490196   -0.6068734    0.3151656
18 months   ki1135781-COHORTS          GUATEMALA                      Wealth Q4            NA                 0.0703135   -0.0062255    0.1410305
18 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.2199196    0.1590349    0.2763964
18 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.0029967   -0.1361727    0.1251192
24 months   ki1000108-CMC-V-BCS-2002   INDIA                          Wealth Q4            NA                -0.0135870   -0.0674032    0.0375159
24 months   ki1000108-IRC              INDIA                          Wealth Q4            NA                 0.1893536    0.0208764    0.3288411
24 months   ki1017093b-PROVIDE         BANGLADESH                     Wealth Q4            NA                 0.2786328    0.1023237    0.4203138
24 months   ki1066203-TanzaniaChild2   TANZANIA, UNITED REPUBLIC OF   Wealth Q4            NA                -0.0112667   -0.1704823    0.1262915
24 months   ki1113344-GMS-Nepal        NEPAL                          Wealth Q4            NA                 0.0438706   -0.0739705    0.1487816
24 months   ki1114097-CONTENT          PERU                           Wealth Q4            NA                -0.0518688   -0.6305393    0.3214343
24 months   ki1135781-COHORTS          PHILIPPINES                    Wealth Q4            NA                 0.1767774    0.1283916    0.2224772
24 months   ki1148112-LCNI-5           MALAWI                         Wealth Q4            NA                 0.0356902   -0.0732317    0.1335576