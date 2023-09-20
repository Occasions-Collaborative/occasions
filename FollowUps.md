### As of 20 September, the vercel production seems to be working fine.

## Issues occurring in deployment.

### The website says:

```
500: INTERNAL_SERVER_ERROR
Code: EDGE_FUNCTION_INVOCATION_FAILED
ID: bom1::9dnwb-1694066765707-ec6245271774
```

### Logs at the deployment on Vercel say:

Function: /middleware

```
Error: either NEXT_PUBLIC_SUPABASE_URL and NEXT_PUBLIC_SUPABASE_ANON_KEY env variables or supabaseUrl and supabaseKey are required!
    at (node_modules/@supabase/auth-helpers-nextjs/dist/index.js:192:10)
    at (middleware.ts:10:42)
    at (node_modules/next/dist/esm/server/web/adapter.js:165:22)
    at (node_modules/next/dist/esm/server/async-storage/request-async-storage-wrapper.js:72:23)
    at (node_modules/next/dist/esm/server/web/adapter.js:152:52)
```

There are 12 logs of errors, consisting of favicon and middleware [extension: .ts].
Type of request: GET

### To resolve, check on the following:

https://vercel.com/docs/error/application/EDGE_FUNCTION_INVOCATION_FAILED
and the Deployment Runtime Logs at Vercel.
