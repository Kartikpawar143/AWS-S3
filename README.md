# Static Website Hosting Using AWS S3
# Step 1:

-Sign in to the "AWS Management Console".

![Screenshot 2025-01-11 214628](https://github.com/user-attachments/assets/8e1d58e6-4de5-44e8-81e6-78d77968716a)

# Step 2: 

-Navigate to the S3 service by searching for "S3" in the AWS Management Console search bar.

![Screenshot 2025-01-11 214650](https://github.com/user-attachments/assets/c4a76fe7-e905-4414-8848-fa2aaabd0b02)


 # Step 3:  

-Click on the "Create bucket" button to start the bucket creation process. 

![Screenshot 2025-01-11 214736](https://github.com/user-attachments/assets/812bf5bd-bf13-4633-a555-9dab66e4939f)



# Step 4:

-Provide a unique name for your bucket. This name will be part of the website URL, so it should be globally unique.

-Choose the region where you want your bucket to be located.  

![Screenshot 2025-01-11 214916](https://github.com/user-attachments/assets/4ce93568-98fa-4fd1-baeb-634d8f3331f9)

-Leave all other settings as their default values and click on the "Create" button to create the bucket.

![Screenshot 2025-01-11 214846](https://github.com/user-attachments/assets/32bb3666-61c9-44b9-b0ff-95b678bd244c)


# Step 5: 

-Your Bucket is Successfully Created.

![Screenshot 2025-01-11 214927](https://github.com/user-attachments/assets/4d74c493-5a88-416e-be50-0107b5f2b87b)

-Navigate to bucket "Properties"

![Screenshot 2025-01-11 215020](https://github.com/user-attachments/assets/39805d72-3d10-4e6f-9ec8-fbb9ab994df8)

-Under "Static website hosting," click on the "Edit" button. 

![Screenshot 2025-01-11 215054](https://github.com/user-attachments/assets/cc5ed5f4-e49b-47b0-a852-503d805979d8)

-Select the option "Enable". 

-In the "Index document" field, enter the name of your main HTML file (e.g., "index.html"). 

-Optionally, you can provide a custom error document for handling 404 errors. 

-Click on the "Save changes" button.

![Screenshot 2025-01-11 215603](https://github.com/user-attachments/assets/249855e5-cab0-4d61-9441-19dd7a033338)


# Step 6: 

Upload Website Files 

Open Notepad or any text editor and create a new file.

Write the desired content that you want to display on the website.

![Screenshot 2025-01-11 215603](https://github.com/user-attachments/assets/249855e5-cab0-4d61-9441-19dd7a033338)

Go to the "File" menu and click on "Save As".

Enter a file name for your webpage, ensuring that you include the ".html" extension, such as "index.html".

Click on the "Save" button to save the file.

![Screenshot 2025-01-11 215651](https://github.com/user-attachments/assets/1def5401-279c-4fb6-9881-742984d02a42)



-Navigate to bucket "Object"

-Go to the "Upload" button or and click on it

![Screenshot 2025-01-11 215742](https://github.com/user-attachments/assets/c2cc97b9-edf2-44c5-aba7-1a679dbc6311)


-Go to the "Add files".

![Screenshot 2025-01-11 215800](https://github.com/user-attachments/assets/fef8a726-c567-4a27-8dc2-8c1bdda1900f)

-Select the "dipindex.html" file.

![Screenshot 2025-01-11 215826](https://github.com/user-attachments/assets/0bbddce4-0ddb-43aa-99fc-94d1a498cbd6)

-Then click on the "Upload" button.
![Screenshot 2025-01-11 215844](https://github.com/user-attachments/assets/6bd69e7d-d304-4152-99d7-cec160a1bee3)

-Once the upload is complete, you will see a confirmation message indicating that the file has been successfully uploaded.

![Screenshot 2025-01-11 215859](https://github.com/user-attachments/assets/80bdc732-077a-4f06-8835-b20f5ed082a5)




# Step 7

-Enable Public Access 

-Go to the bucket settings and select "Permissions."

-Locate the section titled "Block public access (bucket settings)" and click on "Edit."

![Screenshot 2025-01-11 215920](https://github.com/user-attachments/assets/3163b76f-277a-4bc0-9bbd-d7402a6241eb)



-Uncheck the box labeled "Block all public access" to allow public access to the bucket.

![Screenshot 2025-01-11 215951](https://github.com/user-attachments/assets/dc026fdc-96c7-47a8-8449-ae5a9086a702)



-In the designated field, type "confirm" to confirm your changes.

-this will will effectively enable public access for the bucket

![Screenshot 2025-01-11 220019](https://github.com/user-attachments/assets/6ca623a0-6705-4c08-b198-3aa9de69c351)

# Step 8

-Go to the bucket settings and select "Permissions."

-Locate the section titled "Bucket policy" and click on "Edit."

![Screenshot 2025-01-11 220039](https://github.com/user-attachments/assets/83b37c35-3af7-478e-b957-e39055a64ab3)

-Click on "Policy Generator" it will open in a new window.

![Screenshot 2025-01-11 220100](https://github.com/user-attachments/assets/e69be994-1a4d-4116-9ac1-16967e5cdf1e)

-Copy that "Bucket ARN" keep it for next Step.

![Screenshot 2025-01-11 220116](https://github.com/user-attachments/assets/00bf68b8-d291-46da-9d96-2b04ae06f99c)

-Select the type of policy as "S3" and set the effect to "Allow."

-In the "Principal" field, enter "*" to allow all the resourses.

-In the "Action" field, select "GetObject" to grant read access to the objects in the bucket.

-Paste the Bucket ARN (Amazon Resource Name) from the earlier tab you copy.

-Click on "Add Statement" to include the generated policy.

![Screenshot 2025-01-11 220349](https://github.com/user-attachments/assets/d598ec0b-10c4-4c59-a2b0-2cb252b8d90e)

-Click on the "Generate Policy" then policy will be generated.

![Screenshot 2025-01-11 220400](https://github.com/user-attachments/assets/9b8cb1ec-fbcd-4712-a9f2-7341dee13fe9)

-Copy the generated policy and paste it into the policy editor tab.

![Screenshot 2025-01-11 220433](https://github.com/user-attachments/assets/af0f0e35-a9d6-47db-9e4d-f4bb32ec5b53)

-Paste that policy here.

-Add "/*" at the end of the resource to allow access to all files under the bucket.

-Click on "Save Changes" to apply the bucket policy.

![Screenshot 2025-01-11 220649](https://github.com/user-attachments/assets/c2c27d29-2ff4-4142-84d5-8725e58acab1)

-Go to the Bucket "Properties".

![Screenshot 2025-01-11 220715](https://github.com/user-attachments/assets/e3463d8e-99fb-4049-a6ba-2004806a4646)

-Navigate to the bucket's website endpoint and copy the provided link.

![Screenshot 2025-01-11 220728](https://github.com/user-attachments/assets/c1eabe85-ba6c-4772-82fc-257195483475)

-Open the link in a browser to verify if the website is functioning correctly.

-You should now see your static website live and accessible through the provided URL.

![Screenshot 2025-01-11 220801](https://github.com/user-attachments/assets/837187dc-3bdf-49ed-a639-97513e1ef986)


# That's it! You have successfully hosted a static website using AWS S3.
