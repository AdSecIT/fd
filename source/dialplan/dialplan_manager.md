# Dialplan Manager

The dialplan is used to setup call destinations based on conditions and context. You can use the dialplan to send calls to gateways, auto attendants, external numbers, to scripts, or any destination.

| Dialplan Name             | Dialplan Number      |
|---------------------------|----------------------|
| [caller-details](dialplan_details.html#caller-details) |                      |
| *Details about the caller.* |                      |
| **not-found:**            |                      |
| *Used to help trigger fail2ban from bogus calls.* |                      |
| **call-limit:**           |                      |
| *Limit calls based on number of calls and more.* |                      |
| **speed_dial:**           | *0[ext]              |
| *Uses LUA for extension speed dial.* |                      |
| **agent_status:**         | *22                  |
| *Agent login to call center.* |                      |
| **page-extension:**       | *8[ext]              |
| *Password protected paging of an extension.* |                      |
| **eavesdrop:**            | *33[ext]             |
| *Password protected eavesdropping on extensions.* |                      |
| **send_to_voicemail:**    | *99[ext]             |
| *Sending an active call to an extensions voicemail.* |                      |
| **cf:**                   | cf                   |
| *                         |                      |
| **echo:**                 | *9196                |
| *Real time echo test.*    |                      |
| **milliwatt:**            | *9197                |
| *Plays a milliwatt test tone.* |                      |
| **recordings:**           | *732                 |
| *Password protected way to record audio that can be used in other applications like IVR.* |                      |
| **directory:**            | *411                 |
| *Directory of users.*     |                      |
| **user_exists:**          |                      |
| *Determines if a user exists on the switch.* |                      |
| **caller-details:**       |                      |
| *Logic to decipher caller details.* |                      |
| **call-direction:**       |                      |
| *Determines the direction of the call.* |                      |
| **variables:**            |                      |
| *Set variables on a domain level.* |                      |
| **is_local:**             |                      |
| *Can be used to evaluate calls as local.* |                      |
| **call_block:**           |                      |
| *Block calls from reaching endpoints.* |                      |
| **user_record:**          |                      |
| *Used to record calls.*   |                      |
| **redial:**               | *870                 |
| *Dial the last number that was dialed.* |                      |
| **default_caller_id:**    |                      |
| *Caller ID that can be set per domain.* |                      |
| **agent_status_id:**      | *23                  |
| *Status of the agent.*    |                      |
| **provision:**            | *11,*12              |
| *Used with devices.*      |                      |
| **clear_sip_auto_answer:**|                      |
| *                         |                      |
| **nway_conference**       | nway                 |
| *                         |                      |
| **cidlookup:**            |                      |
| *                         |                      |
| **group-intercept:**      | *8                   |
| *Intercepts a call from a defined group.* |                      |
| **page:**                 | *724                 |
| *Password protected paging defined set of extensions.* |                      |
| **conf-xfer:**            |                      |
| *                         |                      |
| **call_privacy:**         | *67[d+]              |
| *Send a privacy header to the carrier to hide caller id.* |                      |
| **call_return:**          | *69                  |
| *Call the last number that called the endpoint.* |                      |
| **extension_queue:**      | *800[ext]            |
| *                         |                      |
| **intercept-ext:**        | **[ext]              |
| *Password protected intercept of an extension.* |                      |
| **dx:**                   | dx                   |
| *Direct transfer.*        |                      |
| **att_xfer:**             | att_xfer             |
| *Attended transfer.*      |                      |
| **extension-to-voicemail:** | [ext]              |
| *Used for extension to voicemail.* |                      |
| **vmain**                 | *98                  |
| *Main menu to access any voicemail using a pin number.* |                      |
| **xfer_vm**               | xfer_vm              |
| *Transfer to voicemail.*  |                      |
| **is_transfer**           | is_transfer          |
| *Used for call transferring.* |                      |
| [vmain_user](/en/latest/dialplan/dialplan_details.html#voicemail-vmain-user) | *97                  |
| *Endpoint's voicemail using a pin number.* |                      |
| **delay_echo**            | *9195                |
| *Play back an echo with a 5 second delay.* |                      |
| **please_hold**           |                      |
| *Plays an audio file when on hold.* |                      |
| **is_zrtp_secure**        |                      |
| *                         |                      |
| **is_secure**             | is_secure            |
| *                         |                      |
| **tone_stream**           | *9198                |
| *Tones that stream and sound like Tetris music.* |                      |
| **hold_music**            | *9664                |
| *Play music on hold. Good for testing on an endpoint.* |                      |
| **freeswitch_conference** | *9888                |
| *An easy way to join the Cluecon Weekly call.* |                      |
| **disa**                  | *3472                |
| *Call in to a phone number and provide a pin to dial out.* |                      |
| **wake-up**               | *925                 |
| *Schedule date and time for an automated call.* |                      |
| **extension_queue**       |                      |
| *                         |                      |
| **valet_park**            | park+*5901-*5999     |
| *Default range to valet park calls.* |                      |
| **valet_park_in**         | park+*5900           |
| *Default number to send valet calls to.* |                      |
| **valet_park_out**        | park+*5901-*5999     |
| *Default range to retrieve valet parked calls.* |                      |
| [operator](dialplan_details.html#operator) | 0                    |
| *Configurable option for an operator.* |                      |
| [operator-forward](dialplan_details.html#operator-forward) | *000                 |
| *Uses dial_string.lua.*   |                      |
| [do-not-disturb](dialplan_details.html#do-not-disturb) | *77,*78,*79          |
| *Turn on, toggle, turn off do not disturb.* |                      |
| [call-forward](dialplan_details.html#call-forward) | *72,*73,*74          |
| *Turn on, toggle on/off and turn off call forwarding.* |                      |
| [Follow Me](dialplan_details.html#follow-me) | *21                  |
| *Forwards call to defined list of phone numbers or extensions.* |                      |
| [bind_digit_action](dialplan_details.html#bind-digit-action) |                      |
| *                         |                      |
| [call_screen](dialplan_details.html#call-screen) | [ext]                |
| *Play an audio file and give options to the caller to record a short message for the <br> call recipient. Call recipient can then accept or reject the call.* |                      |
| [local_extension](dialplan_details.html#local-extension) | [ext]                |
| *Examines to see if the extension is local.* |                      |
| [voicemail](dialplan_details.html#voicemail) | [ext]                |
| *Voicemail for extensions.* |                      |
