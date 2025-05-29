## **March Madness Predictor: 2025 Tournament Performance Summary**

### **Overall Accuracy & Scoring**

- **Reported Overall Accuracy**: **61.9% ****correct predictions (39 out of 63 games)
    
    ***An "average bracket score" is noted to be around 60-65%.***
    
- **Performance by Points** (Standard ESPN Per Correct Scoring: 10-20-40-80-160-320):
    - **Round of 64 (10pts/game):** 230 / 320 points (23 out of 32 correct)
    - **Round of 32 (20pts/game)**: 160 / 320 points (8 out of 16 correct)
    - **Sweet 16 (40pts/game):** 200 / 320 points (5 out of 8 correct)
    - **Elite Eight (80pts/game)**: 160 / 320 points (2 out of 4 correct)
    - **Final Four (160pts/game)**: 160 / 320 points (1 out of 2 correct semifinal winners)
    - **Championship (320pts/game)**: 0 / 320 points (0 out of 1 correct champion)
    - **Total Points**: 910 / 1920 points.
1. **Upset Prediction Analysis** (Note: the model defines upsets as any game with a seed margin ≥ 5)
    - **Correct Upsets Predicted** (Model correctly picked a lower seed to win): **2**
        - RD1: (12) Colorado St. over (5) Memphis (Margin: +8 pts for CSU)
        - RD1: (11) Drake over (6) Missouri (Margin: +10 pts for Drake)
    - **Incorrect Upsets Predicted** (Model picked a lower seed to win, but they lost): 9
        - RD1: (12) UC San Diego over (5) Michigan ***(Margin: -3 pts for UCSD)****
        - RD1: (13) Yale over (4) Texas A&M (Margin: -9 pts for Yale)
        - RD1: (12) Liberty over (5) Oregon (Margin: -29 pts for Liberty)
        - RD1: (11) VCU over (6) BYU (Margin: -9 pts for VCU)
        - RD1: (14) Troy over (3) Kentucky (Margin: -19 pts for Troy)
        - RD2: (7) UCLA over (2) Tennessee (Margin: -9 pts for UCLA)
        - RD2: (8) Gonzaga over (1) Houston ***(Margin: -5 pts for Gonzaga)****
        - RD2: (7) Saint Mary's over (2) Alabama (Margin: -14 pts for Saint Mary's)
        - RD3: (8) Gonzaga over (4) Purdue (Gonzaga did not make it to this round for this matchup)
    - **Accuracy When Calling an Upset**: (2 Correct / 11 total upsets predicted) = 2/11 = **18.2%**
    - **Missed Upsets** (Actual upset occurred, but model picked the higher-seeded favorite): 2
        - RD1: (5) Clemson lost to (12) McNeese ***(Margin: -2 pts for Clemson)****
        - RD2: (2) St. John's lost to (10) Arkansas (Margin: -9 pts for St. John's)
2. **Incorrect Predictions & Close Calls**
    - **Other Incorrect Predictions**: Not a potential upset game, just standard matchups:
        - RD1: (8) Louisville lost to (9) Creighton (Margin: -14 pts for Louisville)
        - RD1: (7) Marquette lost to (10) New Mexico (Margin: -9 pts for Marquette)
        - RD2: (3) Wisconsin lost to (6) BYU ***(Margin: -2 pts for Wisconsin)****
        - RD4: (2) Michigan St. lost to (1) Auburn (Actual margin: -6 pts for Michigan St.)
        - RD5 (Final Four): (1) Duke lost to (1) Houston ***(Margin: -3 pts for Duke)****
        - Champ: (1) Duke vs (1) Florida (Model predicted Duke, Duke did not make final; Florida won)
    - **Total Close Calls** (actual game margin ≤ 5 points):
        - From "Other": Wisconsin (-2 vs BYU), Duke (-3 in FF) = 2 games
        - From "Missed Upsets": McNeese (-2 vs Clemson) = 1 game
        - From "Wrong Upsets": UC San Diego (-3 vs Michigan), Gonzaga (-5 vs Houston in R2) = 2 games
        - **Total correct close calls**: **4 games**
        - **Total incorrect: 5 games**

### **Comparison to Public**

- **Model's ESPN Score**: 910 points.
- **Contextual Performance**:
    - A score of 910 points on ESPN's Tournament Challenge would typically place a bracket below the average percentile, likely in the 50-60th percentile range depending on the year's overall predictability (for context, 1010 points was previously noted as ~62nd percentile).
- **Champion Pick**: The model predicted Duke to win the championship. Duke was a popular public pick, chosen by 25% of brackets. The actual champion was Florida (picked by 21.3%), and Auburn was another popular choice (10.6%).

### **Observations & Takeaways**

- **Strengths**:
    - Achieved an accuracy of 61.9% (39/63 correct games), placing it within the typical range for an average public bracket.
    - Successfully predicted 2 upsets: (12) Colorado St. > (5) Memphis, and (11) Drake > (6) Missouri.
    - Performance was strong through the Sweet 16 (71.8% correct in R1, 50% in R2, 62.5% in S16).
    - Correctly identified two Final Four teams (Duke and Florida), one of which was the eventual champion (Florida) and the other (Duke) losing by 3 in the Final Four!
    - The champion pick (Duke) aligned with a significant portion of public sentiment.
- **Weaknesses**:
    - Low success rate (18.2%) when specifically predicting upsets, while missing some key actual upsets
- **Future Improvements**:
    - Further refinement of feature engineering, particularly for identifying robust upset potential versus high-risk, low-probability upset calls.
    - Explore confidence scoring for predictions to better distinguish high-certainty picks from borderline ones.
    - Consider adding features related to late-season form, key injuries, public sentiment, coaching experience in tournaments, or player-specific metrics if available.

### Final Notes

March Madness is inherently chaotic and difficult to predict, which is exactly what makes it such a captivating and exciting sporting event. With that said, that is also why it is so difficult for even the most robust models to capture defining features of the tournament. Upsets, momentum swings, and clutch performances can dramatically alter outcomes, making it one of the most thrilling yet statistically challenging events in sports. As a reference: the odds of filling out a perfect bracket are around 1 in 9.2 quintillion!

Despite this, the model achieved 61.9% accuracy, placing it as a very average bracket when compared with the rest of the public’s performance. It was strong in early round predictions, and even identified 2 Final Four teams correctly. However, it struggled in correctly identifying possible upsets, making several upset predictions that did not happen.

There are countless factors to consider when making each prediction, and no one can truly identify the more unlikely occurrences in the tournament: like when 14 seed Oakland’s Jack Gohlke, averaging 12.3 PPG shot 10-20 from 3 and dropped a whopping 32 points against a number 3 Kentucky team in 2024. However, there are some aspects that much of the public can consider that some models might not be able to spot. For example, in 2019, a small school that entered the tournament on an 11 game winning streak headed by a projected top 3 NBA pick, Ja Morant. This team did not blow anyone away in advanced metrics or strength of schedule, but the public had a strong sentiment on Murray State to beat Marquette that year because of momentum and star power. 

As a result, integrating additional contextual features, like late season momentum, injuries, star players, and coaching experience could provide more insight into making predictions. Additionally, implementing confidence levels could help separate between solid picks and long shot predictions that could go either way. 

Ultimately, the bracket’s performance strengthens the main idea of March Madness: that it will always be unpredictable and chaotic. This idea is exactly why modeling it is such a challenging, yet rewarding task.