# File Format Performance Comparison 

This project demonstrates how to measure and compare the performance of different file formats (CSV, Pickle, Parquet, Feather) in terms of read and write operations. It utilizes a generated dataset of 5 million records, each with a mixture of categorical, numerical, boolean, datetime, and floating-point columns.

## 📘 Overview

The code consists of two primary components:

1. **Data Generation and I/O Operations**: A dataset is generated with specific characteristics and then written to and read from disk using four different file formats. This process is timed to measure the performance of each file format.
2. **Visualization**: The measured times for read and write operations are visualized using horizontal bar charts, allowing for an easy comparison of performance across the file formats.

### Data Generation 📊

The dataset is generated with the following columns:
- `size`: Categorical column with values 'large', 'medium', 'small'.
- `age`: Integer column with values between 1 and 50.
- `team`: Categorical column with values 'red', 'white', 'blue', 'gold'.
- `win`: Boolean column with values True or False.
- `date`: Datetime column with dates ranging from 2021-01-01 - 2023-12-31.
- `prob`: Floating-point column with values between 0 and 1.

### I/O Operations and Timing ⏲️

The generated dataset is written to and read from disk using four different file formats:
- CSV
- Pickle
- Parquet
- Feather

The time taken for each read and write operation is measured using Python's `time` module.

### Visualization 👀

The measured times are visualized in two horizontal bar charts:
- The first chart shows the time taken for read operations across the different file formats.
- The second chart shows the time taken for write operations.

The charts use shades of red to distinguish between the times, with darker shades indicating longer durations.

<img src="https://github.com/joemcmullin/Data-read-write-speeds/assets/3474363/f5c401bf-c9df-4bfc-945e-109e50d325f9" width="50%"/>
</br>
<img src="https://github.com/joemcmullin/Data-read-write-speeds/assets/3474363/e18520d9-9c05-4f88-a0c7-686ac9b476ca" width="50%" />


## Dependencies →

- Python 3
- Pandas
- NumPy
- Matplotlib
- IPython

## How to Run 🏃🏻‍♂️

1. Ensure all dependencies are installed in your Python environment.
2. Copy the code into a Jupyter Notebook cell. Or just pull the Juypter Notebook. 🙂
3. Run the cell to execute the data generation, I/O operations, timing measurements, and visualization.

## Interpretation of Results 

The results provide insights into the efficiency of different file formats for read and write operations with a large dataset. Typically, binary formats like Pickle, Parquet, and Feather offer better performance compared to the text-based CSV format.

## Conclusion 👍🏼

This project showcases a practical approach to measuring the performance of various file formats in handling large datasets. The insights gained can inform decisions on choosing the appropriate file format for data storage and manipulation in data science and analytics projects.
