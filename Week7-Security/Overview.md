
## AWS Security Service :Credit @vikas Sharma

![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/6ac04a8e-b149-4841-9878-6fb82212815d)

## What is SQL Injection ?

- SQL injection is a code injection technique that might destroy your database.
- SQL injection is one of the most common web hacking techniques.
- SQL injection is the placement of malicious code in SQL statements, via web page input.
  
Ref : https://www.w3schools.com/sql/sql_injection.asp
# Example :
----------------------------------------------------------------------------------------------------
txtUserId = getRequestString("UserId"); \

txtSQL = "SELECT * FROM Users WHERE UserId = " + txtUserId; \

------------------------------------------------------------------------------------------------------

![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/bca456ef-8f7d-4f3e-81b7-d4e96c84bea1)

-------------------------------------------------------------------------------------------------------------------------------

![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/44846917-6ea1-4358-a63f-84b6c889762a)

--------------------------------------------------------------------------------------------------------------------------------
## What is NTP amplification attack

An NTP amplification attack is a type of Distributed Denial of Service (DDoS) attack. In this attack, the attacker uses publicly accessible Network Time Protocol (NTP) servers 
to overwhelm a target system with UDP traffic. NTP is used by machines connected to the Internet to set their clocks accurately.

In an NTP amplification attack, the attacker sends short requests to an open NTP server. The response from the NTP server is dozens of times larger than the request. 
This is called the amplification effect. 

Check

