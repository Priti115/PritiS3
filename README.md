# AWS S3 Upload Project

This project demonstrates how to upload files to Amazon S3 using Python and a simple Streamlit web app. It includes both a command-line uploader and a browser-based interface for easier file uploads.

## What this project does
- Uploads files to an Amazon S3 bucket
- Supports both terminal-based and web-based usage
- Uses AWS credentials from a local environment file
- Includes a sample text file for testing

## Project structure
- [AWS_S3_Bucket/upload_to_s3.py](AWS_S3_Bucket/upload_to_s3.py) - command-line upload script
- [AWS_S3_Bucket/streamlit_app.py](AWS_S3_Bucket/streamlit_app.py) - Streamlit web app
- [AWS_S3_Bucket/app.py](AWS_S3_Bucket/app.py) - alternative Streamlit entry point
- [AWS_S3_Bucket/s3_utils.py](AWS_S3_Bucket/s3_utils.py) - reusable S3 helper functions
- [AWS_S3_Bucket/requirements.txt](AWS_S3_Bucket/requirements.txt) - Python dependencies
- [AWS_S3_Bucket/sample.txt](AWS_S3_Bucket/sample.txt) - sample file for testing

## Demo video
Watch the demo here:
- [Screen Recording 2026-07-01 095117.mp4](Screen%20Recording%202026-07-01%20095117.mp4)

## Prerequisites
- Python 3.9 or above
- An AWS account with permission to use S3
- An S3 bucket name
- AWS access key and secret access key

## Setup
1. Create and activate a virtual environment:
   - Windows:
     `python -m venv .venv`
     `.venv\Scripts\activate`
2. Install the required packages:
   `python -m pip install -r AWS_S3_Bucket/requirements.txt`
3. Create or update [AWS_S3_Bucket/.env](AWS_S3_Bucket/.env) with your AWS settings:
   ```env
   AWS_ACCESS_KEY_ID=your_access_key
   AWS_SECRET_ACCESS_KEY=your_secret_key
   AWS_REGION=us-east-1
   BUCKET_NAME=your-bucket-name
   ```

## Run the project
### Option 1: Command-line upload
Run:
```bash
python AWS_S3_Bucket/upload_to_s3.py AWS_S3_Bucket/sample.txt
```

### Option 2: Streamlit web app
Run:
```bash
streamlit run AWS_S3_Bucket/streamlit_app.py
```

## Notes
- The bucket name can be provided in the environment file or as a command-line argument.
- Keep your bucket private unless you intentionally want to share files publicly.
- For secure sharing, use pre-signed URLs instead of making objects public.

