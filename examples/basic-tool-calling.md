# Basic Tool Calling Example

## Simple Weather Lookup Implementation

```python
from typing import Dict, Any

def get_weather(city: str) -> Dict[str, Any]:
    """Get current weather for a specified city."""
    # Mock implementation - replace with actual API call
    return {
        "city": city,
        "temperature_celsius": 22.5,
        "humidity_percent": 65,
        "conditions": "Partly cloudy",
        "wind_speed_kph": 12
    }

# Usage example
result = get_weather("São Paulo")
print(f"Weather in {result['city']}: {result['temperature_celsius']}°C, {result['conditions']}")
```

## Key Concepts Demonstrated

- **Function Definition:** Clear parameter types and return structure
- **Docstring Documentation:** Describes what the tool does for LLM understanding
- **Structured Output:** Consistent dictionary format enables reliable parsing
- **Error Handling Ready:** Easy to add try/except blocks for API failures

## Next Steps

1. Replace mock data with actual weather API integration (OpenWeatherMap, WeatherAPI)
2. Add error handling for invalid city names and network failures
3. Implement caching to reduce redundant API calls during conversations
4. Create additional tools: forecast lookup, unit conversion, alert checking

---

*Related: [Tool Calling Overview](../tool-calling/README.md) | [Function Calling Details](../tool-calling/function-calling/README.md)*
