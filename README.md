# Comp3110f
Final project

## Team Members
- **Jingsheng Qiu** - qiu32@uwindsor.ca
- **Albert He** - Healber@uwindsor.ca
- **Duc Nguyen** - nguyen7x@uwindsor.ca

## Evaluation Results
- **Accuracy**: 82.5% (236/286 line mappings correct)
- **Dataset**: 27 file pairs from Eclipse projects
- **Best Performance**: about 14 files with ~90-100% accuracy
- **Check**: 'testEclipse.csv' for more detailed results

Project Overview
===============

Given two versions of the same source file,
the tool outputs the line number of each line in the old file corresponding to the new file, or marks it as deleted.

Environmental Requirements
===============

- python3.1x

- Python Virtual Environment：venv

Main Files
===============

- singlePair.py: Apply the row mapping algorithm to a single file pair and output a CSV file.

- filePreprocess.py: Responsible for reading text files for preprocessing (formatting files) and writing the line mapping results to CSV files.

- similarity.py: Edit Distance and Similarity Calculation

- core: Match rows that are identical in their entirety. For the remaining rows, perform similarity analysis; row pairs exceeding the threshold are considered identical.

- eclipseXml_utils.py: Read the XML files in the eclipseTest directory to determine the version and number, as well as the line mappings between orig and new for each version

- eclipseDataset.py: Evaluate the Eclipse dataset located in the eclipseTest directory.

- newDataset: Evaluate the custom datasets in the newDataset directory

- /newDataset: Self-built Dataset Directory:  
 /newDataset/xxx_old.java  
 /newDataset/xxx_new.java  
 /newDataset/xxx.csv: tracking information

How to use:
===============
 1. singlePair.py
    
    Enter at the terminal:
    
    python singlePair.py <oldFile> <newFile> <outputfile(.csv)> <similarityLevel>
    
    Expected Output:
    
    old,new
     
     1,1
      
     2,3
   
     4,5 
    
     6,X
     
     9,6
     
    old: Line numbers in the old file
    
    new: Line numbers in the new file
 
    X: The corresponding line number does not exist in the new file.

    
2. Evaluate the eclipseTest dataset
  
   - Ensure that the eclipseTest folder and eclipseTest.py are in the same directory.
   
   - Run eclipseTest.py directly.

3. Evaluate the newDataset

   - Ensure that the newDataset folder and newDataset.py are in the same directory.
   
   - Run newDataset.py directly.
