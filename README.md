# VCT Match Predictor

A prediction system for VALORANT eSports matches, more specifically, Americas Stage 1 of the VALORANT Champions Tour 2025.

## Dataset
A custom dataset was used which contains key statistics for every match from Americas Kickoff and Stage 1 so far, namely: Pistol Rounds Won, First Kills, KAST%, Clutch%, Eco Rounds Won, Semi-Eco Rounds Won, Half-Buy Rounds Won, Full-Buy Rounds Won, and XvY Conversions (eg: 5v1, 2v4, etc.) for each team.

The data was gathered using rib.gg, a site which contains stats and analytics for all VALORANT eSports teams and matches. However, due to the lack of a public API for the mentioned statistics, the data was ***scraped using Selenium*** — an open-source tool for browser automation

## Methodology
A ***Random Forest Classifier*** is used to predict the result of a match based on the two teams' average stats over the season. 
At the end of each game week, match results are scraped to keep the dataset up to date, and predictions for the next week's matches are made. Additionally, the predictions are also compared to Stake.com betting odds purely as a means for comparison. 


#### ⚠️ DISCLAIMER: ⚠️
***This model is not meant to be used as betting advice. Stake.com odds were used purely for comparison purposes.*  
*I do not endorse or promote gambling, and I am not responsible for any losses resulting from the use or misinterpretation of this project.***


## Results
The results are being updated as the matches go on. For results of each week individually, refer to [the Results page](Results.md).

Latest update: 21st April 2024

<div align="center">
<table>
  <thead>
    <tr>
      <th></th>
      <th>Stake Prediction</th>
      <th>Model Prediction</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Overall Accuracy</strong></td>
      <td align="center"><strong>22/30 (73.33%)</strong></td>
      <td align="center"><strong>24/30 (80%)</strong></td>
    </tr>
  </tbody>
</table>
</div>
