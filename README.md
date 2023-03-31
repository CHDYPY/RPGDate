# RPGDate

The peer assessment dataset was used in our paper, **抽查设定下评分偏差感知的同行互评概率图模型**

## Background and Source

This peer assessment dataset was collected from a self-developed teaching service system. The data comes from peer assessment assignments given by teachers to students in three real courses: "Database Principles," "Data Structures," and "Computer Networks." Each assignment only includes one open-ended question with a maximum score of 10 points. In all peer assessment assignments, each student who submitted an assignment participated as a peer assessor to evaluate three other submitted assignments based on the peer assessment criteria provided by the teacher, ensuring that each submitted assignment has three peer assessment scores. All peer assessment activities are double-blind, and both peer assessors and those being evaluated do not know each other's identities. To obtain the true scores of all peer assessment records in the dataset, two experienced teachers with six years of teaching experience strictly scored all peer assessment records according to the scoring criteria, and the scores given by these two teachers are considered as the true scores of the records.

## Structure



The columns in this dataset are:

- HomeworkID
- GraderUserID
- GradeeUserID
- peerGrade
- teacherGrade

You can import this dataset in Python using the following code:

```python
import csv

def readFile(fileName, dataName):
    with open(fileName, encoding='UTF-8') as csvFile:
        reader = csv.reader(csvFile)
        for line in reader:
            dataName.append(line)
        del dataName[0]
        
data_experiment_1 = []
readFile('experimentGroup_1.csv', data_experiment_1)
```



