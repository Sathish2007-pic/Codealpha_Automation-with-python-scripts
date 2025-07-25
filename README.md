# Codealpha_Automation-with-python-scripts
Codealpha_Automation with python scripts import os
import shutil

source_folder = 'path/to/source/folder'
destination_folder = 'path/to/destination/folder'

# Create destination folder if it doesn't exist
os.makedirs(destination_folder, exist_ok=True)

# Move .jpg files
for filename in os.listdir(source_folder):
    if filename.lower().endswith('.jpg'):
        src_path = os.path.join(source_folder, filename)
        dest_path = os.path.join(destination_folder, filename)
        shutil.move(src_path, dest_path)
        print(f"Moved: {filename}")
