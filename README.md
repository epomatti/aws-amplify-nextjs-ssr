# aws-amplify-nextjs-ssr

Set your repository key as a `$token` variable.

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

