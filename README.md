# Automatic Number Plate Recognition (ANPR) with YOLOv8

This project demonstrates Automatic Number Plate Recognition (ANPR) using YOLOv8 for vehicle detection and license plate detection. It leverages a pre-trained YOLOv8 model (YOLOv8n) to detect vehicles and uses a licensed plate detector to detect license plates. The project also includes methods for handling missing frames in video data and visualizing the detection results.

## Demo
You can view the demo output video [here](out.mp4).

## Dataset
The dataset (sample video) used for training and testing is included in this repository as `sample.mp4`.

## Model
- **YOLOv8n**: A pre-trained YOLOv8 model used for vehicle detection.
- **License Plate Detector**: A custom model trained using YOLOv8 to detect license plates.

## Dependencies

This project requires the following dependencies:
- Python 3.10
- `sort` module (for tracking objects)

### Installing Dependencies

1. Unzip the `sort.zip` file included in the repository. This will extract the necessary `sort` module.

   ```bash
   unzip sort.zip
   ```

2. Create a Python environment with Python 3.10:

   ```bash
   conda create --prefix ./env python==3.10 -y
   ```

3. Activate the environment:

   ```bash
   source activate ./env
   ```

4. Install the project dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Running the Project

1. Run the `main.py` file with the sample input video file (`sample.mp4`) to generate the `test.csv` file:

   ```bash
   python main.py
   ```

2. After running the main script, run `add_missing_data.py` to interpolate values and match up missing frames:

   ```bash
   python add_missing_data.py
   ```

3. Finally, run `visualize.py` to visualize the license plate detection results by passing in the interpolated CSV file. This will generate the output video:

   ```bash
   python visualize.py
   ```

   The resulting output video will be saved as `out.mp4`.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- YOLOv8 for vehicle and license plate detection.
- The SORT (Simple Online and Realtime Tracking) algorithm for object tracking.
```
