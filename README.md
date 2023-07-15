# cloudformation-seed
# ロールを整える
[x] ロール設計(1h)
[x] ロール作成用のCloudformation作成(1h)
RoleArn: !Sub arn:aws:iam::${AWS::AccountId}:role/cloudformation-role
↑ ChangeSet差分確認ロール(調べる)
ロール名: cloudformation-role

---------------------
# S3
# ArtifactのS3作成(sample-codepipeline)
[x] Cloudformation作成(1h)
バケット名：sample-artifacts-${EnvName}

# CloudFrontのログのS3作成
Cloudformation作成(1h)
[x] cloudfront-access-logs.s3.amazonaws.com(cloudfront)
[x] samデプロイ用のS3バケット作成(codepipeline)

---------------------
## Code系
### CodePipeline
RoleArn: !Sub arn:aws:iam::${AWS::AccountId}:role/codepipeline-role
ロール名: codepipeline-role
[x] 作成
----------------------

# KMSの作成(CodePipeline+CodeCommit)
[x] KMSのCloudformation作成(1h)
[x] KMS作成(1h)

----------------------
### CodeCommit
[x] 調査(0.5h)
RoleArn: !Sub arn:aws:iam::[?????????]:role/codecommit-role  # TODO: 元となるAccount(灰色とか)ID
ロール名: codecommit-role
[x] Cloudformation作成(1h)
[x] ロール作成(1h)

### CodeBuildロール
[ ] ServiceRole: !Sub arn:aws:iam::${AWS::AccountId}:role/codebuild-role # TODO: codebuildロール
    ロール名: codebuild-role

----------------------

# KMSの作成
[x] KMSのCloudformation作成(1h)
[x] KMS作成(1h)

----------------------
# 全体Cloudformationの仮作成
[ ] 作成(1h)

----------------------
# CMSの作成
[ ] DNSで取得？

---------------------
# APIのLambda作成

