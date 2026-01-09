## AWS installation by conda
   micromamba create -n awscli conda-forge::awscli

## AWS configuration
   aws configure

   AWS Access Key ID [None]:
   AWS Secret Access Key [None]:
   Default region name [None]:ap-northeast-1
   Default output format [None]:json

## AWS check connection
   aws s3 ls s3://impdh-coe68/

## AWS create folder key
   aws s3api put-object --bucket your_bucket --key tissue/wgs

## AWS copy a file from your directory to bucket
   aws s3 cp file.txt s3://your_bucket/path/to/file.txt

## AWS download a file to your directory
   aws s3 cp s3://your_bucket/path/to/file.txt .

## AWS copy multiple files in subfolder
   aws s3 cp "path/to/your/directory" s3://your_bucket --recursive

## AWS delete a file
   aws s3 rm s3://your_bucket/path/to/file.txt
