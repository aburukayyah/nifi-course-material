Download the template and upload into NiFi instance

### Configuring Processors

***GenerateFlowFile*** 


Dynamic Properties

| Name | Value |
| ---- | ----- |
| `dynamodb.item.hash.key.value` | `6522` |

***PutDynamoDB***

| Name | Value |
| ---- | ----- |
| Table Name | `nifi-test` |
| Hash Key Name | `id` |
| Json Document attribute | `data` |
| Region | `US East (N. Virginia)` |
| Access Key ID | `access id` |
| Secret Access Key | `secret key` |