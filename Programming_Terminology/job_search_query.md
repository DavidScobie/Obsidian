The key details of the jobs not applied to:
```dataview
TABLE WITHOUT ID
file.inlinks AS "Title",
file.link AS "Company",
Rating,
Location,
Expired,
Notes,
Applied,
Status
FROM #jobs/advertisement 
SORT Rating DESC
WHERE (Applied = "no") AND (Expired != "yes") AND (Expired != "Yes")
```

The jobs that I'm waiting to hear back from:
```dataview
TABLE WITHOUT ID
file.inlinks AS "Title",
file.link AS "Company",
Rating,
Location,
Expired,
Notes,
Applied,
Status
FROM #jobs/advertisement 
SORT Rating DESC
WHERE (Applied != "no") AND (Status = "Waiting")
```
These jobs have responded positively:
```dataview
TABLE WITHOUT ID
file.inlinks AS "Title",
file.link AS "Company",
Rating,
Location,
Expired,
Notes,
Applied,
Status
FROM #jobs/advertisement 
SORT Rating DESC
WHERE (Applied != "no") AND (Status != "Waiting") AND (Status != "Rejected")
```

These jobs have rejected me:
```dataview
TABLE WITHOUT ID
file.inlinks AS "Title",
file.link AS "Company",
Rating,
Location,
Expired,
Notes,
Applied,
Status
FROM #jobs/advertisement 
SORT Rating DESC
WHERE Status = "Rejected"
```