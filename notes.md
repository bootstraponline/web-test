# Playwright Test

https://github.com/microsoft/playwright-test

- https://www.npmjs.com/package/npx
- https://www.npmjs.com/package/@playwright/test

- `npm install -g npx`
- `npm install -D @playwright/test-runner`
- `npm install -g @playwright/test-runner`
- `npm install -g @playwright/test`
- `npm i -D @playwright/test`
- `npm i -D @playwright/test-runner`

`npx test-runner --browser-name=chromium`

See the [upstream issue](https://github.com/microsoft/playwright-test/issues/137) about making `test-runner` a dependency.

npx test --browser-name=chromium

# Sauce CTL

- `npm i -g saucectl`
https://github.com/saucelabs/testrunner-toolkit

- `echo $SAUCE_USERNAME`
- `echo $SAUCE_ACCESS_KEY`

`saucectl new`

`saucectl run`

# Docker

https://github.com/saucelabs/sauce-playwright-runner

`docker pull saucelabs/stt-playwright-jest-node:latest`


docker run --env SAUCE_USERNAME --env SAUCE_ACCESS_KEY -d --name=testrunner saucelabs/stt-playwright-jest-node:latest

docker cp ./tests/test.spec.ts testrunner:/home/seluser/tests

docker exec -it testrunner /bin/bash
# note ~/.sauce dir doesn't exist in the published image
# copy .yml file from https://github.com/saucelabs/sauce-playwright-runner/blob/master/config.yaml
#
# failed to locate job configuration: open /home/seluser/.sauce/config.yml: no such file or directory
docker cp ./config.yml testrunner:/home/seluser/.sauce/

docker exec testrunner saucectl run /home/seluser/tests

