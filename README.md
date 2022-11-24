# Data-Processing-for-Energy-Consumption-and-PV
****Project Goal:****
Finding the energy consumption and power consumption for 58 houses in the building from the sensor energy metric data of a building by applying the relevant electrical formulas on the data. The converted data will then be used to calculate the building's total power and energy consumption.

Since the Returned Low and Pv measurements are not at the same minute, I put the dates of the returned low between the pv data to align the signals, and predict what the pv will be at that minute and hour using scipy.interpolate.BPoly.from_derivatives using a piecewise polynomial. I also found these values ​​with the ffill method. And as the real pv signal, I used the average of these 2 signals according to certain situations.

![Comparsion of Interpolation Methods](https://user-images.githubusercontent.com/76845631/203826104-089c9d2d-d7fc-4241-8918-5f2d71489880.png)

![Both](https://user-images.githubusercontent.com/76845631/203828380-10bf607b-ed34-4fb7-b44f-671239c79d09.png)

![pv retlow](https://user-images.githubusercontent.com/76845631/203830982-849317d0-c6e7-417f-80fa-b8665a3b12b9.png)



****Project Steps:****

1 - Filtering 70 million rows of data to 10 million rows to speed up data processing.

2 - Data Processing Steps (Logical operations - Time Series Operations)

3 - Finding increment between Watt/Hour Measurements.

4 - Finding time differences between measurements.

5 - Clearing inaccurate measurements between measurements.

6 - Adjusting the frequency of the data so that it is suitable for use in the formula.

7 - Finding energy consumption with appropriate electric formula.

8 - Calculation of power and energy consumption values ​ for 58 different houses in 15-minute intervals for 1 year. 

9 - Dynamic visualization of results.

![Sensor Data Pipeline (2)](https://user-images.githubusercontent.com/76845631/197052584-1bb25e0e-0e09-42de-8ad9-42b867e9ece5.png)


