# CrusherProject
#Mining Equipment Downtime Analysis in Python
import pandas as pd

data = {
    "Machine": ["Crusher 1","Crusher 2","Crusher 1","Crusher 3","Crusher 2","Crusher 1"],
    "Downtime_hours": [5,2,3,4,1,6],
    "Failure_reason": ["Bearing","Belt","Overheat","Motor","Belt","Bearing"]
}

df = pd.DataFrame(data)

print(df)

downtime_by_machine = df.groupby("Machine")["Downtime_hours"].sum()

print(downtime_by_machine)

failure_counts = df["Failure_reason"].value_counts()

print(failure_counts)

import matplotlib.pyplot as plt

downtime_by_machine.plot(kind="bar")

plt.title("Crusher Downtime Analysis")
plt.ylabel("Downtime Hours")
plt.xlabel("Machine")

plt.show()

data = {
"Machine":["Crusher 1","Crusher 2","Crusher 3","Crusher 1","Crusher 2","Crusher 3","Crusher 1","Crusher 2"],
"Downtime_hours":[5,2,4,6,1,3,7,2],
"Failure_reason":["Bearing","Belt","Motor","Bearing","Belt","Overheat","Bearing","Belt"],
"Shift":["Day","Night","Day","Night","Day"]
}