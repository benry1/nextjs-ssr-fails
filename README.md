This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app). This is to be deployed to AWS via [`sst`](https://sst.dev).

Only modifications were:
1. Removed most of the content from Index (for simplicity)
2. Added a Hello World `getServerSideProps` function

## The Problem

Simplest-case Serverside Rendering does not work when deployed with SST. It will always throw a 500, and render a page that says "Internal Server Error"

## To Reproduce

Notice you can run the app normally, using `npx next`.

Then, deploy it via SST:

`npx sst deploy --stage test`

You should see output like this:

```
✔  Deployed:
   Site
   SiteUrl: https://unique-url.cloudfront.net
```

Go to your unique URL and observe the error.