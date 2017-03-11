## Testing locally

Number 1, do

```bash
npm install express
```

Number 2, do

```bash
coffee -e 'a=require("express")(); a.use(require("express").static(__dirname)); a.listen(5000);'
```

This will serve the directory to port 5000

## Updating

Number 1, change the files.

Number 2, run the following command

```bash
aws --profile=perceptionz s3 sync . s3://static.itinerantfoodie.com --region ap-northeast-2 --exclude '.DS_Store' --exclude 'node_modules/*' --exclude '.git/*' --exclude '.gitignore' --acl public-read
```
