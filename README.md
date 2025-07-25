# Andela’s COVID-19 Impact Estimator

_A simplified infection/impact estimator originally built for the 2020 **#BuildForSDG** assessment by Andela & Facebook Developer Circles. Adapted, extended, and maintained by **Adeyemi Aina**._

---

## 1. Why this project matters

During the early COVID-19 outbreak, leaders needed quick, comprehensible numbers: How many people might get infected? How many will need hospital beds, ICU care, or ventilators? What’s the likely economic hit on households? This estimator provides a transparent, open-source way to answer those questions rapidly, using a minimal input set and reproducible logic.

In line with the UN Sustainable Development Goals (SDGs), the tool empowers public institutions, educators, and NGOs to plan resources and mitigate impact—especially where data science capacity is limited.

---

## 2. What the estimator does (at a glance)

- **Accepts a concise JSON payload** describing population, reported cases, time horizon, health-system capacity, and income indicators.  
- **Computes two scenarios** (“impact” and “severeImpact”) to bracket uncertainty.  
- **Returns key projections**: infections over time, severe cases, ICU/ventilator needs, hospital bed gaps, and economic loss (“dollars in flight”).  
- **Is framework-agnostic** (JavaScript core logic; easy to port to Python/Go/Rust).  
- **Is auditable and testable**: every step is documented, unit-tested, and reproducible.

---

## 3. Inputs

```json
{
  "region": {
    "name": "Africa",
    "avgAge": 19.7,
    "avgDailyIncomeInUSD": 4,
    "avgDailyIncomePopulation": 0.73
  },
  "periodType": "days",          // days | weeks | months
  "timeToElapse": 58,
  "reportedCases": 674,
  "population": 66622705,
  "totalHospitalBeds": 1380614
}

{
  "data": { ...inputPayload },
  "impact": {
    "currentlyInfected": 3370,
    "infectionsByRequestedTime": 106146523,
    "severeCasesByRequestedTime": 15921978,
    "hospitalBedsByRequestedTime": -1300000,
    "casesForICUByRequestedTime": 5307326,
    "casesForVentilatorsByRequestedTime": 2122930,
    "dollarsInFlight": 281984049
  },
  "severeImpact": {
    "currentlyInfected": 33700,
    "infectionsByRequestedTime": 1061465230,
    ...
  }
}


# #BuildForSDG Cohort-1 Python Assessment

> Build an overly simplified COVID-19 infection impact estimator

This is an eligibility assessment for the 2020 [#BuildforSDG](https://buildforsdg.andela.com/) program

The assessment empowers me to **attempt** helping society and leaders prepare for the **real big problem** of COVID-19, which is **its impact on lives, health systems, supply chains, and the economy**: 
> 1.  Too many patients, not enough hospitals and beds. A serious shortage of ventilators, masks and other PPE - if *we don’t practice social distancing*.
> 2.  Job losses or freezes, low cash flow and low production (even for essentials like food). These and more from too many people being sick, a sizable number dying (including some of the best people in many fields), and many others affected by the impact of losing loved ones or a world operating in slow motion

## How To Proceed

### Project Setup & Submission Process

> Go to [this Google Drive](https://drive.google.com/drive/u/0/folders/132af5VHpYX5LDTzqQETThXpDpw6Q6jRv) for guides on [how to setup your project](https://drive.google.com/file/d/1izTv3RdKwJf2V0RsarRc2ULDemKEAC16/view), take the assessment in one of the supported programming languages (Javascript, Python, or PHP), and how to submit your work. Make sure you read the instructions carefully, because missing a step might cost you in the long run.
---
