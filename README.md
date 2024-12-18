# Automatic Number Plate Recognition (ANPR) with YOLOv8

This project demonstrates Automatic Number Plate Recognition (ANPR) using YOLOv8 for vehicle detection and license plate detection. It leverages a pre-trained YOLOv8 model (YOLOv8n) to detect vehicles and uses a license plate detector to detect license plates. The project also includes methods for handling missing frames in video data and visualizing the detection results.

## Demo
You can view the demo output video [here](out.mp4).

## Dataset
The dataset (sample video) used for training and testing is included in this repository as `sample.mp4`.

## Model
- **YOLOv8n**: A pre-trained YOLOv8 model used for vehicle detection.
- **License Plate Detector**: A custom model trained using YOLOv8 to detect license plates.

## Cloning the Repository in VS Code

To clone this repository in Visual Studio Code:

1. **Open VS Code**: Launch Visual Studio Code on your system.

2. **Open the Command Palette**: 
   - You can open the Command Palette by pressing `Ctrl + Shift + P` (Windows/Linux) or `Cmd + Shift + P` (Mac).

3. **Clone the Repository**:
   - Type `Git: Clone` in the Command Palette and select the `Git: Clone` option.
   - In the prompt that appears, paste the URL of this repository: `https://github.com/dhanyakini/License-plate-recognition`.
   - Press Enter.

4. **Choose a Directory**:
   - VS Code will prompt you to select a location on your system where you want to save the cloned repository. Choose your desired directory.

5. **Open the Repository**:
   - Once the cloning is complete, VS Code will ask if you want to open the cloned repository. Click `Open` to open the folder in VS Code.

## Setting Up the Environment

1. **Create a Python environment with Python 3.10**:

   ```bash
   conda create --prefix ./env python==3.10 -y
   ```

2. **Activate the environment**:

   ```bash
   source activate ./env
   ```

3. **Install the project dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Unzip the `sort.zip` file** to extract the necessary `sort` module:

   ```bash
   unzip sort.zip
   ```

5. **Navigate into the `sort` directory**:

   ```bash
   cd sort
   ```

6. **Install the required dependencies for `sort`**:

   ```bash
   pip install -r requirements.txt
   ```

7. **Navigate back to the root project directory**:

   ```bash
   cd ..
   ```

## Running the Project

1. **Run the `main.py` file** with the sample input video file (`sample.mp4`) to generate the `test.csv` file:

   ```bash
   python main.py
   ```

2. **Run `add_missing_data.py`** to interpolate values and match up missing frames:

   ```bash
   python add_missing_data.py
   ```

3. **Run `visualize.py`** to visualize the license plate detection results by passing in the interpolated CSV file. This will generate the output video:

   ```bash
   python visualize.py
   ```

   The resulting output video will be saved as `out.mp4`.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- YOLOv8 for vehicle and license plate detection.
- The SORT (Simple Online and Realtime Tracking) algorithm for object tracking.
