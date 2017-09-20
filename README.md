# ladbclinicneo4j

## 2. Create a Database
### 4 Create a database
example
```
CREATE (c:County {name:"ke"})<-[:FOR_COUNTY]-(p:PopulationPrediction{population:10000,year:2017,gender:"Male",age:33})
```
