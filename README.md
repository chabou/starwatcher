# StarWatcher

Watch a github repository and push a notification at every new star

## Deploy with one line

Using [now](https://zeit.co/now), you don't even need to checkout and build this
repository.

`$ now -e REPO="<username>/<repository>" -e
SLACK_URL="<your_slack_incoming_webhook>" chabou/starwatcher`

That's it.

## Options

| Option            | Default       | Comments                                                                                                                                                                             |
| ----------------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `REPO`            | `zeit/hyper`  | Github repository with username. Example: `chabou/hyper-pane`                                                                                                                        |
| `CHECK_INTERVAL`  | `2m`          | Time to wait between 2 GitHub API calls. Example: `1000`, `2m`, `1h`. Be careful to [Github rate limiting](https://developer.github.com/v3/#rate-limiting)                           |
| `NOTIFY_INTERVAL` | `1`           | Divisor use to perform a modulo operation to determine if a new star should trigger a notification. Example: a value of `5` will trigger notifications for a 5, 10 or 15 star count. |
| `SLACK_URL`       | none          | Slack webhook URL. Example: `https://hooks.slack.com/services/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`                                                                          |
| `SLACK_CHANNEL`   | none          | Slack channel where notifications will be post. Example: `general`                                                                                                                   |
| `SLACK_USERNAME`  | `StarWatcher` | Name used as sender in slack notification                                                                                                                                            |

## Notification

Only Slack webhook is supported
