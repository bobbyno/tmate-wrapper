# tmate-wrapper: tm

Provides some extra features for `tmate`, most notably a convenient way to
invite people to join your `tmate` session on Slack with a link to your video
session in Zoom. Yes, this is highly biased towards my workflow, but at 50 lines
of Bash, it would be very easy to extend the wrapper to support other tools.

This is a true wrapper: Any `tmate` command will work through `tmate-wrapper`.
Think of `tm` as your new `tmate`.

### Start a new tmate session

`tm`

### Send an invitation to @someone in a #channel on Slack

`tm slack channel someone`

### Show your tmate ssh address

```
tm address
=> ssh qRBbcBAQJcU5NazhagxewPVHh@ny.tmate.io
```

### Show tmate's version

`tm -v`

### Get help for tmate / tmux and the tmate-wrapper

`tm -h`

## Installing

`git clone https://github.com/bobbyno/tmate-wrapper.git`
`make install`

This will create a symlink to `/usr/local/bin/tm`.

Create two environment variables in your `.bashrc` or equivalent:

* _Zoom Personal Meeting ID (PMI)_

In the Meetings tab in the zoom app, check "Always use PMI for instant meetings on this computer".
Use your PMI without dashes in your default zoom url:

`export DEFAULT_ZOOM=https://zoom.us/j/655321`

* _Slack Incoming Webhook_

```
export SLACK_WEBHOOK=https://hooks.slack.com/services/xyz/123
```
