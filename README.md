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

![Screenshot_20230620_131813](https://github.com/Diplahane/AWS-S3/assets/129828021/79e43ee8-29a8-4efa-8e07-4b445a2e2171)



-Uncheck the box labeled "Block all public access" to allow public access to the bucket.

![Screenshot_20230620_131849](https://github.com/Diplahane/AWS-S3/assets/129828021/c7725df5-5b6f-41c7-bcb0-06abd5ba414a)



-In the designated field, type "confirm" to confirm your changes.

-this will will effectively enable public access for the bucket

![Screenshot_20230620_131924](https://github.com/Diplahane/AWS-S3/assets/129828021/86ae9715-dd6a-477b-9424-619cfb7acab1)

# Step 8

-Go to the bucket settings and select "Permissions."

-Locate the section titled "Bucket policy" and click on "Edit."

![Screenshot_20230620_132038](https://github.com/Diplahane/AWS-S3/assets/129828021/397ce014-d02a-42bc-9aa8-6ce6cc4844fb)

-Click on "Policy Generator" it will open in a new window.

![Screenshot_20230620_132107](https://github.com/Diplahane/AWS-S3/assets/129828021/684af865-550f-494c-851b-0d4fa33c1d54)

-Copy that "Bucket ARN" keep it for next Step.

![Screenshot_20230620_132348](https://github.com/Diplahane/AWS-S3/assets/129828021/74473f02-cf0e-4d4a-9f8a-98d30f2d0bdb)

-Select the type of policy as "S3" and set the effect to "Allow."

-In the "Principal" field, enter "*" to allow all the resourses.

-In the "Action" field, select "GetObject" to grant read access to the objects in the bucket.

-Paste the Bucket ARN (Amazon Resource Name) from the earlier tab you copy.

-Click on "Add Statement" to include the generated policy.

![Screenshot_20230620_132420](https://github.com/Diplahane/AWS-S3/assets/129828021/43d77d85-72fc-487e-ad19-0d0f430fa51c)

-Click on the "Generate Policy" then policy will be generated.

![Screenshot_20230620_132442](https://github.com/Diplahane/AWS-S3/assets/129828021/6e32a6a8-fc23-413a-8b5c-d3a857f33015)

-Copy the generated policy and paste it into the policy editor tab.

![Screenshot_20230620_132454](https://github.com/Diplahane/AWS-S3/assets/129828021/c9a88095-bf47-4a89-827b-bcc7398214de)

-Paste that policy here.

-Add "/*" at the end of the resource to allow access to all files under the bucket.

-Click on "Save Changes" to apply the bucket policy.

![Screenshot_20230620_133544](https://github.com/Diplahane/AWS-S3/assets/129828021/f7e0908b-8d52-4a47-bb4d-bf3991d1cb35)

-Go to the Bucket "Properties".

![Screenshot_20230620_133818](https://github.com/Diplahane/AWS-S3/assets/129828021/07b69bd9-efc2-402e-b044-4124b03a79b8)

-Navigate to the bucket's website endpoint and copy the provided link.

![Screenshot_20230620_133830](https://github.com/Diplahane/AWS-S3/assets/129828021/624e6002-cd59-4a7c-b8fb-66ea0efbc897)

-Open the link in a browser to verify if the website is functioning correctly.

-You should now see your static website live and accessible through the provided URL.

![Screenshot_20230620_133904](https://github.com/Diplahane/AWS-S3/assets/129828021/dbe3c381-bc01-4fe1-b486-1551edbf4cfd)


# That's it! You have successfully hosted a static website using AWS S3.
