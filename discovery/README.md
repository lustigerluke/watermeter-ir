# DISCOVERY

Assuming you do have some idea of how MQTT works. 


<table>
<table style="width:600px">
  <colgroup>
    <col style="width:200px">
    <col style="width:400px">
  </colgroup>
  <tr>
    <th>MQTT topic</th>
    <th>JSON content</th>
  </tr>
  <tr>
    <td>homeassistant/sensor/kamstir_mac/config </td>
    <td><pre><code>
    {
        "name": "MAC Address",
        "state_topic": "kamstir/smart_gateways/mac_address",
        "unique_id": "kamstir_mac",
        "entity_category": "diagnostic",
        "value_template": "{{ value }}",
        "icon": "mdi:lan",
        "device": {
            "identifiers": ["kamstirgateway"]
        }
    }
  </code></pre></td>
  </tr>

  <tr>
    <td>homeassistant/sensor/kamstir_battery_days_left/config </td>
    <td><pre><code>
    {
      "name": "Battery Days Left",
      "state_topic": "kamstir/reading/battery_days_left",
      "unique_id": "kamstir_battery_days_left",
      "value_template": "{{ value }}",
      "entity_category": "diagnostic",
      "icon": "mdi:battery",
      "device": {
        "identifiers": ["kamstirgateway"]
      }
    }
    </code></pre></td>
  </tr>

  <tr>
    <td>homeassistant/sensor/kamstir_gateway_firmware_version/config </td>
    <td><pre><code>
    {
      "name": "Firmware: current Version",
      "state_topic": "kamstir/smart_gateways/running_firmware_version",
      "unique_id": "kamstir_gateway_firmware_version",
      "entity_category": "diagnostic",
      "icon": "mdi:chip",
      "value_template": "{{ value }}",
      "device": {
        "identifiers": ["kamstirgateway"],
        "name": "watermeter-ir",
        "manufacturer": "Smart Gateways",
        "model": "Kamst-IR Gateway"
      }
    }
    </code></pre></td>
  </tr>

  <tr>
    <td>homeassistant/sensor/kamstir_available_gateway_firmware_version/config</td>
    <td><pre><code>
    {
      "name": "Firmware: available Version",
      "state_topic": "kamstir/smart_gateways/available_firmware_version",
      "unique_id": "kamstir_available_gateway_firmware_version",
      "entity_category": "diagnostic",
      "icon": "mdi:update",
      "value_template": "{{ value }}",
      "device": {
        "identifiers": ["kamstirgateway"],
        "name": "watermeter-ir",
        "manufacturer": "Smart Gateways",
        "model": "Kamst-IR Gateway"
      }
    }
    </code></pre></td>
  </tr>

  <tr>
    <td>homeassistant/sensor/kamstir_startup_time/config</td>
    <td><pre><code>
    {
      "name": "Startup Time",
      "state_topic": "kamstir/smart_gateways/startup_time",
      "unique_id": "kamstir_startup_time",
      "device_class": "timestamp",
      "entity_category": "diagnostic",
      "icon": "mdi:clock-start",
      "value_template": "{{ value }}",
      "device": {
        "identifiers": ["kamstirgateway"],
        "name": "watermeter-ir",
        "manufacturer": "Smart Gateways",
        "model": "Kamst-IR Gateway"
      }
    }
    </code></pre></td>
  </tr>

  <tr>
    <td>homeassistant/sensor/kamstir_ip_address/config</td>
    <td><pre><code>
    {
      "name": "IP Address",
      "state_topic": "kamstir/smart_gateways/ip_address",
      "unique_id": "kamstir_ip_address",
      "entity_category": "diagnostic",
      "icon": "mdi:ip-network",
      "value_template": "{{ value }}",
      "device": {
        "identifiers": ["kamstirgateway"],
        "name": "watermeter-ir",
        "manufacturer": "Smart Gateways",
        "model": "Kamst-IR Gateway"
      }
    }
    </code></pre></td>
  </tr>
</table>