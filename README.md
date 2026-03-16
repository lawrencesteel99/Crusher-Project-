# CrusherProject
Mining Equipment Downtime Analysis in Python
import pandas as pd

data = {
    "Machine": ["Crusher 1","Crusher 2","Crusher 1","Crusher 3","Crusher 2","Crusher 1"],
    "Downtime_hours": [5,2,3,4,1,6],
    "Failure_reason": ["Bearing","Belt","Overheat","Motor","Belt","Bearing"]
}

df = pd.DataFrame(data)

print(df)