# Intel 471's Titan + Microsoft Teams Integration

Titan delivers structured technical and non-technical data and intelligence that is continually updated by Intel 471's global team and automated processes.

With this integration you'll stay updated on what's going on in Titan without leaving Microsoft Teams. The updates will be delivered either to your private space or to the Teams channel for better collaboration.

## Table of Contents
- [Get started](#get-started)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Authorization](#authorization)
- [Available streams](#available-streams)
 - [Interacting with the bot](#interacting-with-the-bot) 
   - [Showing status](#showing-status)
   - [Enabling streams](#enabling-streams)
   - [Modifying streams](#modifying-streams)
   - [Disabling streams](#disabling-streams)
- [Uninstalling](#uninstalling)
- [Feedback](#feedback)
--------
## Get started
### Requirements

Titan API credentials.

### Installation

You can go to Microsoft Teams app store and install **Intel 471 Bot** app or you can install it directly from [here](https://teams.microsoft.com). *This step is not ready yet until the app is submitted to the store*

Once added to your Teams instance, navigate to Apps, click on **Intel 471 bot** and add it to one of the following scopes:

| Scope | How to add | How to interact |
|-----|----|-----|
| Private scope<br />*app in left-hand toolbar* | Click *Open* button| Just type a command (e.g. `status`)  |
| Private chat | Click *Add to a chat*| Mention the bot using `@intel471` handle (e.g. `@intel471 status`) |
| Team<br />*can be configured in any of the team's channels* | Click *Add to a team*.<br />Then navigate to the team's channel of your choice and type `@intel471 install` | ditto  |

Upon installation, a welcome message with short manual and basic information will be sent to the chosen scope. 
<p align="center"><img width="500" alt="Intro message" src="img/intro.png"></p>
 
### Authorization
At this point the bot is installed but is not authorized yet. Authorization is required so the bot can access the Titan data on your behalf. Click on the **Intel 41 bot auth page** link provided in the welcome message and provide your Titan credentials.

<p align="center"><img width="500" alt="Auth page" src="img/auth-page.png"></p>

 Once completed, all supported streams with default intervals will be activated. The
 bot is now all set and you will start seeing the updates shortly after they appear in Titan.

 <p align="center"><img width="500" alt="Auth confirmed" src="img/auth-confirmed.png"></p>

## Uninstalling

| Scope | How to uninstall |
|-----|----|
| Private scope<br />*app in left-hand toolbar* | Right click the bot's icon in the left-hand toolbar and click *Uninstall*|
| Private chat | Click three dots next to selected chat -> Manage apps -> Click trash bin icon next to **Intel 471 bot** | 
| Team<br />*for all channels* | Click three dots next to selected team -> Manage team -> Apps -> Click trash bin icon next to **Intel 471 bot** | 
| Team<br />*selected channel* | Navigate to the channel of your choice and type `@intel471 uninstall` | 

## Interacting with the bot

You can send the bot commands in order to see its status and to configure the streams.
In private scope you just type the command. In other scopes you also need to mention
the bot by its handle `@intel471`. In following examples the latter form will be used.

<p align="center"><img width="500" alt="Auth confirmed" src="img/command.png"></p>

`@intel471 help` - Shows help information.

`@intel471 status` - Shows the list of active and inactive streams in your channel and information regarding the installed instance.

`@intel471 enable stream interval [options]` - Enables or reschedules the specified stream. The first argument is the name of the stream. The second argument is the interval, which can be provided in several formats: every several minutes (e.g., `15m`), every several hours (e.g., `2h`) or every day at a specific time UTC (e.g., `14:30`). The following arguments are optional and specific to the selected stream. Example: `@intel471 enable fintel 15m`.

`@intel471 disable stream [options]` - Disables selected stream or removes options from the stream. You can turn the stream back on at any time using the enable command. Example: `@intel471 disable fintel`.

`@intel471 watchers` - Shows the list of the logged-in user’s Watcher groups defined in Titan.

## Available streams

- `fintel` - Finished Intelligence - key insights from Intel 471 field reporting, raw underground content, open sources and more.
- `malware` - Technical updates of malware families and adversaries.
- `news` - Latest announcements and blog posts.
- `reports` - Detailed reports based on tactical observations of cybercriminal activity enhanced with our assessment of credibility and reliability.
- `sitrep` - Summary status reports of an ongoing situation or activity monitored by Intel 471.
- `spotrep` - Brief summaries used to communicate timely intelligence or status changes for significant events.
- `alerts` - Alerts matching search criteria defined in Titan’s Watchers for the logged-in user. This stream accepts the following optional arguments:
    * `ignoreRead` - Do not show alerts marked as read. Show all by default
    * `markAsRead` - Mark alerts posted to the channel as read. Do not mark by default.
    * `<watcher-group-uid>` - One or more unique identifiers (UIDs) of Watcher groups to narrow down the stream. The UIDs can be obtained from the `watchers` command. Example showing the full command to subscribe to only unread alerts from two selected Watcher groups and continue to mark them as read: `@intel471 enable alerts 10m ignoreRead markAsRead 7fbb148b-e59f... e59f4798-9634...`



## Feedback

Please send an email to support@intel471.com to request a feature or report a problem.
