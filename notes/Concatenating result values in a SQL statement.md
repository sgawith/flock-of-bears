# Concatenating result values in a SQL statement
When using postgreSQL, you can use the array_agg method to get all row values for a specific field as an array:

```
SELECT ocu.ocucode, array_agg(resourcegroup.resourcegroupcode) AS groups 
FROM ocu, resourcegroup 
WHERE resourcegroup.ocuid=ocu.ocuid 
GROUP BY ocu.ocucode 
ORDER BY ocu.ocucode ASC
```

You can then string these together to get multiple comma-separated lists in a single result:

```
SELECT ocu.ocucode, ocu.ocudescription, cadqueues.queues, resourcegroups.groups 
FROM ocu, 
		(
			SELECT ocu.ocucode, array_agg(cadqueue.cadqueuecode) AS queues 
			FROM ocu, cadqueue 
			WHERE cadqueue.ocuibd=ocu.ocuid 
			GROUP BY ocu.ocucode
		) AS cadqueues,
		(
			SELECT ocu.ocucode, array_agg(resourcegroup.resourcegroupcode) AS groups 
			FROM ocu, resourcegroup 
			WHERE resourcegroup.ocuid=ocu.ocuid 
			GROUP BY ocu.ocucode
		) AS resourcegroups
WHERE cadqueues.ocucode = ocu.ocucode 
AND resourcegroups.ocucode = ocu.ocucode
ORDER BY ocu.ocucode
```

Unfortunately, this only returns results which have both lists populated. To return mixed results, use this one:

```
SELECT ocu.ocucode, array_agg(groupsandqueues.cadqueuecode) AS cadqueues, array_agg(groupsandqueues.resourcegroupcode) AS resourcegroups
FROM ocu, 
(SELECT ocuid, resourcegroupcode, '' AS cadqueuecode
FROM resourcegroup
UNION
SELECT ocuid, '' AS resourcegroupcode, cadqueuecode
FROM cadqueue) AS groupsandqueues
WHERE ocu.ocuid = groupsandqueues.ocuid
GROUP BY ocu.ocuid
ORDER BY ocu.ocucode
```

#sql #postgres