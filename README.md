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

## License
View [license information](https://www.apache.org/licenses/LICENSE-2.0) for the software contained in this image.

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
