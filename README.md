# tap-xunit
tap-xunit in a can

## What is this thing?
This docker image is simply just [tap-xunit](https://www.npmjs.com/package/tap-xunit). This is meant to be used in cicd environments that don't support native tap files but do support xunit, such as [circleci](https://circleci.com/docs/2.0/collect-test-data/#ava-for-nodejs).

## How do I use it?
```
docker run -i hypergig/tap-xunit <  test_results.tap | tee test_results.xml
```
or if you want to skip a step you can just pipe it...
```
bats -t my_test.bats | docker run -i hypergig/tap-xunit | tee test_results.xml
```
