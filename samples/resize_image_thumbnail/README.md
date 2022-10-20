## Resources:
  - Lambda (function + layer)
  - S3
  - Cloudwatch
  - IAM

## Steps
  1. Create buckets for upload origin images and put images has been process S3 (etc drubyy-origins and drubyy-thumbs)
  2. Upload lambda layer with zip (at folder layers)
  3. Upload function lambda
  4. Attach lambda layer to function
  6. Create event (create object) at S3 bucket origin and choose function lambda to trigger
  5. Upload some image to bucket drubyy-origins
  6. Check bucket druby-thumbs

  NOTE: if wanna test, use this test data: (replace with your correct data)
  ```
  {
    "Records": [
      {
        "eventVersion": "2.1",
        "eventSource": "aws:s3",
        "awsRegion": "ap-southeast-1",
        "eventTime": "2022-10-20T08:45:20.245Z",
        "eventName": "ObjectCreated:Put",
        "userIdentity": {
          "principalId": "AWS2LVJ0JVU0G"
        },
        "requestParameters": {
          "sourceIPAddress": "221.133.18.67"
        },
        "responseElements": {
          "x-amz-request-id": "6244D7VD6M4PBP3E",
          "x-amz-id-2": "uhcX0rR5gzeykMUatbjhCXr+HI/Dpu+/T9jlI1oaNiz4F1vdtbTnURCgrK2xC/6B5K+PZf2Kkon6wiGeQPAp1KPKyuwvum11"
        },
        "s3": {
          "s3SchemaVersion": "1.0",
          "configurationId": "thumbnailEvent",
          "bucket": {
            "name": "drubyy-lambda",
            "ownerIdentity": {
              "principalId": "AWS2LVJ0JVU0G"
            },
            "arn": "arn:aws:s3:::drubyy-lambda"
          },
          "object": {
            "key": "Screenshot+from+2022-10-19+11-53-49.png",
            "size": 762615,
            "eTag": "603824ea62c7c018feae874fdb690c39",
            "sequencer": "0063510AA02B105E8A"
          }
        }
      }
    ]
  }
  ```