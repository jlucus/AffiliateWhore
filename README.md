# Affiliate Whore:
## KPI's
1. Monthly Active Players (MAP): Tracks unique users who log in and engage monthly.
2. Net Gaming Revenue (NGR): Measures revenue retained after payouts.
3. Customer Acquisition Cost (CAC): Average expense to acquire a player.
4. Customer Lifetime Value (CLV): Total revenue generated by a player over their activity span.
5. Net Promoter Score (NPS): Measures player satisfaction and loyalty.
6. Retention Rate (RR): Percentage of players who return to the platform.
7. Deposit Frequency (DF): Tracks how often users fund their accounts.
8. Average Revenue Per User (ARPU): Average earnings per player.
9. Churn Rate (CHR): Percentage of players leaving the platform.
10. Conversion Rate (CVR): Visitors who become depositing players.
11. Bonus to Deposit Ratio (BDR): the ratio of bonus funds to player deposit ratio.

## Improve on the following system:
The current system only shows total deposits, date of last deposit, and the total commissions earned. However, we need to identify clear metrics that account for the possibility of players winning large amounts without hurting the score so long as the players are in profit.
### Current Panel Sample:
Code: BetOnGamba
Rank: BRONZE 3 icon
Name: hoodmood
Wagered: $14930.16
Date Registered: 07/01/2024, 02:31 PM
Commission: $6.85
Shared: $1.03
Total Deposits: $1187.23
Recent Deposit: 12/26/2024

## Sample 30 Day Promotions Available:
1. Leaderboards - Free-for-all style race where the most played in a given time period will take the prize pool.
2. Challenges - Wager or betsize incentivized gameplay that attempts to reach a given target multiplier based on a players minimum bet size.
3. Drops - Free coupons players can redeem provided they meet the requirements.
4. Streams - A way to engage with players in a live stream enviorment, which can dramatically boost engagements. We should only care about the total amount of airtime for any stream, regardless of any other factors.

This project implements a scoring system for affiliate campaigns based on various Key Performance Indicators (KPIs). The system calculates scores for each player and provides a summary report that is easy to understand.

## Features

- Calculate scores for the following KPIs:
  - Monthly Active Players (MAP)
  - Deposit Frequency (DF)
  - Bonus to Deposit Ratio (BDR)
  - Average Bet Size (ABS)
  - Customer Acquisition Cost (CAC)
  - Long Term Value (LTV)
  - Risky Behaviors (RB)
  - Engagement
  - Prompt for player data input
  - Display a summary report of the scores

## Usage: 
1. Clone the repository or copy the code into your local environment.
2. Run the script to input player data and calculate scores.

### Example Usage
```python
data = []
num_players = int(input("Enter number of players: "))
for _ in range(num_players):
    data.append(prompt_player_data())

scores, total_score = calculate_scores(data)
update_ui(scores, total_score)

Functions
calculate_map(data): Calculates the Monthly Active Players score.
calculate_df(data): Calculates the Deposit Frequency score.
calculate_bdr(data): Calculates the Bonus to Deposit Ratio score.
calculate_abs(data): Calculates the Average Bet Size score.
calculate_cac(data): Calculates the Customer Acquisition Cost score.
calculate_ltv(data): Calculates the Long Term Value score.
calculate_rb(data): Calculates the Risky Behaviors score.
calculate_engagement(data): Calculates the Engagement score.
calculate_scores(data): Aggregates all KPI scores and calculates the total score.
prompt_player_data(): Prompts the user to input player data.
update_ui(scores, total_score): Updates the UI to display the scores and total score.
Sample Data
You can use the following sample data to test the system:
data = [
    {
        'name': 'hoodmood',
        'id': 1,
        'last_login_date': '2024-12-26',
        'deposit_count': 5,
        'bonus_amount': 100,
        'deposit_amount': 1187.23,
        'total_wagered': 14930.16,
        'bet_count': 100,
        'acquisition_cost': 50,
        'total_revenue': 200,
        'risky_behavior': False,
        'last_deposit_date': '2024-12-26',
        'engagement_score': 25
    },
    # Add more sample players as needed
]
```

```python
def display_kpi_summary(data):
    scores, total_score = calculate_scores(data)
    
    print("Affiliate KPI Summary Report")
    print("============================")
    print(f"Total Score: {total_score}")
    print()
    
    for player in data:
        print(f"Player: {player['name']}")
        print(f"  - Monthly Active Players: {scores['monthly_active_players']}")
        print(f"  - Deposit Frequency: {scores['deposit_frequency']}")
        print(f"  - Bonus to Deposit Ratio: {scores['bonus_to_deposit_ratio']}")
        print(f"  - Average Bet Size: {scores['average_bet_size']}")
        print(f"  - Customer Acquisition Cost: {scores['customer_acquisition_cost']}")
        print(f"  - Long Term Value: {scores['long_term_value']}")
        print(f"  - Risky Behaviors: {scores['risky_behaviors']}")
        print()
```

#### License
This project is licensed under the MIT License.

