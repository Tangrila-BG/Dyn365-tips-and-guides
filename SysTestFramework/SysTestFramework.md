# The SysTestFramework helps you make tests

## Data in tests

The while executing tests the SysTest Framework has its own state of the current database and cannot see the records in it by default, except the ones created during the test execution. So you need to setup your dependent data before running the test or in it, but before accessing it.