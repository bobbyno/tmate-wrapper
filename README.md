# tm: tmate-wrapper

`tm` is a small wrapper script that enhances [tmate's](https://tmate.io) usability and makes it easy to integrate with other tools.

Use `tm` anywhere you would have used `tmate`.

### Start a new tmate session

`tm`

This starts `tmate` as a daemon as described on the [tmate.io website](https://tmate.io) and attaches a session.

### Show your tmate addresses

```
# read-write address
tm address
=> ssh qRBbcBAQJcU5NazhagxewPVHh@ny.tmate.io

# read-only address
tm address-ro
=> ssh ro-C4b1hemhlJDqQxCnt07SdvyUq@ny2.tmate.io

# html address
tm address-html
=> https://tmate.io/t/sww8BF5FrYnJi4iuw1d4qPsQl

# read-only html address
tm address-html
=> https://tmate.io/t/ro-C4b1hemhlJDqQxCnt07SdvyUq

```

If you're on OS X, add `| pbcopy` to the above to easily copy your links.

### Send an invitation to @someone in a #channel on Slack

`tm slack channel someone`

### Show tmate's version

`tm version` or `tm -V`

### Get help for tmate / tmux and the tmate-wrapper

`tm help` or `tm -h`

Any of these `tmate` commands will work through `tm`.

## Installation

`git clone https://github.com/bobbyno/tmate-wrapper.git`

`make install`

This will create a symlink to `/usr/local/bin/tm`.

### Slack Integration (optional)

To enable the `slack` command, add a _Slack Incoming Webhook_
address as an environment variable in your `.bashrc` or equivalent:

```
export SLACK_WEBHOOK=https://hooks.slack.com/services/xyz/123
```
