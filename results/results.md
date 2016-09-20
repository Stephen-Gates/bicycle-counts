#Results
Use the links below to perform the tests using Good Tables.

## Test using valid data and no schema
- [Test Active-Transport-Sites.csv without a schema]()
- [Test averagebicyclecountsbydayandhour.csv without a schema]()


## Test using valid data with its schema
- [Test Active-Transport-Sites.csv with a schema]()
- [Test averagebicyclecountsbydayandhour.csv with a schema]()


## Test using invalid data and its schema
- [Test an invalid Active-Transport-Sites.csv with a schema]()
- [Test an invalid averagebicyclecountsbydayandhour.csv with a schema]()


## Good Tables issues
- Good Tables supposedly has a 100,000 row limit (see [goodtables-web #54](https://github.com/frictionlessdata/goodtables-web/issues/54)) but it appears to be [limited to 30,000*](https://github.com/frictionlessdata/goodtables-web#api)
- Good Tables only returns a [limited number of errors](https://github.com/frictionlessdata/goodtables-web/issues/66) so the [test data](https://github.com/Stephen-Gates/GTFS/tree/master/tests) will need to be split into smaller sets.
- Good Tables doesn't use the primary key to check for duplicates ([see goodtables-web #64](https://github.com/frictionlessdata/goodtables-web/issues/64))
- Good Tables doesn't handle optional uri fields (see [goodtables #109](https://github.com/frictionlessdata/goodtables/issues/109))
- view other [goodtables-web](https://github.com/frictionlessdata/goodtables-web/issues) and [goodtables](https://github.com/frictionlessdata/goodtables/issues) issues
