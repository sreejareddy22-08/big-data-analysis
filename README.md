# Big Data Analysis

*COMPANY*: CODETECH IT SOLUTIONS

*NAME*: SREEJA

*INTERN ID*: CT06WL92

*DOMAIN*: DATA ANALYSIS

*DURATION*: 6 WEEKS

*MENTOR*: NEELA SANTHOSH

# description of task
Gain a solid knowledge of vital Data Analytics concepts via practical use cases
Created elegant data visualizations using Jupyter
Run, process, and analyze large chunks of datasets using PySpark
Utilize Spark SQL to easily load big data into DataFrames
Created fast and scalable Machine Learning applications using MLlib with Spark
Perform exploratory Data Analysis in a scalable way
Achieve scalable, high-throughput and fault-tolerant processing of data streams using Spark Streaming
Downloading data
The Docker Image bundled with this course (see Dockerfile) is based on the pyspark-notebook, distributed and maintained by Jupyter

Github link Original copyright (c) Jupyter Development Team. Distributed under the terms of the Modified BSD License.

This task Docker image extends the pyspark-notebook with the following additions:

enables Jupyter Lab by default
exposes correct ports for JupyterLab and SparkUI
sets numerous default settings to improve Quality of Life for the user
installs numerous add-ons (such as pyspark-stubs and blackcellmagic) using jupyter_contrib_nbextensions
Instructions for use
There are 2 ways to access the Docker container in this :

Through the bundled run_me.py script (recommended to use)
Through the Docker CLI (only for advanced users)
Using the bundled script to run the container
The easiest way to run the container that belongs to this task is by running python run_me.py from the task repository. This will automatically build the Docker image, set up the Docker container, download the data, and set up the necessary volume mounts.

Using Docker CLI
If you rather start the Docker container manually, use the following instructions:

Download the data

python download_data.py
Build the image

docker build --rm -f "Dockerfile" -t mastering_pyspark_ml:latest .
Run the image Ensure that you replace /path/to/mastering_pyspark_ml/repo/ in the following command, and run it in a terminal or command prompt:

docker run  -v /path/to/mastering_pyspark_ml/repo/:/home/jovyan/ --rm -d -p 8888:8888 -p 4040:4040 --name mastering_pyspark_ml mastering_pyspark_ml .
Open Jupyter lab once Docker image is running Navigate to http://localhost:8888/lab

To Stop the Docker Image
Once you are ready to shutdown the Docker container, you can use the following command:

docker stop mastering_pyspark_ml

