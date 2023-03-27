The following are instructions on making **VTube Studio** run with **OpenSeeFace** face tracking on Linux (specifically Arch Linux). This will require some technical knowledge about Linux and is not recommended for beginners, but if you're reading this I'm sure you're already aware of that.

Thanks to **Ruyi#0110** for making this guide.

# Guide: Running VTube Studio using OpenSeeFace webcam tracking on Linux

Used distro: **Arch Linux**. The dollar sign represents the start of the command line, don't include that.

## Install python39

`$sudo pacman -Sy python39` 

Note that `pacman` cannot run without `sudo`. `pacman` is the package manager on the used Arch install, yours might be different.

`-Sy` is the argument for `pacman` that tells it to update the mirrors and install the package.

`python39` is the package name itself (I think on debian it might be called 3.9).


## Install the requirements

`$sudo pacman -Sy python-pip python-virtualenv git`


`python-pip` is the thing we will use to install stuff in our virtual environment.

`python-virtualenv` is the virtual environment itself.

`git` will help us download `OpenSeeFace`. Again, the package names might be different. Some packages you might already have installed.

## Download/Install OpenSeeFace

`$git clone https://github.com/emilianavt/OpenSeeFace`

Then enter its folder:

`$cd OpenSeeFace`

And create the virtual environment:

`$virtualenv -p python39 env`

Then start the virtual environment:

`$source env/bin/activate`

And install all the stuff the facetracker requires to run:

`$pip install onnxruntime opencv-python pillow numpy==1.21.6`

The reason `numpy` is different is because we need an older version of `numpy`. This specific version is required.

And then, this is where the magic happens!

`$python facetracker.py -c 0 -W 1280 -H 720 --discard-after 0 --scan-every 0 --no-3d-adapt 1 --max-feature-updates 900`

## Start VTube Studio

Now you should be able to open up VTube Studio, select `VTubeStudioCam` and enjoy (don't worry if the resolution says 4x4, all we need is the `OpenSeeFace` info from it).

Note that you need to start the virtual environment every time you want to use `OpenSeeFace`, using the following three commands:

*  `$cd OpenSeeFace`
*  `$source env/bin/activate`
*  `$python facetracker.py -c 0 -W 1280 -H 720 --discard-after 0 --scan-every 0 --no-3d-adapt 1 --max-feature-updates 900`

Note that `-c 0` represents your camera. It usually is `0` but if you have multiple cameras (like the camera from the Valve index) you may need to use a different number here (try `1`, `2`, ...)