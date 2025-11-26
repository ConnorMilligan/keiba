I have access to a dataset using [this](https://github.com/new-village/KeibaScraper) with the following parameters:

# Data

## Race
- Race ID
- Race number
- Race name
- Race date
- Race time
- Type (turf/dirt)
- Length (metres)
- Length class (Long, Intermediate, Sprint)
- Handed (右, 左)
- Weather (曇, 晴)
- Condition (良, 稍, etc)
- Place (中山, 札幌, 阪神)
- Course (中山芝1200)
- Round
- Days
- Head Count
- Max Prize
### Entry
#### Horse
- Race ID
- Rank
- Bracket
- Horse Number
- Horse ID
- Horse Name
- Gender
- Age
- Burden
- Jockey ID
- Jockey Name
- Rap Time
- Diff Time
- Passage Rank
- Last 3f
- Weight (kg)
- Weight Diff
- Trainer ID
- Trainer Name
- Prize
- ID  (This horse in this race)
#### Odds
- Race ID
- Horse Number
- Win (93.0, 115.0, etc)
- Show Min (12.7, etc)
- Show Max (23.7, etc)
- ID (This horse in this race)
## Horse
- CURRENTLY BROKEN

# Goals
Predict outcomes of horse races using historical data. A program should be able to maximize prediction accuracy based on given information against historical outcomes and attempt to apply that same prediction strategy to as of yet undecided races.
## Predicted significant factors
- Race distance
- Track type
- Lineage
- Trainer
- Jockey
- Previous performance
# Potential Issues
- The current keibascraper doesn't pull data about individual horses, this should be fixed and likely expanded to include past performance and course aptitudes if any.
- Time window could potentially be a factor, as the racing careers of horses that aren't producing offspring could be negligent. Detailed information about past races could spoil data given potential for development in things such as training methods across trainers.
- The scraping script does impose a load on the actual netkeiba website, which could cause issues when attempting to pull months or years of information at a time. This should be minimized to reduce load on the servers and reduce risk of IP bans.

# Steps to take
- Fix the keibascraper horse data scraping and add race history.
- (Potentially add Jockey data as well)
- Build a structured dataset that a model can be trained off of.
- Model training and testing.
- Find ways to expand the dataset with new race data.
