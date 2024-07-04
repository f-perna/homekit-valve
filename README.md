# homekit-valve
This is still heavily under development, any help is greatly appriciated

## Overview
This is a custom componnet for home assistant that adds valve timer support to the core component `homekit`

## Progress
- Support for a single valve switch
- Set/Adjust timer in settings of accessory
- Timer countsdown and updates accordingly with the irrigation timer entity on home assistant

## Requirments
- Must have a `number` entity in minutes that counts down immediately after being set
- Use `entity_config` option `linked_irrigation_timer` to reference the `number` entity mentioned above in `configuration.yaml`
- Example:
```
homekit:
  - name: HASS Bridge
    port: XXXXX
    filter:
      include_entities:
        - valve.water_timer_valve
        
    entity_config:
      valve.water_timer_valve:
        linked_irrigation_timer: number.water_timer_valve_irrigation_time

```

## Screenshots
![0](https://github.com/f-perna/homekit-valve/assets/113391793/90f75162-4c01-4db2-8804-951e4151969d)
