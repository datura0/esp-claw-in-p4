---
{
  "name": "read_temperature",
  "description": "Read the ESP32-P4 internal temperature sensor. Use when the user asks about chip temperature, thermal status, or overheating concerns.",
  "metadata": {
    "cap_groups": ["cap_system"],
    "manage_mode": "readonly"
  }
}
---

# Read Internal Temperature Sensor

Use the Lua `system.temp()` function to read the ESP32-P4 internal die temperature in degrees Celsius.

## Usage

Run in the Lua console:
```lua
system.temp()
```

Or from a Lua script:
```lua
local temp = system.temp()
print(string.format("CPU Temperature: %.1f°C", temp))
```

## Notes
- Returns temperature in degrees Celsius as a float (e.g., 45.3)
- Range: -10°C to 80°C
- The sensor is initialized automatically on first call
- No GPIOs are used (internal sensor)
