# HOWTO:  interact with files using minio with docker and docker-compose
par Thomas Ragot
2018-02-22

## Requirements
have docker and docker-compose installed on your computer or server


## Run the demo 

### Step - prepare env file

- make a copy name .env of the .env.example file. 

- fill the MINIO_DATA_ROOT_DIR variable with the absolute path to the wanted root folder for the data
- choose some access and secret key and fill MINIO_ACCESS_KEY and MINIO_SECRET_KEY

### Step - run containers.
at the root of the directory, run :
`docker-compose up -d`

### Step - check everything is correct and give it a try
- MINIO_DATA_ROOT_DIR dir should be filled  a dir test-bucket containing a file myfile.txt 
- by using the web interface (http://localhost:9000 if you runned the containers on your computer)
you should be able to add buckets and file and have it persisted in MINIO_DATA_ROOT_DIR

### remove the containers (but not the data)
at the root of the directory, run :
`docker-compose down`

