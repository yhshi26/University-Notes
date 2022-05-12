# L5: Epidemiological investigation and estimation of risk from cohort and case-control studies
[PHPS20010_2020-21 EPI(4)_27Jan2022](https://brightspace.ucd.ie/d2l/le/content/158326/viewContent/1850320/View)
###### tags: `PHPS20010 - Epidemiology, Biostatistics and Public Health`

## Learning objectives
- Provide evidence linking exposure to occurence of disease in a population
- Provide estimates of magnitude of risk related to a particular level of exposure/dose
- Quantify probability that observed relationships are real vs. have occured by chance
- Should have potential to control for other risk factors and/or confounders of outcome illness being studied

## Basic elements of conducting epidemiological studies
1. Formulation of study question/hypothesis
2. Selection of study populations and study samples
3. Selection of indicators of exposure
4. Measurements of exposure and disease
5. Evaluation of role of bias and confounding
6. Analysis and interpretation of relationship between exposure and disease
7. Evaluation of role of chance

### 1. Formulation of study question/hypothesis
Study question should be formulated such that it can be tested using statistical methods, e.g.
- Concern: exposure to wastewater compared with no exposure to wastewater increases rate of ascaris infection
- Null hypothesis: any observed differences are due to change (e.g. sampling error or other chance occurrence)

Hypothesis formation:
- H~0~ = "null" hypothesis (assumed/to be "disproven")
    - H~0~ states there is no association between exposure and disease of interest
- H~a~ = "alternative" hypothesis
    - H~a~ states there is an association between exposure and disease of interest

### 2. Selection of study populations and study samples
Choice of study population will depend on:
- Research question/subject of search
- Type of epidemiological study best suited to address research question

Fundamentally, investigation is about comparison of a study population exposed (to factor(s) of interest) and a control population (not exposed to factor(s) of interest)

In prospective cohort study angle cohort is recruited followed longitudinally and analysis is on exposure status

In retrospective case control study cases (with disease) and controls (without disease) are assessed for prior exposures

#### Cohort and case control studies
![](https://i.imgur.com/ypDpEyc.png =350x)

Samples from exposure and control populations need to be as similar as possible to each other ina ll other factors other than factors of interest e.g. socioeconomic status and other risk factors for disease outcome of interest
- Since samples never 100% same, need to record possible confounding factors and control for them in analysis

Difficulties arise due to selection bias and sample size

### 3. Selection of indicators of exposure
- Generic exposures
    - Age, gender, occupation, ethnicity
- Specific exposures
    - Smoking, alcohol consumption, dietary factors, medications, family history, environmental exposures, contaminated water, behavioural/lifestyle factors, etc.
    - Think of webs of causation

### 4. Measurement of exposure and disease
- How/study instruments (including questionnaires)
    - Issues of:
        - Source (standard available/self-designed?)
        - Design
        - Accuracy
- Potential for measurement error
    - Bias (in recall, interpretation, etc.)
    - Lack of standardisation in definition/measurement
- Omission of potential confounding factors
    - Factors which can be related to suspected cause and outcome

### 5. Evaluation of role of bias and confounding
Bias is any systematic error that results in an incorrect estimate of association beyweem exposure and disease

Types of bias include: selection bias, information bias, recall bias, confounding

Efforts to reduce bias are critical

#### 1. Selection bias
- Occures when inclusion fo study subjects on bias of either exposure/diases is somehow related to disease/exposure being studied
- Patients in hospital/more severe end of disease spectrum
- Selected samples not representative of population from which drawn
- Samples which are too small to give meaningful results

#### 2. Information bias:
- Occurs when there are systematic differences in way data on exposure/outcome are obtained from different study groups
- Recall bias occurs when reporting of disease status is different depending on exposure status (or vice versa in case-control study)
- Interviewer bias occurs when interviewersare aware of exposure status of individuals and probe for answers on disease status differentially between exposure groups
- In cohort studies where individuals leave study or are otherwise lost to follow-up, there can be bias if those lost are different to those who remain
- These types of bias can generally be dealt with by careful design and conduct of a study

#### 3. Confounding
- Occurs when relationship between exposure and disease is attributable (partly/wholly) to effect of another risk factor, i.e. confounder
- Other risk factor is an independant risk factor for the disease and is also associated with exposure
- Can result in an over- or underestimate of relationship between exposure and disease controlled for using statistical analysis (e.g. logistic regression used to adjust measure of association between exposure and disease for effects of other risk factors)

##### Dealing with confounding
Risk factors that could be confounders must be:
- Measured during study
- Controlled for using statistical analysis (e.g. logistic regression used to adjust measure of association between exposure and disease for effect of other risk factors)
- In review/interpretation of literature look for evidence these strategies have taken place

### 6. Measuring outcome of interest (disease)
- Definition of endpoint of interest
- Diagnostic criteria used
- Diagnostic techniques available
- Case ascertainment (all case or a selection,/biased)

### 7. Analysis and interpretation of relationship between exposure and disease
- Absolute risk
- Risk difference/excess risk/attributable risk
- Relative risk (or odds ratio)

## Objectives of epidemiology
- To determine rates of disease by person, place, time
    - Absolute risk (incidence, prevalence)
        - Incidence: number of new cases of disease occuring in specified time period divided by number of individuals at risk of developing disease at same time
        - Prevalence: total number of affected individuals in a population at a specified time period divided by number of people in population at same time
        - Incidence most relevant clinically
- To identify risk factors for disease
    - Relative risk (or odds ratio)
- To develop approaches for disease prevention
    - Attributable risk/attributable fraction

## To develop approaches for disease prevention: 
### Step 1: risk difference/excess risk/attributable risk (AR)
- AR: amount of disease incidence that can be attributed to a specific exposure
    - Difference in incidence of disease between exposed and nonexposed individuals (amount of risk can be prevented)
    - Incidence in nonexposed: background risk
    - AR = [risk among factor positives] - [risk among factor negatives]

### Step 2: attributable risk percent/attributable fraction (AF)/aetiologic fraction
- AF: proportion of disease incidence that can be attributed to specific exposure (among those who were exposed)
    - AR divided by incidence in exposed (which have been ascertained already) * 100%
    - AF = ([risk among risk factor positives]-[risk among risk factor negatives])/[risk among risk factor positives]

## Contingency (2x2) table
In most simple form, findings from epidemiologic studies that purport to investigate cause/risk can be summarized in a 2x2 (contingency) table showing disease status and exposure status

![](https://i.imgur.com/6gWTA38.png =350x)

### Measures of association from 2x2 table
Cohort study: outcome of measure is relative risk (or risk ratio or rate ratio)
- A cohort study begins with a healthy cohort, ascertains (measures) exposure(s) of interest and determines development of disease (outcome of interest) over time
- RR measures likelihood of getting disease if exposed relative to those who are unexposed
- RR: incidence in exposed/incidence in unexposed
- RR = (a/(a+b))/(c/(c+d))

#### Calculating relative risk
![](https://i.imgur.com/UgPLwGP.png =350x)

#### Interpreting relative risk
- Relative risk = 1.38 therefore risk of developing CHD is 1.38 times higher among smokers compared to nonsmokers
- i.e. risk of developing CHD is 38% higher among smokers compared to nonsmokers
![](https://i.imgur.com/s6leGnJ.png =350x)

## Case-control study
Outcome measure is estimate of relative risk or odds ratio (relative odds)
- A case control study begins with disease status and attempts to ascertain (estimate) prior exposure
    - Estimate of risk is odds ratio (OR) which is ratio of odds of exposure in cases (with disease) ratio of exposure in control (without disease)
- Odds ratio (OR): a ratio that compares odds of exposure for cases with odds of exposure for controls
- To get odds of exposure for controls:
    - Begin with proportions for both cases and controls exposed (i.e. probabilities of exposure)
    - Calculate odds for both cases and controls
- Odds of an event: ratio of probability that event will occur to probability event will not occur
    - Probability event will occur = P
    - Probability event will not occur = 1-P
    - Odds of event = P/1-P

![](https://i.imgur.com/xTqOQwB.png =350x)
![](https://i.imgur.com/FZLEuSz.png =350x)

### To identify risk factors for disease
- Relative risk (RR), odds ratio (OR)
    - RR: ratio of incidence of disease in exposed individuals to incidence of disease in nonexposed individuals (from a cohort/prospective study)
        - If RR>1, positive association
        - If RR<1, negative association
    - OR: ratio of odds that cases were exposed to odds that controls were exposed (from a case control/retrospective study) → is an estimate of RR
        - If OR>1, positive association
        - If OR<1, negative association

### 6. Interpreting study results
- No such thing as perfect study
- Recognizing limitations and strengths of any 1 study is critical
- Critiquing epidemiology literature:
    - Are they comparable in terms of demographic and other characteristics?
    - Are they representative of entire population?
    - Are measurement methods comparable (e.g. eligibility and classification criteria, risk factor assessment)
    - Could associations be biased/confounded by other factors not assessed?

### 7. Evaluation of role of chance
2 components:
1. Hypothesis testing, performing a test of statistical significance to determine probability that chance can explain observed results
2. Role of chance assessed by calculating p-value, if low, it's unlikely that observed results would've been caused by chance along but if high, it's more likely that observed results would've been caused by chance
3. Usual to choose p<0.05 (5%) as significance value for testing null hypothesis 
4. P-value reflects both size of sample and magnitude of effect, e.g. p-values can be above level of significance where sample is too small to detect significant effect
