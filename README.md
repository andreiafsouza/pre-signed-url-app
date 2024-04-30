# React/NextJS Application to Upload files to S3 using pre signed URLs

![image](https://github.com/andreiafsouza/pre-signed-url-app/assets/80974585/2acd7caf-77ec-47e7-85ba-e1987475d11b)

## AWS Console Setup:

1. **Create a private S3 bucket with versioning enabled**
   
2. **Add CORS permissions**:
    ```json
    [
        {
            "AllowedHeaders": [
                "*"
            ],
            "AllowedMethods": [
                "PUT"
            ],
            "AllowedOrigins": [
                "*"
            ],
            "ExposeHeaders": []
        }
    ]
    ```
3. **Assign a policy or a role with full access to S3 and create an access key for that user. Save the ACCESS KEY and SECRET KEY.**

## Application Configuration:

1. **Create a `.env` file in the root directory and add the following values to the variables:**
    ```
    ACCESS_KEY=<access key created for the user>
    SECRET_KEY=<secret key created for the user>
    BUCKET_NAME=<the name of the bucket you created>
    REGION=<the region of the bucket you created>
    ```

2. **Ensure you have Node.js installed. If not, download and install it from [here](https://nodejs.org/).**

3. **Run `npm run dev` in the terminal.**

4. **Upload a file to S3!**
