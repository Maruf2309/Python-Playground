# Level1 : Github Repo Setup

### 1.1 Create Repo in Github
```bash
Go Github  > Create new:
Click New Repo 
Give Repository Name like ds-knowlege
Description: Optional
Choose Visibility (Public / Private)
Add ReadMe : Enable it
Add .gitignore: Python
Add License: MIT Licence
Click > Click Repository
```
### 1.2 Clone it
It get all from github to your local system: 
```bash
Go Github  > Your Repository:
Click Code from Top right
Copy the link shows in http :https://github.com/Maruf2309/data-science-knowledge-base.git
```
### 1.2.1 Clone it - Local Drive - Git Bash
```bash
Go Your local drive where you want clone / keep your project
Go Drive 
Instead of creating another folder directly clone it

Clone / Git Bash:
    Go Folder 
    Right click
        Show More
        Open Git bash here
    git clone > enter copied link
    Close Terminal (Git Bash)
```

### 2.0 Open Project From Local System - Open by VS code

```bash
Go inside folder
    You will see: (gitignore, license, readme) keep as it is
Right Click
Open with VS Code
Write ReadMe File (Optional, but Recommended)
ReadMe Preview (Optional)
    Cursor take on ‘ReadMe’ > right click > Open Preview
```

### 3.0 Create Virtual Environment
Go inside folder Like: (Cloned / Project Folder e.g ds-knowledge )
- You will see: (gitignore, license, readme) keep as it is
- Right Click > Open VS Code
- Terminal > Select Command Prompt > 
- You will see (bash) inside bracket if not visible then type 
`active base` 
then you must see (bash) inside bracket. 
- We can create virtual env on base only.

Now create virtual environment with below command:
```
    Create: conda create -n dsknowledge python=3.11 -y
    Active: conda activate dsknowledge
    Check python: python enter
    Close : exit()
```

### 4.0 Requirement Installation
```bash
Create file inside folder as:
    requirements.txt
For learning no need to mention package version (Optional)
Package Installation > go terminal > execute below command:
pip install -r requirements.txt > enter`
Create a Main file as main.py or jarvis.py (Since its my learning directory) so it's optional here !
```

### Automatic Folder Creation (Powersheel for automation)
Run this below in the terminal(Powershell):For automation Powershell is best!


```
$folders = @(
"imputation",
"preprocessing",
"feature_engineering",
"feature_selection",
"exploratory_data_analysis",
"statistics",
"probability",
"pandas",
"numpy",
"visualization",
"data_cleaning",
"data_transformation",
"encoding",
"scaling_normalization",
"outlier_detection",
"time_series",
"machine_learning",
"deep_learning",
"natural_language_processing",
"computer_vision",
"model_evaluation",
"hyperparameter_tuning",
"pipelines",
"deployment",
"mlops",
"big_data",
"sql",
"data_engineering",
"api_integration",
"web_scraping",
"experiments",
"case_studies",
"interview_preparation",
"cheat_sheets",
"algorithms",
"math_for_ml",
"optimization",
"best_practices"
)

foreach ($folder in $folders) {
    New-Item -ItemType Directory -Path $folder -Force | Out-Null
}
```
Press Enter

### 6.2 Add `.gitkeep` so GitHub shows empty folders (Recommended) 
Git does not track empty folders, so run(Terminal > Powershell):

```bash
foreach ($folder in $folders) {
    New-Item -ItemType File -Path "$folder\.gitkeep" -Force | Out-Null
}