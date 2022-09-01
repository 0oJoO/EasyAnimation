# EasyAnimation

This program helps to create effective 2D animations with shapes.


Design of the program:
To create the animation, I split the process into 2 parts: 
  -the basic shapes and the useful information;
  -the animations/changes of the shape.

Thus, I created 2 interfaces representing shapes and animations, and then I combine them together as the complete animation model.
1) Shape 
  -AbstractShape implements Shape, Oval and Rectangle extends AbstractShape.
  -This interface contains the information of shapes. Including the name, the type, the position, 
   the dimension, the appear time, and the disappear time of the shape.
  -The shape interface should be implemented by the rectangle and oval, but the 2 shapes have a lot
   in common, so I created an abstract class to demonstrate the common implementations of some method for the 2 shapes.
2) Animation
  -AbstractAnimation implements Animation, ChangePos, ChangeColor, ChangeScale extends AbstractAnimation.
  -This interface contains the changes (animations) of the shape. The changes are position, color, or scale.
  -The 3 classes of changes also share some commonalities which remain the same during the animations, such as shape type, shape name, start time and finish time of the animation. So I create an abstract class for them.
Now, with both the shape information and animation information, we can build the animation model.
3) AnimationModel
  -AnimationModelImpl implements AnimationModel.
  -In the AnimationModelImpl, we can actually make some changes on a specific shape. 








