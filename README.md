# CATNIP
Welcome to CATNIP, a tool that facilitates the comparison of circumstellar disk images in multiple wavelengths. CATNIP, which stands for Comparative Analysis Tool for Normalized Imagery and Profiles, quantitatively analyzes disk substructures by generating radial and azimuthal profiles. With CATNIP, you can uncover trends in substructure between radio and infrared images, and begin to understand what it says about the underlying physical processes. 


Here are instructions to set up the tool on your computer:

Part 1 - setting up your Google sheet

Download the Google Sheet template here:

https://docs.google.com/spreadsheets/d/184hYnDk9GfWwiSwoP5TETOcQlaXzvlWzp36VwU9htdo/copy

This sheet comes preloaded with information for NIR and ALMA images for the disks EM* AS 209 and HD135344B. The files for these disk images are uploaded in the folder as a part of this tutotrial.

When you have made your own copy of this sheet, first we need to create a json file so the code can have permissions to talk to the sheet. Here are the steps to creating your own json file:

1. Create a new Google Cloud project in the Google Cloud Console (https://console.cloud.google.com)

2. Go to APIs & Services and click on Library

3. Enable Google Sheets API

4. In Cloud Console navigation menu, go to IAM & Admin and click Service Accounts
   
5. Create Service Account, give it a nice name, don't worry about permissions or principles

6. Inside the service account click on Keys, and select “Add Key”, “Create new key”, and chose json

7. Now you should have a downloaded json file

8. Go to your Google sheet and share it with the service account email and give it viewer access

9. Add the json file to the directory the tutorial file is in



Part 2 - setting up the code

Create and activate a new environment:

```
conda create --name myenv python=3.12

conda activate myenv
```

How to download:
```
git clone https://github.com/piper-lentz/CATNIP_draft.git
```

cd into CATNIP_draft folder

Install dependancies:
```
pip install -r requirements.txt
```

Open a Jupyter Lab
```
conda install jupyterlab

jupyter lab
```

and open the tutorial ipynb file in the FIGG-CATNIP folder.

Now work through and add tests and such
