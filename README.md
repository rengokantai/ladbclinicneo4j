# ladbclinicneo4j

## 2. Create a Database
### 4 Create a database
example
```
CREATE (c:County {name:"ke"})<-[:FOR_COUNTY]-(p:PopulationPrediction{population:10000,year:2017,gender:"Male",age:33})
```
```
MATCH(c) DETACH DELETE c;
```

### 5. Query data
```
MATCH (c:Country) WHERE c.name = "ke" RETURN c;
```
extend:
```
MATCH(c:Country)<-[:FOR_COUNTY]-(p:PopulationPrediction) WHERE c.name='ke' RETURN COUNT(p);
```



```
LOAD CSV WITH HEADERS FROM "file://a.csv" AS row RETURN row LIMIT 5
```
