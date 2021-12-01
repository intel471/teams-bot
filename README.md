# Intel 471's Titan + Microsoft Teams Integration

Titan delivers structured technical and non-technical data and intelligence that is continually updated by Intel 471's global team and automated processes.

With this integration you'll stay updated on what's going on in Titan without leaving Microsoft Teams. The updates will be delivered either to your private space or to the Teams channel for better collaboration.

## Table of Contents
- [Get started](#get-started)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Authorization](#authorization)
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
<p align="left"><img width="500" alt="Intro message" src="img/intro.png"></p>
 
## Authorization
At this point the bot is installed but is not authorized yet. Authorization is required so the bot can access the Titan data on your behalf. Click on the **Intel 41 bot auth page** link provided in the welcome message and provide your Titan credentials.

<p align="left"><img width="500" alt="Auth page" src="img/auth-page.png"></p>

 Once completed, all supported streams with default intervals will be activated. You can modify them later using the `enable` command.

 <p align="left"><img width="500" alt="Auth confirmed" src="img/auth-confirmed.png"></p>

## Feedback

Please send an email to support@intel471.com to request a feature or report a problem.
