# NYC_cab_analysis

NYC Taxi Data Analysis

Objective & Problem Statement:
The objective of this project was to analyze NYC taxi ride data from the airport to uncover insights into ride patterns, fare distribution, and overall trends. The project addressed the challenge of efficiently processing and analyzing large datasets to derive meaningful conclusions.

Tools & Technologies Used:
I primarily used Python, leveraging the NumPy library to handle and analyze the dataset.

Process & Methodology:
I began by loading the dataset using NumPy's genfromtxt function, which allowed me to skip the header and work directly with the data. My approach included calculating the mean speed of the taxis, determining the number of rides that occurred in February, and identifying the number of rides where the distance traveled was greater than 50 miles. The methodology was straightforward, utilizing NumPy's powerful array operations to perform these calculations efficiently.

Here is a code snippet demonstrating this process:

import numpy as np
file_path = '/Users/aqsa/Desktop/nyc_taxis.csv'

taxi = np.genfromtxt(file_path, delimiter=',', skip_header=True)
print(taxi)
speed = taxi[:, 7] / (taxi[:, 8] / 3600)
mean_speed = speed.mean()
print("Mean value:", mean_speed)
rides_feb = taxi[taxi[:,1] == 2,1]
print("Number of rides in February:", rides_feb.shape[0])
print(taxi[taxi[:,-3] > 50, -3].shape[0])
print(taxi[taxi[:,6] == 2,6].shape[0])

Challenges:
One challenge I faced was handling the large dataset efficiently without running into memory issues. I overcame this by focusing on the specific columns of interest, which helped reduce memory usage and improved processing speed.

Results & Impact:
The analysis provided insights into the average speed of taxis, the number of rides during February, and the frequency of long-distance rides. These results could help in understanding peak times, fare patterns, and potential areas for improving taxi services in NYC.

Lessons Learned & Future Directions:
This project enhanced my ability to work with large datasets using NumPy and deepened my understanding of data analysis in Python. In the future, I plan to expand this project by incorporating data visualization tools to present the insights more effectively and exploring machine learning models to predict ride patterns.

Reflection & Personal Experience:
This project was instrumental in advancing my technical skills and provided valuable experience in handling real-world datasets. It aligns with my broader career goals in data science and analytics, particularly in urban planning and transportation analysis.

link to project: https://github.com/aqsa75/NYC_cab_analysis
