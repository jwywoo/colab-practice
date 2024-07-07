# Jeju Island Weather Forecast Crawling & Preprocessing

## Goal

1. Getting daily forecast data from [Jeju Datahub](https://www.jejudatahub.net/)
2. Pre-process retrieved data for prediction model

## Data Format

| 항목  | 관측소명            | 날짜       | 평균기온               | 최저기온              | 최저기온시간대               | 최고기온               | 최고기온시간대                | 일일강수량         | 최대풍속             |최대풍속시간대|평균풍속|최대풍속방향|
|-------|-----------------|----------|--------------------|-------------------|-----------------------|--------------------|------------------------|---------------|------------------|------------------|------------------|------------------|
| 이름    | observatoryName | baseDate | averageTemperature | lowestTemperature | lowestTemperatureTime | highestTemperature | highestTemperatureTime | dailyRainfall | maximumWindSpeed |maximumWindSpeedTime|averageWindSpeed|maximumWindSpeedDirection|
| 샘플 | 중문              | 20140101 | 9.1000             | 6.0000            | 2052                  | 13.2000            | 1348                   | 0.0000        | 5.2000           |1246|1.6000|316.3000|

## Time range

2014/01/01 ~ 2024/06/30

## Missing value strategy

Replace missing values with neighbor values

### Data preprocessing strategy

1. Get daily weather forecast within a time range
2. Missing value handling and get avg of cols
3. Turn it into different csv files based on the location
    1. 제주시.csv - rows - baseDate, cols - anything else
