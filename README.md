# AWS Amplify with Next.js SSR

Before deploying, check the app locally:

```
npm install
npm run dev
```

Test it: `http://localhost:3000/`

Create the DynamoDB table:

```
aws dynamodb create-table \
    --table-name MusicCollection \
    --region us-east-2 \
    --attribute-definitions AttributeName=Artist,AttributeType=S AttributeName=SongTitle,AttributeType=S \
    --key-schema AttributeName=Artist,KeyType=HASH AttributeName=SongTitle,KeyType=RANGE \
    --billing-mode PAY_PER_REQUEST
```

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
