Jinkins job creating process
STEP-BY-STEP: Creating Your First Freestyle Job
Step 1: Access Jenkins Dashboard
1.	Open browser
2.	Navigate to: http://localhost:8080
3.	Login with your credentials
📍 You should see the Jenkins Dashboard with menu on left side
Step 2: Create New Job
Method 1: Using "New Item"
1.	Click "New Item" from left sidebar
2.	OR click "Create a job" link in center
Method 2: Using "+ New Item"
1.	Look for "+ New Item" at top left
Step 3: Configure Job Basics
Enter an item name: my-first-job
Job Name Rules:
•	✅ Use lowercase letters
•	✅ Use hyphens (-) instead of spaces
•	✅ Keep it descriptive
•	❌ Avoid special characters (@, #, $, etc.)
•	❌ Don't use spaces
Select Job Type:
1.	Select "Freestyle project"
2.	Click "OK" at bottom
Step 4: Job Configuration Page
You'll see multiple sections:
┌─────────────────────────────────┐
│ General                         │
│ Source Code Management          │
│ Build Triggers                  │
│ Build Environment               │
│ Build Steps                     │
│ Post-build Actions              │
└─────────────────────────────────┘
Step 5: General Configuration
Description (Optional but Recommended):
This is my first Jenkins freestyle job for learning purposes.
Other Options:
•	☐ Discard old builds (leave unchecked for now)
•	☐ This project is parameterized (leave unchecked)
•	☐ Disable this project (leave unchecked)
Step 6: Add Build Step
1.	Scroll down to "Build Steps" section
2.	Click "Add build step"
3.	Select based on your OS:
For Linux/Mac:
•	Select "Execute shell"
For Windows:
•	Select "Execute Windows batch command"
Step 7: Enter Build Commands
For Linux/Mac (Execute shell):
echo "========================================="
echo "Hello from Jenkins!"
echo "========================================="
echo "Current Date and Time: $(date)"
echo "Current User: $(whoami)"
echo "Current Directory: $(pwd)"
echo "Jenkins Job Name: $JOB_NAME"
echo "Build Number: $BUILD_NUMBER"
echo "========================================="
For Windows (Execute Windows batch command):
@echo off
echo =========================================
echo Hello from Jenkins!
echo =========================================
echo Current Date and Time: %date% %time%
echo Current User: %USERNAME%
echo Current Directory: %CD%
echo Jenkins Job Name: %JOB_NAME%
echo Build Number: %BUILD_NUMBER%
echo =========================================
Step 8: Save the Job
1.	Scroll to bottom
2.	Click "Save" button
3.	You'll be redirected to the Job Dashboard
________________________________________
RUNNING YOUR FIRST JOB
Method 1: Manual Build
1.	On Job Dashboard, click "Build Now" (left sidebar)
2.	Build will appear in "Build History" (bottom left)
3.	Build will show as #1 (first build)
