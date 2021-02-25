##Run this ARM template with az CLI

$password="P@ssword1" | ConvertTo-SecureString -AsPlainText -Force

az deployment sub create --name demoSubDeployment --location centralus --template-file azuredeploy3.json --parameters resourceGroup_name=demoResourceGroup resourceGroup_location=centralus workspaceName=demopfeborges pricingTier=standard enableNoPublicIp=true deployment_Name=deploydemopfeborges administratorLogin=roberto administratorLoginPassword=$password serverName=demosvborges elasticPoolName=poolbborges edition=Basic capacity=50 databaseCapacityMin=5 databaseCapacityMax=5 databaseCollation=SQL_Latin1_General_CP1_CI_AS databasesNames="['db1', 'db2']"

