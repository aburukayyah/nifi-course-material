Download the template and upload into NiFi instance

Before running the template, it is important to create files in a directory `/home/nobleprog/Documents`

```shell
# change directory
$ > cd /home/cloud/Desktop

# create directories if does not exist
$ > mkdir -p get-file put-file

# change directory to get-file
$ > cd get-file

# create file
$ > echo "Hello from NiFi" > data.txt
```

### Configuring Processors

***GetFile***

| Name | Value |
| ---- | ----- |
| Input Directory | `/home/nobleprog/Documents/get-file` |

***PutFile***

| Name | Value |
| ---- | ----- |
| Input Directory | `/home/nobleprog/Documents/put-file` |

