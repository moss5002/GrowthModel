# Echo — oral presentation preparation

Each slide's speaker notes contain a suggested script. The planned durations total eight minutes: 40, 45, 45, 55, 55, 45, 60, 55, 45 and 35 seconds. Divide the slides among you, then rehearse with a timer.

## Ideas you should be able to explain

- **Activation**: twenty cumulative listening minutes during the signup week. This is a convention for initial usage, not evidence of retention. Comparisons with ten minutes, two sessions and their combination do not show better W4 retention.
- **Cohort**: people who signed up during the same week. W4 is the fourth week after their signup week. Each user counts once in their cohort's retention rate.
- **Adjusted W4 retention**: channels are compared using the same distribution of signup months and platforms. This reduces some differences in composition without proving a causal channel effect.
- **North Star**: total listening minutes per week. This measures audio usage. Active users and retention accompany it so that a few heavy listeners cannot hide user losses.
- **The claimed +30%**: our calendar reconstruction finds +31.5% total sessions. The team's exact method is unknown. Over twelve comparable weeks per assigned user, sessions rise 8.71%, but listening falls 5.25% and W12 retention falls 11.71 percentage points.
- **Two months or twelve weeks?** Experiment signups run from 15 January to 15 March 2026. Data through June then provides twelve complete follow-up weeks for every participant.
- **CAC and revenue**: paid signups from January to June 2025 have about €2.61 CAC versus €1.62 ad revenue at 52 weeks. Mean payback is not reached at this horizon. This gives neither lifetime LTV nor a certain payback date.
- **Model**: next active users = existing active users × continuation rate + new signups, by channel. Paid depends on budget and CAC. Other channels follow their past signups. Any paid effect on the other channels is unmeasured.
- **Why simple?** Internal validation gives 1.57% listening error for the simple model, versus 2.54% for the tested age bands. Final backtest error is 3.85%. The model underestimates the end of the period.
- **Scenarios**: all keep normal notifications and a €1,630 monthly budget. CAC and churn probability vary by ±5%. These are assumptions, not achieved gains or confidence intervals.

## Our notebook and the course simulator

Both use the same growth logic: retain existing users, add new users, then estimate revenue. The supplied Excel file illustrates this with monthly inputs. Our calculations run in the notebook, using Echo's historical data and explicit forecast assumptions.

| Aspect | Course simulator | Our notebook |
| --- | --- | --- |
| Time and channels | Monthly model with overall inputs | Weekly cohorts, with parameters by acquisition channel |
| Acquisition | Paid budget / CAC and a referral assumption | Paid budget / CAC; historical signup trends for organic and podcast |
| Revenue | ARPU and gross margin assumptions | Ad impressions and the supplied approximate €9 CPM; no invented margin |
| Validation | Teaching examples and scenario comparisons | Historical calibration, internal validation and a held-out 2025 backtest |

The notebook also contains data cleaning, the funnel and the notification experiment. We did not fill in the Excel simulator. We adapted its growth principles to Echo. Code cells are collapsed for reading; expand a cell to inspect or edit its code. All calculations and outputs are retained.

## Using the model for the jury's question

Before the defense, open `G06_Echo_model.ipynb` from the project root and run all cells with the dependencies in `requirements.txt`. Check that charts appear. Keep an unchanged copy to recover the submitted results.

The scenario section has three settings:

| Setting | Submitted value | Purpose |
| --- | --- | --- |
| `BUDGET_PAID_MONTHLY` | 1630 | Monthly paid budget in euros |
| `SCENARIO_CHANGE` | 0.05 | Relative change in CAC and churn |
| `FORECAST_WEEKS` | 26 | Number of forecast weeks |

Change a setting, then rerun the scenario parameter, results and chart cells. For example, a 20% budget increase changes 1630 to 1956. Paid signups increase in the model. This does not prove a higher budget would preserve the same CAC in reality. Other channels receive no automatic increase.

Read last-week active users, cumulative minutes, ad revenue and paid spend. Do not call revenue minus paid spend “profit”: other costs are missing. Restore the submitted settings after the demonstration.

## Before submission

Review the three deliverables together, check any language requirements and add your names if needed. Rehearse the eight-minute presentation and a parameter change. Submit the notebook, PDF report and slides with the data required to run the model, through the channel specified by the instructor.
