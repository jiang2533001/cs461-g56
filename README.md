# Cs461-g56

# Project: 
Prototype Big Data Archive in a Public Cloud

# Group member: 
Zhi Jiang</br>
Isaac T Chan</br>
Zhaoheng Wang

# Client:
David Barber
# Responsibility:
Zhi Jiang: 
 * Load data from S3 into DynamoDB (Ingest and management of sample data)
 * Create table for DynamoDB
 
Zhaoheng Wang:
 * Design the table for DynamoDB
 * Design the workflow for loading new data
 * Create visualization on QuickSight (Rudimentary analysis,visualization)

Isaac T Chan:
 * Cost model for public cloud resources used
 * Test

# Environment:
The project is working on the Amazon Web services, so it requires you must have a AWS account and this account has permission to access our project.
    
# Instruction:
Instruction and Code can be found in Instruction and code folder

Load data from S3 into DynamoDB:
1. Go to AWS EC2 console and start `i-010e91199de2cf622` EC2 instance, then connect it
2. Open an SSH client. Locate your private key file ``osukeypair.pem``. Type command to connect this EC2 instance
3. After connecting into the EC2 instance, run the python file ``create.py`` for creating table
4. After creating tables, run the ``import.py`` for loading data
5. login in the DynamoDB and check the result on the console
6. Stop the EC2 instance on EC2 console

Save the result back to the S3:
1. anonymized record have been created after run the ``import.py``
2. It is stored in a certain bucket

Create visualization on the QuickSight
1. Open the QuickSight console on AWS 
2. Click New analysis button 
3. Choose New data set
4. Click upload a file and choose the csv file which export from the "Records" table
5. Using the data set and select the conlumn which need to evalaute.
6. Select the rows that need to evaluate and choose the visual types.
7. The visual will be created on right side.

# Introduction for project:
OSU campuses generate data constantly from multiples sources, including computer labs, wireless usage, student devices, and many others. This quantity of data, also known as big data, can effectively represent all kinds of behaviors of students for information technology. For example, analysis can be run to determine common student behaviors in order to allocate OSU resources more effectively. Currently, the data is very difficult to manage because it is collected from multiple sources and is impossible to analyze. The data is neither stored in the same formats nor in the same locations, meaning it is inaccessible and useful information is unable to be extracted.Our goal for this project is to unify and organize the data onto the consistent cloud platform of Amazon Web Services, which additionally provides utilities to manage and analyze. To achieve this, we plan to have a working prototype at the Engineering Expo that demonstrates the value of analyzing OSU big data and how the cost-to-value of our Amazon cloud solution compares to locally-hosted hardware. Our prototype will allow OSU big data to be analyzed and eventually it can be scaled to analyze all the data that OSU collects.
