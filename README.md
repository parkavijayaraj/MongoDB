Answers:


1.Find all the topics and tasks which are thought in the month of October

db.zenclass.find({users : "students"},{topic : 1,task : 1}).pretty();

2.Find all the placement drives which appeared between 15 oct-2020 and 31-oct-2020

db. zenclass.find({ users: "student" },{ attendance: 0, topic: 0, task: 0, users: 0, codekata: 0 }).pretty()

3.Find all the placement drives and students who are appeared for the placement

db.zenclass.find({users : "students"},{placement_drives : 1}).pretty();

4.Find the number of problems solved by the user in codekata

db.zenclass.find({users : "students"},{codekata : 1}).pretty();

5.Find all the mentors with who has the mentee's count more than 15

db.zenclass.find({ mentee_count: { $gt: 15 } }).pretty();

6.Find the number of users who are absent and task is not submitted between 15 oct-2020 and 31-oct-2020

db.zenclass.find({users : "students"},{attendance :{ $elemMatch : {status : "A"}}},{task : { $eq : { task : "false" }}}).pretty();
