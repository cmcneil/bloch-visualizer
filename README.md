## Bloch Visualizer
This package can be used to create simple animations.
Use the nice bloch simulator at [neji49/bloch-simulator-python](https://github.com/neji49/bloch-simulator-python) to get a magnetic moment vector's path, and then plug that into this tool for an animation!

### Example
````
# neji49's simulator
from bloch import bloch
import visualize_mag as vm

mx, my, mz = bloch(...)

M = np.zeros((len(mz), 3))
M[:, 0] = mx
M[:, 1] = my
M[:, 2] = mz

frame_rate = 25
subsample = 1
vm.vis_magnetic_moment(M, frame_rate, subsample)
````

Enjoy your animation!
![Animation](example.png?raw=true "Animation")
