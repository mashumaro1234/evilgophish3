# 09/11/2022

Made updates to credential logging so that it is completely unique. This was done by parsing `RIds` out of incoming `evilginx2` requests inside the `evilginx2` source code. By including a unique identifier with each credential submission, this will ensure a credential from a previous campaign will never log into a current campaign. Improvements were also made to `setup.sh`.

# 09/13/2022

Added the option to send campaign events as messages to a channel via `Microsoft Teams`.

# 09/14/2022

Removed transparency endpoint and messages from `GoPhish` altogether and increased the length of `RIds` to `10`.

# 09/16/2022

Added `SMS` campaign support with `Twilio`! Enjoy!

# 09/18/2022

Added error handling of failed `SMS` messages into the dashboard/database. If the sending of an `SMS` message fails, the error will now display right in the `GUI`. Updates to the dashboard were also made so that when viewing campaign results, statistic names now match `SMS` updates. For example, `Email Sent` now displays as `Email/SMS Sent` in the dashboard, etc.

# 09/19/2022

Added the option for operators to set their own `RId` value to use in phishing URLs to combat fingerprinting links.

# 09/20/2022

Removed `Microsoft Teams` messages to a channel and replaced with `Pusher` end-to-end encrypted channels for security reasons.

# 09/24/2022

Added notification count to `Pusher` feed app as well as sound option for events. Color changes were also made to the app :)

# 09/26/2022

Added the ability to view full token `JSON` strings from `evilginx` directly in `GoPhish` dashboard :)

# 09/30/2022

Removed the need to create a fake landing inside `GoPhish` as part of a campaign setup. Removed `Add Tracking Image` button to avoid mistakes being made with operators using this button. This forces the manual insertion of image tags into email templates as it is needed for tracking to properly work. Also added enhancements to the logging process.

# 10/02/2022

Added the `Add Tracking Image` button back and ability to handle email opened tracking events directly from `evilginx2`. This removes the need to proxy to the local `GoPhish` server altogether.

# 10/03/2022

Made further enhancements to the logging process so that if a user triggers an event more than once, every instance will now be captured. Changed `Pusher` notifications to trigger directly from `evilginx` to ensure feed is completely realtime.

# 10/05/2022

Removed `Pusher` messages to a channel to avoid message limit and to ease the live feed setup process. The live feed has been changed to operate completely local, without sending victim data to any remote `API`. The live feed also now has no message limits and added the ability to view full token JSON in live feed :)

# 10/29/2022

Made `Apache2` blacklist optional.

# 01/10/2023

Added `Cisco VPN` phishlet, merged pull request that allows operators to get source `IP` information for victims when generating `GoPhish` reports.

# 02/03/2023

Added some improved logic for logging credentials to `GoPhish` where sometimes the username parameter of a phishlet was lost due to not checking if it was empty. This should improve the overall user experience and credential logging.

# 03/14/2023

Removed a "X-Evilginx" header IOC that was hidden as a XOR encrypted byte array.

# 04/09/2023

Added the option to force a Google reCAPTCHA v2 challenge before granting access to a lure. This was done to combat domain takedowns and thwart off bots.

# 04/19/2023

Added the option to force a Cloudflare Turnstile challenge before granting access to lure. Again this was done to try to thwart off bots.

# 07/08/2023

Upgraded `evilginx2` to `evilginx3`! :)

# 07/08/2023

Deprecated the `Cloudflare Turnstile` and `Google reCAPTCHA` features due to the `redirectors` feature of `evilginx3` which accomplishes the same task.

# 07/15/2023

Made the announcement of my transition into `GitHub Sponsors` and additional announcements for the future of this project. Changes include the end of support for `phishlets` and keeping this public version of the project one version behind the private version for sponsors.

# 08/08/2023

Implemented the version `3.1.0` release of `evilginx3`.