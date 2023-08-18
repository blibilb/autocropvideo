# Simple video autocropper, using random frames to analyze black bars
## made for instagram/tiktok videos that are in a specific aspect ratio creating black bars

# First time setup
## 1. in command prompt
```bash
git clone https://github.com/Hecker5556/autocropvideo.git
```
## 2.
```bash
cd autocropvideo
```
## 3.
```bash
pip install -r requirements.txt
```

# Usage

```
usage: autocropper.py [-h] [-file FILE] [-threshold THRESHOLD] [-amountframes AMOUNTFRAMES] [-deletetemp]

autocrop a video with changeable threshold and amount of frames to analyze

options:
  -h, --help            show this help message and exit
  -file FILE, -i FILE   filepath to video
  -threshold THRESHOLD, -t THRESHOLD
                        threshold, between 1-20 is recommended, default 10
  -amountframes AMOUNTFRAMES, -f AMOUNTFRAMES
                        amount frames to analyze (frames picked at random, default amount of frames is 5)
  -deletetemp, -d       whether to delete temporary files used
```

# Python usage
```python
import sys
if 'path/to/autocropvideo' not in sys.path:
    sys.path.append('path/to/autocropvideo')
from autocropvideo.autocropper import autocrop
outputname = autocrop(filename=filename, threshold=threshold, framestoanalyze=framestoanalyze, deletetemp=deletetemp)
```