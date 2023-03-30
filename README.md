# AWS Amplify with Next.js SSR

Before deploying, check the app locally:

```
npm install
npm run dev
```

Test it: `http://localhost:3000/`

For the cloud, set your repository key as a `$token` variable, and create the Amplify app:

```
aws amplify create-app \
  --name nextssr \
  --region us-east-2
  --repository "https://github.com/epomatti/aws-amplify-nextjs-ssr" \
  --access-token $token

aws amplify create-branch \
  --app-id <appid> \
  --branch-name main
```

Access the SSR application running on the cloud.
