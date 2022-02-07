# Results AWS Friday 04.02.2022

### 1
- go to console :) 

### 2
- To configure cli use `aws configure` and copy credentials from sandbox
- create bucket `super-test-bucket-21314` with `aws s3api create-bucket --bucket super-test-bucket-21314 --region us-east-1` see [docs](https://docs.aws.amazon.com/cli/latest/reference/s3api/create-bucket.html)
- Upload index.html with `aws s3 cp index.html s3://super-test-bucket-21314/index.html` see [docs](https://docs.aws.amazon.com/cli/latest/reference/s3/cp.html)
- Or upload public directly with acl `aws s3 cp index.html s3://super-test-bucket-21314/index.html --acl public-read`
- Make public `aws s3api put-object-acl --bucket super-test-bucket-21314 --key index.html --acl public-read` see [docs](https://docs.aws.amazon.com/cli/latest/reference/s3api/put-object-acl.html)
- Enable Website hosting with `aws s3 website s3://super-test-bucket-21314 --index-document index.html` see [docs](https://docs.aws.amazon.com/cli/latest/reference/s3/website.html)

### 3
- see [workflow](.github/workflows/deploy-website.yml)
