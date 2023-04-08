# svc-colab
This is a work in progress. It is a fork of the colab including fixes by YeezyBeaver. 
The purpose of these modifications are to support multiple speakers from different models to choose from. 
changes made to YeezyBeaver fixed colab nb:

In this updated code, model_urls is defined as a list of URLs, and the for loop iterates over each URL in the list. The if statement inside the loop checks if the URL is a Hugging Face URL, and if it is, it uses the re.sub() function to replace "/blob/" with "/resolve/" in the URL and then downloads the model with download(). If the URL is not a Hugging Face URL, it simply downloads the file with download().

This code recursively searches for all .zip files in the specified directory and extracts them to the same directory. It also removes the zip file after extraction to avoid cluttering the directory. You can use this code by specifying the directory path where your zip files are stored instead of specifying the individual zip file paths.

The code fixes the glob.glob() function to find all zip files in the current and subdirectories. For each zip file found, the extract() function is called to extract the contents of the zip file to the current directory.

Warning! some issues I have not resolved: 
* Using multiple speakers is missing clustering models for all except 1 speaker... meaning the speaker is recognized in the final inferencing cell, however the output is discombobulated. 
* This error is presented through this message:  "Note: No clustering model found for "+folder meanwhile one speaker model will work perfectly fine. All downloaded and extracted speakers will show up in the GUI dropdown menu.
