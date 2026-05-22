# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date: 22-05-2026
# Register no:212224230056
# Aim:
   Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools
# Title: Framing Prompts for AI-Assisted Project Coding
## Objective
Learners will understand how to design effective prompts for AI tools to assist in coding tasks related to mini projects and final year projects. The activity focuses on creating prompts that help AI systems:

* Generate Python code for interacting with APIs
* Compare outputs from multiple APIs
* Suggest meaningful insights and next steps
* Improve coding efficiency and project development

# AI Tool Used

* [ChatGPT](https://chatgpt.com?utm_source=chatgpt.com)

# Explanation

AI-assisted coding helps developers generate code, debug applications, integrate APIs, and analyze outputs efficiently. Instead of directly writing programs, students learn how to frame prompts that guide AI systems to produce accurate and useful coding solutions.

Effective prompts should clearly mention:

* Programming language
* Task requirements
* Input and output format
* API details
* Expected comparison or analysis

# Exercise Description

Students must practice creating prompts that guide AI tools to:

1. Generate Python code for interacting with multiple APIs
2. Compare outputs from different APIs and highlight differences
3. Suggest insights or next steps based on generated results
# Use Case Scenario
## Project Scenario

A student is developing a **Weather Analysis Application** that collects weather information from multiple APIs and compares temperature, humidity, and forecast details.

The student uses AI prompts to generate Python code and analytical insights.

---

# Stage 1: Prompt for Python API Integration

## Designed Prompt

“Generate Python code using the requests library to fetch weather data from two APIs (OpenWeatherMap and WeatherAPI). Display temperature, humidity, and weather conditions for Chennai city.”


## AI-Generated Response

```python
import requests

city = "Chennai"

api1 = "https://api.openweathermap.org/data/2.5/weather?q=Chennai&appid=YOUR_API_KEY"
response1 = requests.get(api1).json()

print("OpenWeatherMap Data")
print("Temperature:", response1["main"]["temp"])
print("Humidity:", response1["main"]["humidity"])

api2 = "https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=Chennai"
response2 = requests.get(api2).json()

print("\nWeatherAPI Data")
print("Temperature:", response2["current"]["temp_c"])
print("Humidity:", response2["current"]["humidity"])
```

## Explanation

The AI generated Python code that:

* Connects to two weather APIs
* Retrieves live weather data
* Displays temperature and humidity values


# Stage 2: Prompt for Comparing API Outputs

## Designed Prompt

“Write Python code to compare temperature values returned by OpenWeatherMap and WeatherAPI and display the difference.”


## AI-Generated Response

```python
temp1 = response1["main"]["temp"]
temp2 = response2["current"]["temp_c"]

difference = abs(temp1 - temp2)

print("Temperature Difference:", difference)
```


## Explanation

The AI-generated code compares outputs from two APIs and calculates the temperature variation.


# Stage 3: Prompt for Insights and Recommendations

## Designed Prompt

“Analyze the compared weather API outputs and suggest meaningful insights if temperature differences are greater than 3 degrees.”

## AI-Generated Response

```python
if difference > 3:
    print("Significant variation detected between APIs.")
    print("Recommendation: Verify data source reliability.")
else:
    print("Weather data from both APIs is consistent.")
```


## Explanation

The AI suggested actionable insights based on output comparison and added recommendation logic.

# Final Code :
```
import requests

# -------------------------------
# WEATHER API INTEGRATION PROJECT
# -------------------------------

city = "Chennai"

# Replace with your actual API keys
OPENWEATHER_API_KEY = "YOUR_OPENWEATHER_API_KEY"
WEATHERAPI_KEY = "YOUR_WEATHERAPI_KEY"

# -------------------------------
# FETCH DATA FROM OPENWEATHERMAP
# -------------------------------

openweather_url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={OPENWEATHER_API_KEY}&units=metric"

response1 = requests.get(openweather_url)

if response1.status_code == 200:
    data1 = response1.json()

    temp1 = data1["main"]["temp"]
    humidity1 = data1["main"]["humidity"]
    condition1 = data1["weather"][0]["description"]

    print("OpenWeatherMap Data")
    print("--------------------")
    print("Temperature:", temp1, "°C")
    print("Humidity:", humidity1, "%")
    print("Condition:", condition1)

else:
    print("Error fetching OpenWeatherMap data")

# -------------------------------
# FETCH DATA FROM WEATHERAPI
# -------------------------------

weatherapi_url = f"https://api.weatherapi.com/v1/current.json?key={WEATHERAPI_KEY}&q={city}"

response2 = requests.get(weatherapi_url)

if response2.status_code == 200:
    data2 = response2.json()

    temp2 = data2["current"]["temp_c"]
    humidity2 = data2["current"]["humidity"]
    condition2 = data2["current"]["condition"]["text"]

    print("\nWeatherAPI Data")
    print("--------------------")
    print("Temperature:", temp2, "°C")
    print("Humidity:", humidity2, "%")
    print("Condition:", condition2)

else:
    print("Error fetching WeatherAPI data")

# -------------------------------
# COMPARE OUTPUTS
# -------------------------------

difference = abs(temp1 - temp2)

print("\nTemperature Comparison")
print("----------------------")
print("Temperature Difference:", difference, "°C")

# -------------------------------
# INSIGHTS AND RECOMMENDATIONS
# -------------------------------

print("\nInsights")
print("----------------------")

if difference > 3:
    print("Significant variation detected between APIs.")
    print("Recommendation: Verify API reliability or check update timings.")
else:
    print("Weather data from both APIs is mostly consistent.")

# -------------------------------
# FINAL SUMMARY
# -------------------------------

print("\nFinal Summary")
print("----------------------")
print(f"City: {city}")
print(f"OpenWeatherMap Temp: {temp1} °C")
print(f"WeatherAPI Temp: {temp2} °C")
print(f"Temperature Difference: {difference} °C")
```

# Prompt Analysis

## Effective Prompt Characteristics

| Feature            | Observation                                    |
| ------------------ | ---------------------------------------------- |
| Clarity            | Clearly specified task requirements            |
| Context            | Included API names and output requirements     |
| Technical Accuracy | AI generated valid Python syntax               |
| Readability        | Code was simple and understandable             |
| Usefulness         | Responses were directly applicable to projects |


# Comparative Evaluation

| Stage              | Prompt Quality | AI Response Quality | Accuracy | Practical Use |
| ------------------ | -------------- | ------------------- | -------- | ------------- |
| API Integration    | High           | High                | High     | Excellent     |
| Output Comparison  | High           | High                | High     | Excellent     |
| Insight Generation | Moderate       | Good                | Good     | Very Useful   |

# Reflection Note

The prompts designed for AI-assisted coding were effective because they clearly described the programming language, APIs, and expected outputs. Detailed prompts helped the AI generate accurate and reusable Python code.

The comparison prompts improved analytical capabilities by helping identify differences between API outputs. Insight-generation prompts demonstrated how AI can assist in decision-making and recommendations.

The prompts could be refined further by:

* Specifying exception handling requirements
* Adding database integration instructions
* Requesting visualization graphs for output comparison
* Including performance optimization requirements

## AI-Assisted Coding Workflow

![Image](https://images.openai.com/static-rsc-4/BJP6SFGYQD9Sgv4Wy9Aogn_eNZdRTKJdxAvhchu7C2AMsvPkbM9Mo_6vnDvRvsMHDlybz2Oq-mszba5sDvBwDDiYybCl6THPdGhKpeNNOwNM8OfxDjxll89WFlC_enRrwIqUFPV6c3WTelRZt4y-9lvXWx8I22Qr_xdwPv_thXXzh7DLT08YiC8USrgpYZWg?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/5CPTZSyl6bqEWQh_3WIFDKeLMD9Icg7OyFzbApB3_SSa0Q9Xc1vbEiXT-J-InFmwfLaX-SOzxInDGz0oao5_367JNADYlzfyO--U88eqpmrSQKi9MFe79Vc_Kn6LbrjTgOfMsZz2pJ2gI87XriF6gozCn8HSxujd5gJTcDgTYCxELCxFhh0K377MAAXhjbhe?purpose=fullsize)

# Conclusion

The experiment demonstrated how prompt engineering can effectively guide AI tools in software development tasks such as API integration, output comparison, and insight generation. Carefully framed prompts improve the accuracy, usefulness, and efficiency of AI-generated code, making AI-assisted coding highly beneficial for academic and real-world projects.

---

# Result

The prompts for AI-assisted project coding were designed and executed successfully. The AI-generated responses produced functional Python code, output comparisons, and meaningful insights for the project scenario.
 The corresponding Prompt is executed successfully.
