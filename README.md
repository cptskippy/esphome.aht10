Modifying the AHT10 component to send the soft reset command during setup.

Example yaml to use in esphome device config:

    external_components:
      - source:
          url: https://github.com/cptskippy/esphome.aht10
          type: git
          ref: main
        components: aht10
        refresh: 0s
    
    sensor:
      - platform: aht10
        update_interval: 20s

    i2c:
      sda: GPIO0
      scl: GPIO2
      scan: true
