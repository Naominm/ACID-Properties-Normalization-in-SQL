# Normalization
Normalization is a technique which is used to organize the data in the database. It is a systematic approach to remove the data redundancy. Normalization is mainly used for two purposes:

- To remove redundancy.

- Ensuring data dependencies is proper.

Without normalization anomalies occur and it become difficult to handle and update data.

 ### The 3 anomalies

 To understand these anomalies lets take a student table.

 |ID        | Name    |Address   |Subject
 | -------- | ------- |-------   |-------
 | 201      | Alice    |Nairobi  |Maths
 | 202      | Charles  |New york |Bio
 | 203      | Daniel   |kisumu    |Physics
 |204       |Eva       |Japan      |Maths

 ### Update Anomaly
 To update address of a student who occurs twice or more than twice in a table, we will have to UpdateAddress Column in all the rows, else data will become inconsistent.

 ### Insertion Anomaly
 Suppose for a new admission, we have a student Id, name and address of a student but if the student has opted for any subject yet we have to insertNULL there, leading to insertion Anomaly.

 ### Deletion Anomaly
 If id 401 has only one subject and temporarily he drops it, when we delete that row, entire student record will be deleted along with id.