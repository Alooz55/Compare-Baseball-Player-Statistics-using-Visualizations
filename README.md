# ⚾ Baseball Statcast Power Analysis (2015-2017)

An advanced statistical analysis and data visualization project utilizing MLB Statcast tracking data to evaluate, compare, and profile the aerodynamic and spatial hitting mechanics of elite sluggers Aaron Judge and Giancarlo Stanton.

---

## 🛠️ Tech Stack & Skills Developed
* **Data Wrangling & Analytics:** Python, Pandas, NumPy.
* **Statistical Visualization:** Seaborn, Matplotlib (Distribution comparisons via Boxplots and Kernel Density Estimate (KDE) plots).
* **Domain Applications:** Statistical modeling of sports telemetry data (Sabermetrics).

---

## 📊 Project Report: Comparing Elite Baseball Power Profiles

### Introduction: The 2017 Home Run Race
In the summer of 2017, Major League Baseball witnessed an extraordinary offensive showcase dominated by two physically imposing teammates: Aaron Judge and Giancarlo Stanton. This project explores the high-resolution tracking data captured by MLB's Statcast system between 2015 and 2017 to uncover the distinct mechanics behind their historic home run productions.

The year 2017 stood out as a historic milestone for both players, as they comfortably led the entire league in home runs:
* **Giancarlo Stanton** captured the peak of the league, blasting an astonishing **59 home runs** to lead all hitters.
* **Aaron Judge** followed closely in a spectacular rookie campaign, launching **52 home runs**.

To put their dominance into perspective, the player trailing in third place across the entire league managed "only" 45 home runs—leaving Stanton and Judge in a league of their own. While both athletes achieved elite outcomes, the paths their baseballs traveled were fundamentally different. By looking at these core frequencies, we set the stage to analyze the hidden distributions of pitch speeds, launch angles, and spatial strike zones that defined this modern hitting rivalry.

---

### Section 1: Home Run Pitch Velocity Analysis
While absolute home run totals tell us how many times the ball cleared the fence, exploring the velocity of the incoming pitches tells us how these athletes leverage their reaction times. By isolating the release speed (`release_speed`) of every home run ball, we can map out each hitter's comfort zone against major league pitching.

#### Insights from the Distribution:
* **The High-Velocity Punisher (Aaron Judge):** The data reveals that Judge consistently thrives against higher internal velocities. His distribution, including a higher median marker, shows that he routinely turns fastballs and high-velocity pitches into deep scoring plays.
* **The Off-Speed Adjuster (Giancarlo Stanton):** While Stanton also punishes high heat, his overall distribution stretches lower, indicating a remarkable ability to stay back, adjust to off-speed pitches or breaking balls, and still generate enough leverage to drive them out of the park.

---

### Section 2: Bivariate Distribution of Launch Metrics
To understand the ball flight mechanics behind each player's home runs, we map `launch_angle` against `launch_speed`. This probabilistic visualization highlights the high-density regions—the "sweet spots"—where home run production is most concentrated. 

#### Structural Flight Comparisons:
* **Giancarlo Stanton (The Line-Drive Enforcer):** Displays a highly concentrated density centered at a lower launch angle but a significantly higher launch speed. His home run profile is characterized by low-trajectory, high-velocity line drives. His hits rely less on aerodynamic carry and more on pure exit velocity to clear the outfield fences.
* **Aaron Judge (The True Fly-Ball Threat):** Exhibits a broader, slightly higher launch angle distribution combined with a lower average launch speed compared to Stanton. His profile favors high-arching fly balls with optimal carry and extensive hang time.

---

### Section 3: Spatial Heatmap Analysis of Home Run Strike Zones
This analysis maps the physical coordinate distribution of home runs across the 3x3 strike zone matrix. Pitches outside the standard strike zone boundaries (zones 11, 12, 13, and 14) are excluded to ensure focus on standard strike encounters. 

#### Spatial Density Observations:
* **Aaron Judge:** Demonstrates balanced coverage across the middle and lower sectors of the strike zone, with his absolute peak concentration (14 home runs) positioned dead-center.
* **Giancarlo Stanton:** Concentrates massive offensive production heavily toward the inside and lower-middle sections of the plate, racking up exceptional frequencies (23 and 19 home runs) in those specific quadrants. This demonstrates a distinct mechanical preference for low-and-in pitches.

---

### 🎯 The Analytical Verdict
Having analyzed the spatial configurations of the strike zone, pitch velocities, and aerodynamic launch metrics, we can synthesize our findings into a definitive structural profile for both elite sluggers.

While Stanton dominates the sheer velocity metrics and exhibits hyper-dense specialization in low-and-inside pitches, **Aaron Judge offers a more fundamentally balanced and high-carry home run profile**. Judge's ability to consistently find the optimal launch angle across a wider spatial distribution of the strike zone yields a more stable, versatile, and high-carry fly-ball profile—making his hitting mechanics the structurally preferred model for sustained home run production.

---

## 📂 Project Structure
* `notebook.ipynb` - Core Jupyter Notebook containing data pipeline, statistical modeling, and visualization scripts.
* `judge.csv` & `stanton.csv` - Comprehensive clean Statcast historical datasets.
* `judge_wide.jpg` & `zone.png` - Visual assets integrated into the analytical reporting.
