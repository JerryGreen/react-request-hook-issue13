# react-request-hook issue13

This is a minimal project setup to reproduce [the issue](https://github.com/schettino/react-request-hook/issues/13)

The steps to reproduce:

```bash
mkdir react-request-hook-issue13
cd react-request-hook-issue13

git clone git@github.com:schettino/react-request-hook.git
cd react-request-hook
yarn
yarn build
yarn link
cd ..

git clone git@github.com:JerryGreen/react-request-hook-issue13.git test-project
cd test-project
yarn
yarn link react-request-hook
yarn start
```

But if you do this, it will work perfectly:

```bash
yarn unlink react-request-hook
yarn install --force
yarn start
```

Again, make a link, and it will break:

```bash
yarn link react-request-hook
yarn start
```
