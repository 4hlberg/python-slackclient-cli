# python-slackclient-cli
A command line interface for Slack  
[![PyPI version](https://badge.fury.io/py/slackclient-cli.svg)](https://badge.fury.io/py/slackclient-cli)

# Reference
  https://api.slack.com/methods

# Install
    pip install slackclient-cli

# Usage
    slackclient-cli --help
    usage: slackclient-cli [-h]
      {reactions.remove,users.setPresence,users.getPresence,groups.setPurpose,usergroups.users.update,dnd.info,reminders.info,pins.list,mpim.open,channels.kick,reminders.add,channels.unarchive,team.profile.get,im.replies,channels.join,mpim.close,groups.setTopic,emoji.list,reactions.get,chat.update,groups.list,groups.archive,stars.list,mpim.list,im.history,auth.revoke,groups.open,mpim.mark,groups.info,im.close,im.list,files.comments.delete,team.accessLogs,usergroups.users.list,groups.kick,bots.info,groups.history,users.profile.get,groups.unarchive,channels.invite,groups.replies,files.sharedPublicURL,search.files,channels.rename,channels.list,im.open,team.info,channels.leave,chat.postMessage,users.list,groups.invite,team.billableInfo,groups.rename,files.comments.edit,groups.createChild,groups.create,reminders.delete,auth.test,oauth.access,users.setPhoto,pins.remove,im.mark,dnd.teamInfo,stars.remove,reminders.list,chat.delete,users.setActive,channels.replies,channels.history,files.upload,pins.add,groups.mark,channels.archive,mpim.history,search.all,users.info,usergroups.list,channels.info,files.comments.add,dnd.setSnooze,files.delete,files.list,channels.setTopic,files.info,stars.add,usergroups.disable,mpim.replies,team.integrationLogs,users.deletePhoto,reminders.complete,channels.setPurpose,dnd.endDnd,channels.mark,search.messages,channels.create,users.identity,groups.leave,usergroups.enable,dnd.endSnooze,users.profile.set,chat.meMessage,files.revokePublicURL,usergroups.update,reactions.add,reactions.list,usergroups.create,groups.close}

    /bin/slackclient-cli [Args] [Options] Detailed options -h or --help

    positional arguments:
      {reactions.remove,users.setPresence,users.getPresence,groups.setPurpose,usergroups.users.update,dnd.info,reminders.info,pins.list,mpim.open,channels.kick,reminders.add,channels.unarchive,team.profile.get,im.replies,channels.join,mpim.close,groups.setTopic,emoji.list,reactions.get,chat.update,groups.list,groups.archive,stars.list,mpim.list,im.history,auth.revoke,groups.open,mpim.mark,groups.info,im.close,im.list,files.comments.delete,team.accessLogs,usergroups.users.list,groups.kick,bots.info,groups.history,users.profile.get,groups.unarchive,channels.invite,groups.replies,files.sharedPublicURL,search.files,channels.rename,channels.list,im.open,team.info,channels.leave,chat.postMessage,users.list,groups.invite,team.billableInfo,groups.rename,files.comments.edit,groups.createChild,groups.create,reminders.delete,auth.test,oauth.access,users.setPhoto,pins.remove,im.mark,dnd.teamInfo,stars.remove,reminders.list,chat.delete,users.setActive,channels.replies,channels.history,files.upload,pins.add,groups.mark,channels.archive,mpim.history,search.all,users.info,usergroups.list,channels.info,files.comments.add,dnd.setSnooze,files.delete,files.list,channels.setTopic,files.info,stars.add,usergroups.disable,mpim.replies,team.integrationLogs,users.deletePhoto,reminders.complete,channels.setPurpose,dnd.endDnd,channels.mark,search.messages,channels.create,users.identity,groups.leave,usergroups.enable,dnd.endSnooze,users.profile.set,chat.meMessage,files.revokePublicURL,usergroups.update,reactions.add,reactions.list,usergroups.create,groups.close

    optional arguments:
      -h, --help            show this help message and exit
      --version             show program's version number and exit

# SubCommand Usage(ex. chat.postMessage)
    usage: slackclient-cli chat.postMessage -h
    usage: slackclient-cli chat.postMessage [-h] [--quiet] --token TOKEN --channel
                                  CHANNEL --text TEXT [--parse PARSE]
                                  [--link_names LINK_NAMES]
                                  [--attachments ATTACHMENTS]
                                  [--unfurl_links UNFURL_LINKS]
                                  [--unfurl_media UNFURL_MEDIA]
                                  [--username USERNAME] [--as_user AS_USER]
                                  [--icon_url ICON_URL]
                                  [--icon_emoji ICON_EMOJI]
                                  [--thread_ts THREAD_TS]
                                  [--reply_broadcast REPLY_BROADCAST]
    optional arguments:
      -h, --help            show this help message and exit
      --quiet               don't print api response
      --token TOKEN         Authentication token. Requires scope: chat:write:bot
                            or chat:write:user
      --channel CHANNEL     Channel, private group, or IM channel to send message
                            to. Can be an encoded ID, or a name. See below for
                            more details.
      --text TEXT           Text of the message to send. See below for an
                            explanation of formatting. This field is usually
                            required, unless you're providing only attachments
                            instead.
      --parse PARSE         Text of the message to send. See below for an
                            explanation of formatting. This field is usually
                            required, unless you're providing only attachments
                            instead.Change how messages are treated. Defaults to
                            none. See below.
      --link_names LINK_NAMES
                            Find and link channel names and usernames.
      --attachments ATTACHMENTS
                            Structured message attachments.
      --unfurl_links UNFURL_LINKS
                            Pass true to enable unfurling of primarily text-based
                            content.
      --unfurl_media UNFURL_MEDIA
                            Pass false to disable unfurling of media content.
      --username USERNAME   Set your bot's user name. Must be used in conjunction
                            with as_user set to false, otherwise ignored. See
                            authorship below.
      --as_user AS_USER     Pass true to post the message as the authed user,
                            instead of as a bot. Defaults to false. See authorship
                            below.
      --icon_url ICON_URL   URL to an image to use as the icon for this message.
                            Must be used in conjunction with as_user set to false,
                            otherwise ignored. See authorship below.
      --icon_emoji ICON_EMOJI
                            Emoji to use as the icon for this message. Overrides
                            icon_url. Must be used in conjunction with as_user set
                            to false, otherwise ignored. See authorship below.
      --thread_ts THREAD_TS
                            Provide another message's ts value to make this
                            message a reply. Avoid using a reply's ts value; use
                            its parent instead.
      --reply_broadcast REPLY_BROADCAST
                            Used in conjunction with thread_ts and indicates
                            whether reply should be made visible to everyone in
                            the channel or conversation. Defaults to false.

    # It can also be specified by environment variable
    export SLACK_API_TOKEN='xoxp-xxxxxxxxxxxxxxxxx'
    export SLACK_API_CHANNEL = '#some_channel'
    export SLACK_API_{arg.upper()} = 'some value'

# License
MIT License
