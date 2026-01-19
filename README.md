## Workaround Instructions for SaaS Workshop 

**Copy and Paste below commands into the workshop provided VS Code terminal**

```bash
sed -i 's/rds.AuroraPostgresEngineVersion.VER_15_4/rds.AuroraPostgresEngineVersion.VER_15_8/g' "/Workshop/aws-saas-tenant-usage-and-cost-attribution/saas-app-plane/product-review-service/cdk/lib/RdsPostgresConstruct.ts" && \
sed -i 's/"aws-cdk-lib": "2.154.1"/"aws-cdk-lib": "2.234.1"/g' "/Workshop/aws-saas-tenant-usage-and-cost-attribution/saas-app-plane/product-review-service/cdk/package.json" && \
cd "/Workshop/aws-saas-tenant-usage-and-cost-attribution/saas-app-plane/product-review-service/cdk/" && \
npm install aws-cdk@latest && \
cd "/Workshop/aws-saas-tenant-usage-and-cost-attribution/saas-app-plane/product-review-service/scripts/" && \
./deploy.sh 1
cd ../../../
```
