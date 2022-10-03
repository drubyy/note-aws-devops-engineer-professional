# note-aws-devops-engineer-professional
### CodeCommit
 - connect: Sử dụng https hoặc ssh
   + Không thể sử dụng được ssh đối với root account
   + Có thể sử dụng HTTPS đối với root account nhưng NOT RECOMMENDED
   + Nên sử dụng IAM user để connect
<hr/>

### CodeBuild
 - What: Code build được sử dụng với mục đích build, test version code nào đó
 - Environment variables: Có 3 dạng
   + Plain text: Dạng string thường
   + SSM
   + Secret manager
 - Artifact: Là đầu ra của codebuild sau khi CodeBuild thực hiện build code => sẽ được lưu trữ ở đâu đó, vd như S3
<hr/>
