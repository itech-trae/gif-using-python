# gif-using-python

import imageio

images = ["frame1.png", "frame2.png", "frame3.png"]

with imageio.get_writer("my_animation.gif", mode="I", duration=0.5) as writer:

    for filename in images:
    
        frame = imageio.imread(filename)
        writer.append_data(frame)


