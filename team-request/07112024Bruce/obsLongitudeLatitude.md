# Observatory Longitude & Latitude

| 항목  | 관측소명            | 경도       | 위도                |
|-------|-----------------|----------|--------------------|
| 이름    | observatoryName | longitude | latitude |
| 샘플 | 중문              | 126.4061 | 33.2495 |

```python
import pandas as pd 
import os

file_path = os.path.join('path')
df = pd.read_csv(file_path,'observatoryLongitudeLatitude.csv')
# 상위 10개 출력
print(df.head())
# csv 어떻게 생겼는지 출력
print(df.describe())

# Data frame iteration
for index, row in df.iterrows():
    print(index, row['observatoryName'], row['longitude'], row['위도'])

# 0 중문 126.4061 33.2495
# 1 .......
```
