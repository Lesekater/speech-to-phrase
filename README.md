# Speech-to-phrase

**NOTE:** This library is in beta! Expect things to change and break.

A fast but limited speech-to-text system that is personalized with your [Home Assistant](https://www.home-assistant.io/) device names.

Speech-to-phrase is not a general purpose speech recognition system. Instead of answering the question "what did the user say?", it answers "which of the phrases I know did the user say?".
This is accomplished by combining [pre-defined sentence templates](speech_to_phrase/sentences) with the names of your Home Assistant [entities, areas, and floors](https://www.home-assistant.io/getting-started/concepts-terminology/) that have been [exposed to Assist](https://www.home-assistant.io/voice_control/voice_remote_expose_devices/).

[![Show add-on](https://my.home-assistant.io/badges/supervisor_addon.svg)](https://my.home-assistant.io/redirect/supervisor_addon/?addon=47701997_speech-to-phrase&repository_url=https%3A%2F%2Fgithub.com%2Frhasspy%2Fhassio-addons)

## Supported Languages

- [English](#english)
- Français (French)
- Deutsch (German)
- Nederlands (Dutch)
- Spanish (Español)
- Italian (Italiano)

## English

### Date and Time

- "what time is it?"
- "what's the date?"

### Weather and Temperature

- "what's the weather?"
    - Requires a [weather][] entity to be configured
- "what's the weather like in New York?"
    - Requires a [weather][] entity named "New York"
- "what's the temperature?"
    - Requires a [climate][] entity to be configured
- "what's the temperature of the EcoBee?"
    - Requires a [climate][] entity named "EcoBee"
    
### Lights

- "turn on/off the lights"
    - Requires voice satellite to be in an [area][]
- "turn on/off standing light"
    - Requires a [light][] entity named "standing light"
- "turn on/off lights in the kitchen"
    - Requires an [area][] named "kitchen"
- "turn on/off lights on the first floor"
    - Requires a [floor][] named "first floor"
- "set kitchen lights to green"
    - Requires an [area][] named "kitchen" with at least one [light][] entity in it that supports setting color
- "set bed light brightness to 100 percent"
    - Requires a [light][] entity named "bed light" that supports setting brightness
    - Brightness from 10-100 by 10s

### Sensors

- "what is the outdoor humidity?"
    - Requires a [sensor][] entity named "outdoor humidity"

### Doors and Windows

- "open/close the garage door"
    - Requires a [cover][] entity named "garage door"
- "is the garage door open/closed?"
    - Requires a [cover][] entity named "garage door"
    
### Locks

- "lock/unlock the front door"
    - Requires a [lock][] entity named "front door"
- "is the front door locked/unlocked?"
    - Requires a [lock][] entity named "front door"

### Media

- "pause"
    - Requires a [media player][] entity that is playing
- "resume"
    - Requires a [media player][] entity that is paused
- "next"
    - Requires a [media player][] entity to that is playing and supports next track

### Timers

- "set a timer for five minutes"
    - minutes from 1-10, 15, 20, 30, 40, 45, 50-100 by 10s
- "set a timer for thirty seconds"
    - seconds from 10-100 by 5s
- "set a timer for three hours and ten minutes"
    - hours from 1-24
- "pause/resume timer"
- "cancel timer"
- "cancel all timers"
- "timer status"

### Scenes and Scripts

- "run party time"
    - Requires a [script][] named "party time"
- "activate mood lighting"
    - Requires a [scene][] named "mood lighting"

### Miscellaneous

- "nevermind"

<!-- Links -->
[area]: https://www.home-assistant.io/docs/organizing/#area
[climate]: https://www.home-assistant.io/integrations/climate/
[cover]: https://www.home-assistant.io/integrations/cover/
[floor]: https://www.home-assistant.io/docs/organizing/#floor
[light]: https://www.home-assistant.io/integrations/light/
[lock]: https://www.home-assistant.io/integrations/lock/
[media player]: https://www.home-assistant.io/integrations/media_player/
[scene]: https://www.home-assistant.io/integrations/scene/
[script]: https://www.home-assistant.io/integrations/script/
[sensor]: https://www.home-assistant.io/integrations/sensor/
[weather]: https://www.home-assistant.io/integrations/weather/
