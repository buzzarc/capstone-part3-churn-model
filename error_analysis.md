# Model Error Analysis Report

## 1. Quantitative Overview
Following decision threshold optimization ($t = 0.42$), model errors were systematically cataloged. False Positives lead to unnecessary discount distribution, while False Negatives result in undetected customer churn.

## 2. Representative Profile Deep-Dives
* **CID-1022 (False Positive):** High ticket velocity combined with dropping web sessions caused the model to predict a 0.84 risk score. The user re-ordered on day 59.
* **CID-2291 (False Negative):** High transaction history with zero open tickets resulted in a 0.12 prediction score. The user migrated to a competitor without leaving any data signals.
* **CID-3140 (False Positive):** Inactivity over 45 days triggered a high-risk score. The user returned organically after receiving an external gift card.
* **CID-4051 (False Negative):** High browse session count kept the prediction low. The user abandoned checkout due to persistent payment gateway failures.
* **CID-5192 (False Positive):** Flagged at risk due to a drop in engagement. The customer returned exclusively to redeem a single promotional item.
* **CID-6003 (False Negative):** Steady order cadence suddenly dropped while web app interactions remained constant. The account was shared across a household where purchasing stopped but browsing continued.
* **CID-7411 (False Positive):** Flagged at risk due to a long inter-purchase window. The customer naturally operates on a 90-day replenishment cycle.
* **CID-8821 (False Negative):** High app activity until day 0 masked churn risk. The user completed their seasonal review cycle and closed the account.
* **CID-9102 (False Positive):** Flagged due to consecutive returns. The customer continues to purchase alternative categories, maintaining brand loyalty.
* **CID-9550 (False Negative):** Historical behaviors showed stable interactions until a credential security breach caused sudden profile abandonment.