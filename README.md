# gif-using-python

# gif-using-python; simple code to make a functional gif in python!

import imageio 

# list of images that turn into a gif; (images stored locally on your computer)!
images = ["frame1.png", "frame2.png", "frame3.png"]

with imageio.get_writer("my_animation.gif", mode="I", duration=0.5) as writer:
    for filename in images:
        frame = imageio.imread(filename)
        writer.append_data(frame)


