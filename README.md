# Python-Dataframe
import pandas as pd
data = {
    'Name': ['Rasheed', 'Ahmad ', 'Sajawal', 'Ali', 'Abbas'],
    'Age': [25, 32, 28, 40, 35],
    'Department': ['HR', 'Finance', 'IT', 'HR', 'Finance'],
    'Salary': [50000, 60000, 55000, 65000, 70000]
}
df = pd.DataFrame(data)
print("Original DataFrame:\n", df)
filtered_df=df[df['Age'] > 30]

print("\nEmployees Older than 30:\n",filtered_df)
mean_salary_by_department=df.groupby('Department')['Salary'].mean()
print("\nMean Salary by Department:\n", mean_salary_by_department)
df['Bonus'] =df['Salary'] * 0.10
print("\nDataFrame with Bonus Column:\n", df)
df['Total Saly of this mo'] = df['Salary'] + df['Bonus']
print("\nDataFrame with Total Compensation (Salary + Bonus):\n", df)
