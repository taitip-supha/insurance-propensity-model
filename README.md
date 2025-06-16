# insurance-propensity-model

## 📊 Input Feature Definitions
| Feature | Field Type | Definition |
|---------|------------|------------|
| `num_children` | Demographics | Total number of children. |
| `age` | Demographics | Current age at the campaign begins. |
| `income` | Demographics | Income at the campaign begins. |
| `maxosdc_last_30d` | Balance & Transaction | Max debit card outstanding balance in the last 30 days. |
| `dcspend_last_30d` | Balance & Transaction | Total spending via debit card in the last 30 days. |
| `easypymt_last_30d` | Balance & Transaction | Total payment in the last 30 days. |
| `savacc_bal` | Balance & Transaction | Total saving account balance in the last 30 days. |
| `currentacc_bal` | Balance & Transaction | Total current account balance in the last 30 days. |
| `avg_savaccbal_30d` | Balance & Transaction | Avg. of saving account balance in the last 30 days. |
| `avg_currentaccbal_30d` | Balance & Transaction | Avg. of current account balance in the last 30 days. |
| `mob` | Product Holding | Month on book (number of months since account opened). |
| `inflow30d` | Balance & Transaction | Total inflow to accounts in the last 30 days. |
| `outflow30d` | Balance & Transaction | Total outflow from accounts in the last 30 days. |
| `inflow1_15` | Balance & Transaction | Total inflow in the first 15 days. |
| `outflow1_15` | Balance & Transaction | Total outflow in the first 15 days. |
| `net_flow_30d` | Balance & Transaction | Inflow minus outflow in the last 30 days. |
| `net_flow_15d` | Balance & Transaction | Inflow minus outflow in the first 15 days. |
| `payroll` | Product Holding | Flag: 1 if customer has payroll, 0 otherwise. |
| `have_cc` | Product Holding | Flag: 1 if customer has/had credit card. |
| `have_acc_planet` | Product Holding | Flag: 1 if customer has travel card account. |
| `ntu_flag` | Product Holding | Flag: 1 if customer_segment is null. |
| `occ_sa` | Demographics | Flag: Occupation is Salary Man. |
| `occ_se` | Demographics | Flag: Occupation is Self-Employed. |
| `occ_gov` | Demographics | Flag: Occupation is Government. |
| `occ_prof` | Demographics | Flag: Occupation is Professional. |
| `occ_ent` | Demographics | Flag: Occupation is Entertainer. |
| `occ_frl` | Demographics | Flag: Occupation is Freelance. |
| `occ_hwf` | Demographics | Flag: Occupation is Housewife. |
| `occ_stu` | Demographics | Flag: Occupation is Student. |
| `occ_une` | Demographics | Flag: Occupation is Unemployed. |
| `seg_lmass` | Segment | Flag: Customer is Lower Mass segment. |
| `seg_mass` | Segment | Flag: Customer is Mass segment. |
| `seg_umass` | Segment | Flag: Customer is Upper Mass segment. |
| `gender_female` | Demographics | Flag: 1 if customer is female. |
| `sta_single` | Demographics | Flag: 1 if customer is single. |
| `avgsav2incm` | Balance & Transaction | avg_savaccbal_30d / income |
| `avgsav2inflow` | Balance & Transaction | avg_savaccbal_30d / inflow30d |
| `debitspend2inflow` | Balance & Transaction | dcspend_last_30d / inflow30d |
| `savings_ratio` | Balance & Transaction | savacc_bal / (savacc_bal + currentacc_bal) |
| `sav_stability` | Balance & Transaction | avg_savaccbal_30d / savacc_bal |
| `netflow2inflow` | Balance & Transaction | net_flow_30d / inflow30d |
| `bank_sav` | Product Holding | Flag: 1 if avg_savaccbal_30d > 0 |
| `bank_cur` | Product Holding | Flag: 1 if avg_currentaccbal_30d > 0 |
| `bank_prod` | Product Holding | payroll + have_cc + have_acc_planet + bank_sav + bank_cur |
