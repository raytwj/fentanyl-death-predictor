![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)
# DSI-23: Capstone Project

## Predicting Fentanyl Presence In Accidental Drug Overdose Deaths In Connecticut, USA

Ray Tan

### Keywords

fentanyl, opioid, user, victim, overdose, death, crisis, connecticut

### Background

Fentanyl is a synthetic opioid analgesic used to treat severe chronic pain or severe pain following surgery [[1]](https://www.dea.gov/resources/facts-about-fentanyl). With a potency 100 times more than morphine and 50 times more than heroin, fentanyl is highly potent and poses a serious health threat [[2]](https://www.tandfonline.com/doi/pdf/10.1080/10410236.2020.1748820). It is prescribed by doctors, commonly in the form of transdermal patches or sublingual tablets, for approved indications [[3]](https://www.nbcconnecticut.com/news/local/a-perfect-storm-for-everybody-struggling-ct-saw-1374-deadly-drug-overdoses-in-2020/2476648/). However, fentanyl can be misused and abused by users who extract it from the patches and administer it via intravenous injection [[3]](https://www.nbcconnecticut.com/news/local/a-perfect-storm-for-everybody-struggling-ct-saw-1374-deadly-drug-overdoses-in-2020/2476648/). The form of fentanyl that is most often associated with overdoses is illegally manufactured in underground laboratories and sold on the illicit drug market as powders, eye drops, nasal sprays, and increasingly, as pills made to look like legitimate prescription painkillers [[3]](https://www.nbcconnecticut.com/news/local/a-perfect-storm-for-everybody-struggling-ct-saw-1374-deadly-drug-overdoses-in-2020/2476648/). Because there is no official oversight or quality control, these counterfeit pills often contain lethal doses of fentanyl, with none of the promised drug [[1]](https://www.dea.gov/resources/facts-about-fentanyl). Toxicological data shows that fentanyl use is inextricably linked with polydrug use: Fentanyl is often mixed with other drugs such as heroin, cocaine, and methamphetamine – with or without the user’s knowledge – to increase its euphoric effects; but, this also increases the likelihood of a fatal interaction [[1]](https://www.dea.gov/resources/facts-about-fentanyl)[[2]](https://www.tandfonline.com/doi/pdf/10.1080/10410236.2020.1748820)[[3]](https://www.nbcconnecticut.com/news/local/a-perfect-storm-for-everybody-struggling-ct-saw-1374-deadly-drug-overdoses-in-2020/2476648/).

2013 marks the year of emergence of fentanyl in the illicit drug market [[4]](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(21)00080-3/fulltext). Latest evidence points to a disturbing increase in the illicit use of fentanyl: Fentanyl-related overdose deaths have skyrocketed in recent years and have become a huge contributor to the current overdose death crisis in the USA [[2]](https://www.tandfonline.com/doi/pdf/10.1080/10410236.2020.1748820). Connecticut has surpassed the national death rate for drug overdoses and fentanyl-related overdoses since 2013 [[5]](https://overdose.trendct.org/story/main)[[6]](https://www.livestories.com/statistics/connecticut/fentanyl-deaths-mortality). 2020 alone has been a record-breaking year for drug overdose deaths and fentanyl-related overdose deaths in Connecticut [[3]](https://www.nbcconnecticut.com/news/local/a-perfect-storm-for-everybody-struggling-ct-saw-1374-deadly-drug-overdoses-in-2020/2476648/). In 2013, there were 490 total overdose deaths in Connecticut, of which 38 (or 7.7%) involved fentanyl [[7]](https://data.ct.gov/Health-and-Human-Services/Accidental-Drug-Related-Deaths-2012-2020/rybz-nyjw). In 2020, there were 1366 total overdose deaths in Connecticut, of which 1152 (or 84.3%) involved fentanyl [[7]](https://data.ct.gov/Health-and-Human-Services/Accidental-Drug-Related-Deaths-2012-2020/rybz-nyjw). The increase in the number of fentanyl deaths has outpaced the increase in the number of total deaths every year since 2013 [[7]](https://data.ct.gov/Health-and-Human-Services/Accidental-Drug-Related-Deaths-2012-2020/rybz-nyjw).

### Problem Statement

With the accidental drug overdose death problem expected to continue to worsen in the coming year and fentanyl being the dominant drug seen in overdose deaths today, there is an urgent need for effective harm-reduction strategies to tackle the escalating fentanyl crisis and stop deaths from occurring. As a start, it would be beneficial to know what are some of the main factors or drivers causing the surge in fentanyl-related overdose deaths in recent years.

### Target Audience

This project would be targeted at Connecticut state officials. Its aim is to help them better understand the circumstances surrounding fentanyl-related overdose deaths and better recognise the top features that are most important in explaining fentanyl presence in accidental drug overdose deaths.

### Objectives

To achieve this, several classification models will be developed. Their individual performance will be evaluated based on two metrics: Accuracy and Area Under Curve. The final chosen model will be the best-performing hyperparameter-tuned model that achieves an accuracy closest to 1 and an area under curve closest to 1. The top features that are most important in explaining fentanyl presence in accidental drug overdose deaths will be identified from the model. This will be helpful for guiding Connecticut state officials on the allocation of scarce resources to key areas that influence fentanyl presence in accidental drug overdose deaths and assisting them in working towards preventing such deaths from happening.

### Data Sources

The following datasets were used:

* [`accidental_drug_related_deaths_2012_2020.csv`](../data/accidental_drug_related_deaths_2012_2020.csv): Accidental Drug-Related Deaths In Connecticut (2012-2020) Dataset

> This dataset contains a listing of each accidental death associated with drug overdose in Connecticut from 2012 to 2020. It has 7,679 rows and 42 columns. It holds information on each victim's age, sex, race, county of death, city of death, place of death, cause of death, other significant conditions, overdosed drugs, etc. It was obtained from the Connecticut state government website over [here](https://data.ct.gov/Health-and-Human-Services/Accidental-Drug-Related-Deaths-2012-2020/rybz-nyjw). A separate detailed description of the variables in the dataset can be found [here](https://code.datasciencedojo.com/khanh_quang/datasets/tree/master/Accidental%20Drug%20Related%20Deaths%20in%20Connecticut,%20US).

<details>

<summary>(click here to show a brief description of the dataset)</summary>
    
**Accidental Drug Related Deaths 2012-2020**

A listing of each accidental death associated with drug overdose in Connecticut from 2012 to 2020.

A "Y" value under the different substance columns indicates that particular substance was detected. Data are derived from an investigation by the Office of the Chief Medical Examiner which includes the toxicity report, death certificate, as well as a scene investigation.

The “Morphine (Not Heroin)” values are related to the differences between how Morphine and Heroin are metabolized and therefor detected in the toxicity results. Heroin metabolizes to 6-MAM which then metabolizes to morphine. 6-MAM is unique to heroin, and has a short half-life (as does heroin itself). Thus, in some heroin deaths, the toxicity results will not indicate whether the morphine is from heroin or prescription morphine. In these cases the Medical Examiner may be able to determine the cause based on the scene investigation (such as finding heroin needles). If they find prescription morphine at the scene it is certified as “Morphine (not heroin).” Therefor, the Cause of Death may indicate Morphine, but the Heroin or Morphine (Not Heroin) may not be indicated.

</details><br>

* [`connecticut.csv`](../data/connecticut.csv): Cities And Counties In Connecticut (2021) Dataset

> This dataset contains a listing of the cities and counties in Connecticut in 2021. It was obtained from the Connecticut state library website over [here](https://ctstatelibrary.org/cttowns/counties).

### Data Dictionary

A list of the clean datasets is given below:

* [`accidental_drug_related_deaths_2012_2020_clean.csv`](../data/accidental_drug_related_deaths_2012_2020_clean.csv): Accidental Drug-Related Deaths In Connecticut (2012-2020) Clean Dataset

A description of the variables in the clean datasets is given below:

* Accidental Drug-Related Deaths In Connecticut (2012-2020) Clean Dataset

| Variable | Type | Description |
|:---|:---|:---|
| Date | datetime | Date of death in YYYY-MM-DD |
| Age | integer | Age of victim |
| Sex | object | Sex of victim |
| Race | object | Race of victim |
| Death_County | object | County of death |
| Death_City | object | City of death |
| Death_City_Geo | object | GPS coordinate of death |
| Death_Place | object | Place of death |
| Injury_Place | object | Place of injury (that caused death) |
| Fentanyl | object | Fentanyl found in victim |
| Any_Fentanyl_Analogue | object | Any fentanyl analogue found in victim |
| Buprenorphine | object | Buprenorphine found in victim |
| Methadone | object | Methadone found in victim |
| Oxymorphone | object | Oxymorphone found in victim |
| Hydromorphone | object | Hydromorphone found in victim |
| Oxycodone | object | Oxycodone found in victim |
| Hydrocodone | object | Hydrocodone found in victim |
| Heroin | object | Heroin found in victim |
| Morphine_Not_Heroin | object | Morphine (not heroin) found in victim |
| Tramadol | object | Tramadol found in victim |
| Codeine | object | Codeine found in victim |
| Ethanol | object | Ethanol found in victim |
| Cocaine | object | Cocaine found in victim |
| Xylazine | object | Xylazine found in victim |
| Phencyclidine | object | Phencyclidine found in victim |
| Any_Benzodiazepine | object | Any benzodiazepine found in victim |
| Any_Amphetamine | object | Any amphetamine found in victim |
| Other_Drug | object | Other drug (not stated above) found in victim |
| Any_Opioid | object | Any opioid found in victim |
| Other_Opioid | object | Other opioid (not stated above) found in victim |
| Covid_Pandemic | object | Death occurred on or after declaration of Covid-19 as a pandemic on 11-03-2020 |
| Num_Drugs | integer | Number of named drugs found in victim |
| Num_Conditions | integer | Number of significant conditions that victim has |

### Results & Discussion

The final chosen model, a Custom Light Gradient Boosting Machine Classifier, has done well and was able to achieve decent performance scores that surpass that of the baseline null model. To further improve the predictive ability of the final chosen model and achieve even better performance scores, information on the following features should ideally be obtained:

Socioeconomic background indicators

- What is the highest education level obtained by the individual?
- What is the yearly income of the individual?
- Is the individual living alone?
- Is the individual under foster care?

Drug use history indicators

- How long has the individual been using drugs?
- Has the individual been into drug rehabilitation before?
- Has the individual been prescribed fentanyl before?
- Has the individual been prescribed other opioid painkillers before?

### Recommendations

A few recommendations on harm-reduction strategies can be made:

- Initiate education campaigns in schools and colleges to teach young kids and adults about the dangers of using drugs on the illicit drug market, especially on the overdose risks and widespread availability of illegally manufactured fentanyl
- Pass stricter laws that deal out harsher penalties to individuals involved in the purchase and supply of several illicit drugs, given the high likelihood of finding illegally manufactured fentanyl laced into the supplies of other illicit drugs
- Work with doctors to promote the appropriate use of opioids for pain to reduce irrational or inappropriate opioid prescribing and dispensing, with added measures for higher-risk opioids such as fentanyl that would involve statewide monitoring of all prescribing and dispensing activities

Investing in harm-reduction strategies does not just solve one problem but multiple problems at once:

- Outbreaks of diseases such as hepatitis and HIV/AIDS are closely connected to drug use and can be prevented by reducing drug use in the population
- Decreasing the number of deaths from accidental drug overdose would have positive ripple effects on the other fronts of the war against drugs such as drug manufacturing and drug trafficking

### Conclusion

The fentanyl crisis is a complex perennial problem that presents a major challenge for public health policy. It requires a multi-pronged approach and a concerted effort from individuals, communities, and governments to overcome successfully.

The final chosen model, a Custom Light Gradient Boosting Machine Classifier, was able to accurately predict 79.08% of accidental drug overdose deaths to have either no fentanyl present or fentanyl present. It has found the three most important features that predicted fentanyl presence to be age, number of drugs, and heroin presence. This information may be used to lead and direct the implementation of harm-reduction strategies aimed at reducing fentanyl-related overdose deaths.

Next steps for this project would involve extending it to help predict fentanyl presence in overdose deaths in other states of the USA. It can also be adapted to investigate the presence of other drugs such as heroin and cocaine that are commonly implicated in overdose deaths.

In the context of Southeast Asia, while countries such as Singapore are not embroiled in a drug crisis, countries such as Myanmar, Laos, and Thailand, whose borders form the infamous Golden Triangle, have served as the hub for illicit drug manufacturing and trafficking for many decades and could benefit from efforts targeted at tackling the problem. Formerly one of the world’s largest opium-producing areas, operations in the region have since shifted from opium poppy farming to synthetic drug production, and today it is one of the world’s leading areas for the production of methamphetamine. Myanmar, in particular, is facing a public health disaster as more and more of its young children are getting addicted to methamphetamine.

Future plans for this project could involve applying it to Myanmar as a starting point for understanding what are some of the main factors or drivers causing the surge in addiction to methamphetamine in recent years.

### References

[1] https://www.dea.gov/resources/facts-about-fentanyl<br>
[2] https://www.tandfonline.com/doi/pdf/10.1080/10410236.2020.1748820<br>
[3] https://www.nbcconnecticut.com/news/local/a-perfect-storm-for-everybody-struggling-ct-saw-1374-deadly-drug-overdoses-in-2020/2476648/<br>
[4] https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(21)00080-3/fulltext<br>
[5] https://overdose.trendct.org/story/main<br>
[6] https://www.livestories.com/statistics/connecticut/fentanyl-deaths-mortality<br>
[7] https://data.ct.gov/Health-and-Human-Services/Accidental-Drug-Related-Deaths-2012-2020/rybz-nyjw<br>