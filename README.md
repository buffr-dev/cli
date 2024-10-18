This is a repo with a sample docker compose file for using S3 on your local machine. Save on AWS costs and do not hook up to production when you're just developing!

# Usage

1) Install Docker CLI
2) Clone this repository
3) Set .env variables to something that makes sense for your project. Reference them in your client code to connect to the bucket
4) Run `$ docker compose up`. This will:
   - a) Download the minio image if needed
   - b) Startup a minio container
   - c) Create a bucket using the given .env variables

**Note**: This configuration uses a file-backed s3 store. All uploaded files will be persisted to a minio-data folder. To save disk space, you can delete this when finished. Otherwise, the files will be available for you when you restart the container.