StripScope

StripScope is a Windows desktop tool that turns AVI inspection CSV files into a one-page production report (PDF and Excel). It works per strip and shows how many strips were inspected, how many defects were found, and which defect types are most common.

What the report shows

First-pass, re-inspected, and total strip counts.
Total defects and average defects per strip. This counts NG results only; NF results are excluded.
Average defect count per strip for the front side and the back side.
Inspection start and end time, actual inspection time, and utilization rate.
CTAvgTime and CTNowTime.
The top defect location and type, for example Metal / Discolor, plus a chart of the top five defect types with the rest grouped as Other.

How to use it

Select the folder that contains the inspection summary CSV files.
Optionally select the folder with the AI defect files and enter a filename pattern, such as AI*.csv;*.ai. Strips are matched by the last four digits of Step_Code, which is the Strip ID.
Choose an output folder and click Generate to get the PDF, Excel, and chart image.


powershell 

cd "C:\Users\user\Downloads\PulseFlow-Windows-Builder-v1.4"


py -3.12 -m venv .venv


.\.venv\Scripts\Activate.ps1


python -m pip install --upgrade pip
python -m pip install matplotlib openpyxl pillow pyinstaller


python -m PyInstaller --noconfirm --clean ProductionReportGenerator.spec
