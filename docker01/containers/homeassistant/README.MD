Im Container die configuration.yaml ändern und die IPs entsprechend abändern.
Wenn nicht sicher ist welche IP freigegeben werden muss einfach einmal den Container starten und die URL aufrufen.
Im Log wird dann die IP angezeigt die freigegeben werden muss.

```yaml
# Configure a default setup of Home Assistant (frontend, api, etc)
default_config:

http:
  use_x_forwarded_for: true
  trusted_proxies:
  - 127.0.0.1
  - 172.18.0.2
  ip_ban_enabled: true
  login_attempts_threshold: 5

# Text to speech
tts:
  - platform: google_translate

group: !include groups.yaml
automation: !include automations.yaml
script: !include scripts.yaml
scene: !include scenes.yaml
```
