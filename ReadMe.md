# Lesion Network Mapping Tutorial

## Examples of Lesion Network Mapping Studies
### Vestibular Symptoms
All figures should look identical up to 2:59 in the [BRAIN Journals video](https://www.youtube.com/watch?v=KIXw283fk7I&ab_channel=BRAINJournals).

Another example: [OnNeuro video](https://www.youtube.com/watch?v=TQyZ_FUaDF4&ab_channel=OnNeuro).

## Background
Lesion network mapping (LNM) utilizes the human connectome to investigate associations between neurological or psychiatric symptoms and distributed functional networks in the brain. The networks and connected brain regions identified could be potential treatment targets using both invasive and noninvasive brain stimulation techniques. Mike’s NEJM paper provides helpful information on the rationale and basics of LNM.

This tutorial covers the basic steps of an LNM analysis, from tracing literature lesions to associating functional networks with behavior. It will equip you with the fundamentals to develop scripts, conduct analyses, or investigate a symptom-specific question of your own.

## Overview of Steps:
1. Trace lesions using 3D Slicer
2. Upload lesions and master CSV to metadata folder in project. 
3. Generate descriptive statistics tables of metadata (Notebook 01). 
4. Register lesions to the correct space (Notebook 02)
5. Run lesions as seeds through the human connectome (Notebook 02)
6. Add generated niftis for each patient to the master CSV (Notebook 03)
7. Generate Sensitivity Map for Lesions and Lesion Networks (Notebook 04/04b)
8. Generate Specificty Map (Notebook 05)
9. Generate Conjunction Map (Notebook 06)
10. Run additional analyses as needed. 

## Step-by-Step Guide

### Step 0: Setup
1. Set up a directory.
2. Open a terminal in that directory.
3. Run `pip install calvin_utils`.
4. Ensure `nimlab` is installed.
5. Clone the repository:
   ```bash
   git clone https://github.com/Calvinwhow/HowardLesionNetworkMapping.git .
   ```

### Step 1: 3D Slicer
- Refer to the prior examples provided.

### Step 2: Accessing the Server
1. If unclear, this will be demonstrated at a lab meeting. For questions, email Calvin.
2. Navigate to [JupyterHub](https://jupyterhub2.partners.org/hub/home).
3. Enter your username and password.
4. Start the server.
5. Navigate to the study folders.

### Step 3: Upload Critical Data
1. Create a folder called `metadata` within your project folder.
2. Upload your master list to this folder. This CSV contains each patient’s demographics and metrics.
3. Create a folder called `Derivatives` within the project folder.
4. Create a subfolder called `Raws` within `Derivatives`.
5. Upload your traced NIfTI files here, either in BIDS format or all together.
6. If you have questions, ask Calvin.

### Step 4: Generate Demographics and Other Relevant Tables
1. Use Notebook 01 to import your master list.
2. Generate a table for patient demographics.
3. Generate a table for patient symptoms/extracted data.

### Step 5: Process Lesions and Run the Connectome
1. Open Notebook 01 and follow the instructions. For questions, email Calvin.
2. Enter the path to your uploaded NIfTI files:
   - If uploaded in the same directory, use ‘OPTION ONE’.
   - If uploaded in BIDS format, use ‘OPTION TWO’.
3. Use `MNI_152_T1_2mm_brain_mask` and generate only functional connectivity.
4. Add generated pictures to your PowerPoint to track them.

### Step 6: Add Processed Lesion NIfTIs to the Master List
1. Open Notebook 03 and follow the instructions. Email Calvin for questions.
2. Run it to add the processed NIfTIs to the master list.
3. Run it again to add the lesion network connectivity NIfTIs to the master list.

### Step 7: Generate Sensitivity Map
1. Open Notebook 03 in your project directory.
2. Apply thresholds: 100%, 90%, 80%, 70% overlap.
3. Perform this for both lesions and lesion networks.

### Step 8: Generate Specificity Map
1. Open Notebook 04 in your project directory.
2. Calvin will assist at the lab meeting.
3. Generate multiple specificity maps for each relevant contrast.

### Step 9: Generate Conjunction Map
1. Open Notebook 05 in your project directory and follow the instructions.
2. Calvin will assist at the lab meeting.