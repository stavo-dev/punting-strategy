# punting-strategy

### What is Category Punting

"Punting a category means that a fantasy manager intentionally chooses to not focus on a specific category during their draft. The reasoning behind this is you can strengthen your team in the categories that you are not punting."

Source: https://support.fantasypros.com/hc/en-us/articles/1260803684989-What-does-it-mean-to-punt-a-category-and-how-does-it-affect-my-pick-recommendations-in-Draft-Wizard-MLB-#:~:text=Punting%20a%20category%20means%20that,that%20you%20are%20not%20punting

### Punting Strategy Tool

This new tool affords the knowledge needed to optimize Fantasy Basbeall draft strategy and settings.

### How it works

The Punting Strategy Tool ingests:

* League Settings,
* Player Projections,
* Projected Draft Values, and
* outputs all category combinations with a Punting Strategy Score.

### Logic

The needed logic expands on the Fantasy Baseball Salary Cap Calculator: https://draftwizard.fantasypros.com/editor/createFromProjections.jsp?auction=Y&sport=mlb

* Punting Strategy (PS) is created from all category combinations.
* Projected Draft Value (PDV) is subtracted from Player Value (PV) to arrive at Player Alpha (PA).
* Player Alpha (PA) is summed by Punting Strategy (PS) to create the Punting Strategy Score (PSS).

### Result

    ---------------------------------------------
    ID          Punting Strategy            Score
    ---------------------------------------------
    13      - HR RBI SB ---         646.8
    4       R HR RBI -- ---         628.7
    10      R -- RBI -- AVG         591.8
    11      R -- --- SB AVG         573.2
    14	    - HR RBI -- AVG         556.5
    7	    R HR --- -- AVG         508.4
    3	    R HR RBI -- AVG         497.1
    6	    R HR --- SB ---         475.8
    16	    - -- RBI SB AVG         464.8
    2	    R HR RBI SB ---         463.5
    8	    R -- RBI SB AVG         459.8
    9	    R -- RBI SB ---         423.4
    12	    - HR RBI SB AVG         395.9
    15	    - HR --- SB AVG         380.0
    1	    R HR RBI SB AVG         379.9
    5	    R HR --- SB AVG         379.1
    ---------------------------------------------
    ---------------------------------------------

### Demo

I created this basic demo to test my logic using MySQL. This demo calculated for:

* hitters,
* 10 teams,
* 8 positions, and
* limited players to one eligible position.

The MySQL dump is available here: https://github.com/stavo-dev/punting-strategy/blob/main/db_punting_strategy.sql

I’m happy to provide additional MySQL code and formulas upon request.
