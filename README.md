# Ansible playbook for Exoscale S3

Ansible playbook which demonstrates how to use s3 operations on Exoscale:

- create a temporary file of size `file_size` (default: 15M)
- create a bucket on exoscale s3
- upload the temporary file to the bucket
- download the temporary file through a classic public url
- download the temporary file through the pre-signed url
- delete the file in the bucket
- delete the bucket
- validate both download signatures against the original file


To run the playbook:
```
export AWS_ACCESS_KEY=...
export AWS_SECRET_KEY=...
ansible-playbook exoscale-s3.yml
```

If you wish to overwrite one or more variables, for example with a bigger file:
```
ansible-playbook exoscale-s3.yml -e "file_size=1G"
```
