# React Screenshot Test Example

The example is powered by two additional packages: `jest-puppeteer` and `jest-image-snapshot`.

Screenshot tests are usually used in integration tests, instead of unit test.

```
npm run test:integration
```

## How to use screenshot tests in pull requests

After you have made your change and run regular tests, do the following

1. Run `npm run test:integration`.
2. If success, nothing to do. Otherwise, continue.
3. You should get some image diff in `__test__/__image_snapshots__/__diff_output__`
   folder. Check if every difference is expected.
4. If unexpected thing found, go back to fix your code. Otherwise, save them to
   other place. You will need these diff in PR.
5. Run `npm run test:integration -- -u` to update screenshots, so your build pass
   CI checking.
6. Commit and make PR. Attach image diff you have saved.

[Example pull request](https://github.com/advclb/react-screenshot-test-example/pull/1)

If you are able to configure pipline, these diffs can be automatically generated
and attached into the PR.
