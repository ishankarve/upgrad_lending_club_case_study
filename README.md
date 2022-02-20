# Project Name
> You work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile.

In this case study, you will use EDA to understand how consumer attributes and loan attributes influence the tendency of default.


## Table of Contents
* [Data Dictionary](#data-dictionary)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## Data Dictionary
* [acc_now_delinq] The number of accounts on which the borrower is now delinquent.
* [acc_open_past_24mths] Number of trades opened in past 24 months.
* [addr_state] The state provided by the borrower in the loan application
* [all_util] Balance to credit limit on all trades
* [annual_inc] The self-reported annual income provided by the borrower during registration.
* [annual_inc_joint] The combined self-reported annual income provided by the co-borrowers during registration
* [application_type] Indicates whether the loan is an individual application or a joint application with two co-borrowers
* [avg_cur_bal] Average current balance of all accounts
* [bc_open_to_buy] Total open to buy on revolving bankcards.
* [bc_util] Ratio of total current balance to high credit/credit limit for all bankcard accounts.
* [chargeoff_within_12_mths] Number of charge-offs within 12 months
* [collection_recovery_fee] post charge off collection fee
* [collections_12_mths_ex_med] Number of collections in 12 months excluding medical collections
* [delinq_2yrs] The number of 30+ days past-due incidences of delinquency in the borrower's credit file for the past 2 years
* [delinq_amnt] The past-due amount owed for the accounts on which the borrower is now delinquent.
* [desc] Loan description provided by the borrower
* [dti] A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LC loan, divided by the borrower’s self-reported monthly income.
* [dti_joint] A ratio calculated using the co-borrowers' total monthly payments on the total debt obligations, excluding mortgages and the requested LC loan, divided by the co-borrowers' combined self-reported monthly income
* [earliest_cr_line] The month the borrower's earliest reported credit line was opened
* [emp_length] Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years. 
* [emp_title] The job title supplied by the Borrower when applying for the loan.*
* [fico_range_high] The upper boundary range the borrower’s FICO at loan origination belongs to.
* [fico_range_low] The lower boundary range the borrower’s FICO at loan origination belongs to.
* [funded_amnt] The total amount committed to that loan at that point in time.
* [funded_amnt_inv] The total amount committed by investors for that loan at that point in time.
* [grade] LC assigned loan grade
* [home_ownership] The home ownership status provided by the borrower during registration. Our values are: RENT, OWN, MORTGAGE, OTHER.
* [id] A unique LC assigned ID for the loan listing.
* [il_util] Ratio of total current balance to high credit/credit limit on all install acct
* [initial_list_status] The initial listing status of the loan. Possible values are – W, F
* [inq_fi] Number of personal finance inquiries
* [inq_last_12m] Number of credit inquiries in past 12 months
* [inq_last_6mths] The number of inquiries in past 6 months (excluding auto and mortgage inquiries)
* [installment] The monthly payment owed by the borrower if the loan originates.
* [int_rate] Interest Rate on the loan
* [issue_d] The month which the loan was funded
* [last_credit_pull_d] The most recent month LC pulled credit for this loan
* [last_fico_range_high] The upper boundary range the borrower’s last FICO pulled belongs to.
* [last_fico_range_low] The lower boundary range the borrower’s last FICO pulled belongs to.
* [last_pymnt_amnt] Last total payment amount received
* [last_pymnt_d] Last month payment was received
* [loan_amnt] The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.
* [loan_status] Current status of the loan
* [max_bal_bc] Maximum current balance owed on all revolving accounts
* [member_id] A unique LC assigned Id for the borrower member.
* [mo_sin_old_il_acct] Months since oldest bank installment account opened
* [mo_sin_old_rev_tl_op] Months since oldest revolving account opened
* [mo_sin_rcnt_rev_tl_op] Months since most recent revolving account opened
* [mo_sin_rcnt_tl] Months since most recent account opened
* [mort_acc] Number of mortgage accounts.
* [mths_since_last_delinq] The number of months since the borrower's last delinquency.
* [mths_since_last_major_derog] Months since most recent 90-day or worse rating
* [mths_since_last_record] The number of months since the last public record.
* [mths_since_rcnt_il] Months since most recent installment accounts opened
* [mths_since_recent_bc] Months since most recent bankcard account opened.
* [mths_since_recent_bc_dlq] Months since most recent bankcard delinquency
* [mths_since_recent_inq] Months since most recent inquiry.
* [mths_since_recent_revol_delinq] Months since most recent revolving delinquency.
* [next_pymnt_d] Next scheduled payment date
* [num_accts_ever_120_pd] Number of accounts ever 120 or more days past due
* [num_actv_bc_tl] Number of currently active bankcard accounts
* [num_actv_rev_tl] Number of currently active revolving trades
* [num_bc_sats] Number of satisfactory bankcard accounts
* [num_bc_tl] Number of bankcard accounts
* [num_il_tl] Number of installment accounts
* [num_op_rev_tl] Number of open revolving accounts
* [num_rev_accts] Number of revolving accounts
* [num_rev_tl_bal_gt_0] Number of revolving trades with balance >0
* [num_sats] Number of satisfactory accounts
* [num_tl_120dpd_2m] Number of accounts currently 120 days past due (updated in past 2 months)
* [num_tl_30dpd] Number of accounts currently 30 days past due (updated in past 2 months)
* [num_tl_90g_dpd_24m] Number of accounts 90 or more days past due in last 24 months
* [num_tl_op_past_12m] Number of accounts opened in past 12 months
* [open_acc] The number of open credit lines in the borrower's credit file.
* [open_acc_6m] Number of open trades in last 6 months
* [open_il_12m] Number of installment accounts opened in past 12 months
* [open_il_24m] Number of installment accounts opened in past 24 months
* [open_il_6m] Number of currently active installment trades
* [open_rv_12m] Number of revolving trades opened in past 12 months
* [open_rv_24m] Number of revolving trades opened in past 24 months
* [out_prncp] Remaining outstanding principal for total amount funded
* [out_prncp_inv] Remaining outstanding principal for portion of total amount funded by investors
* [pct_tl_nvr_dlq] Percent of trades never delinquent
* [percent_bc_gt_75] Percentage of all bankcard accounts > 75% of limit.
* [policy_code] publicly available policy_code=1 new products not publicly available policy_code=2
* [pub_rec] Number of derogatory public records
* [pub_rec_bankruptcies] Number of public record bankruptcies
* [purpose] A category provided by the borrower for the loan request. 
* [pymnt_plan] Indicates if a payment plan has been put in place for the loan
* [recoveries] post charge off gross recovery
* [revol_bal] Total credit revolving balance
* [revol_util] Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.
* [sub_grade] LC assigned loan subgrade
* [tax_liens] Number of tax liens
* [term] The number of payments on the loan. Values are in months and can be either 36 or 60.
* [title] The loan title provided by the borrower
* [tot_coll_amt] Total collection amounts ever owed
* [tot_cur_bal] Total current balance of all accounts
* [tot_hi_cred_lim] Total high credit/credit limit
* [total_acc] The total number of credit lines currently in the borrower's credit file
* [total_bal_ex_mort] Total credit balance excluding mortgage
* [total_bal_il] Total current balance of all installment accounts
* [total_bc_limit] Total bankcard high credit/credit limit
* [total_cu_tl] Number of finance trades
* [total_il_high_credit_limit] Total installment high credit/credit limit
* [total_pymnt] Payments received to date for total amount funded
* [total_pymnt_inv] Payments received to date for portion of total amount funded by investors
* [total_rec_int] Interest received to date
* [total_rec_late_fee] Late fees received to date
* [total_rec_prncp] Principal received to date
* [total_rev_hi_lim  ] Total revolving high credit/credit limit
* [url] URL for the LC page with listing data.
* [verification_status] Indicates if income was verified by LC, not verified, or if the income source was verified
* [verified_status_joint] Indicates if the co-borrowers' joint income was verified by LC, not verified, or if the income source was verified
* [zip_code] The first 3 numbers of the zip code provided by the borrower in the loan application.

#### Employer Title replaces Employer Name for all loans listed after 9/23/2013

## General Information
- Provide general information about your project here.
- What is the background of your project?
- What is the business probem that your project is trying to solve?
- What is the dataset that is being used?

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- Conclusion 1 from the analysis
- Conclusion 2 from the analysis
- Conclusion 3 from the analysis
- Conclusion 4 from the analysis

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- library - version 1.0
- library - version 2.0
- library - version 3.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).


## Contact
Created by [@gishankarve] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->