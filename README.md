# Simple way to generate poses

## Why?
* The objective of this repo is create an alternative [LLFF](https://github.com/fyusion/llff) repo to generate poses required for models such as NeRF without all of the bloat of having to run LLFF.
* Note that pretty much all of the code was borrowed from the LLFF repo, so credits to the authors of the original repo.
## Instructions
1. First you need to have installed [colmap](https://github.com/colmap/colmap)
* Note that if you require Cuda acceleration you need to [compile colmap yourself](https://colmap.github.io/install.html)
2. Clone the repo.
``` bash
git clone https://github.com/EmanuelRiquelme/Generate_poses_Colmap
```
3. Create a parent directory named points and a child directory named images and copy your images to the images directory.
create the directories by.
``` bash
mkdir -p points/images
```
4. Run the script for extracting the features of the image using colmap
``` bash
chmod +x runcolmap.sh
./runcolmap.sh
```
5. Run gen_poses.py script to generate the poses.
```
python3 gen_poses.py 
```
* the poses file will be stored on the points directory
* Note numpy is required for running the python script.
