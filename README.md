# RL Project 2020: Training agent to paint a portrait

Paper Source: https://arxiv.org/pdf/1903.04411.pdf \
DDPG Source: https://arxiv.org/pdf/1509.02971.pdf \
TD3 Source: https://arxiv.org/pdf/1802.09477.pdf 

Image Dataset
http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html

To test the code
```
python3 DDPG/baseline/test.py --max_step=80 --actor=actor.pkl --renderer=renderer.pkl --img='path to image' --divide=5
ffmpeg -r 30 -f image2 -i output/generated%d.png -s 512x512 -c:v libx264 -pix_fmt yuv420p video_t.mp4 -q:v 0 -q:a 0
```
In python interpreter:
```
from IPython.display import display, Image
import moviepy.editor as mpy
display(mpy.ipython_display('video_t.mp4', height=256, max_duration=100.))
display(Image('output/generated399.png'))
```
