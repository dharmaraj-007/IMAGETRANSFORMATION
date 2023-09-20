# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4
Display the modified image output.

### Step5:
End the program.

## Program:
```python
Developed By:Dharmaraj S
Register Number:212222240025
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lion.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()

ii) Image Scaling
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lion.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,50],
              [0,1,50],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 


iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lion.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()


iv)Image Reflection
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lion.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  



v)Image Rotation
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lion.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()  



vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("lion.png")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:500 ,10:700]
plt.imshow(cropped_img)
plt.show()



```
## Output:
### i)Image Translation
![1](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/e3c4e7c6-b24c-4620-b689-8eec31b50258)


### ii) Image Scaling

![2](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/dd2dddf2-e592-47ef-bb08-aa587d992373)


### iii)Image shearing

![3](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/7583ec50-34bb-40d4-87f1-4857daeae11b)
![4](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/72421e7c-2617-46ff-a3d6-8f3c860e4fde)


### iv)Image Reflection
![5](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/8b9c60af-2873-4140-bb48-ce6ad850a7a9)
![6](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/7b645482-070e-47e7-af2b-f1876be3fc40)


### v)Image Rotation

![7](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/76d4deb6-b254-42fd-90fa-8c5546d3a2fa)



### vi)Image Cropping
![8](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/7ef09a26-32d3-49f1-8e6f-582d6ad51878)

![9](https://github.com/dharmaraj-007/IMAGETRANSFORMATION/assets/119560386/656da586-b6ae-4391-9444-e60a970f68af)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
