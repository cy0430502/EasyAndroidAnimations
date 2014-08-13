AndroidAnimator
===============

AndroidAnimator is an animation library aims to make android animation easier, many complex animation effects can be achieved with one or two lines of code.


Demo Video
----------

[![ScreenShot](https://raw.githubusercontent.com/2359media/AndroidAnimator/develop/Animation_demo/android%20animator%20demo%20screenshot.PNG)](http://www.youtube.com/watch?v=qb63BYjTebU)


Usage:
======

*See `Animation_demo/` folder for a working implementation of this library.*

  1. For example, if you wanted a view to mimic the bounce animation with the default parameters,
  ```
    new BounceAnimation(yourView).animate();
  ```

  2. If you wanted to use your own parameters instead of the default ones,
  ```
    new BounceAnimation(yourView)
      .setBounceDistance(50)
      .setBounces(5)
      .setDuration(500)
      .animate();
  ```

  3. Here's another example of mimicking the explode animation with your own parameters as well as the addition of an animation listener.
  ```
    new ExplodeAnimation(yourView)
      .setExplodeMatrix(ExplodeAnimation.MATRIX_2X2)
      .setInterpolator(new DecelerateInterpolator())
      .setDuration(500)
      .setListener(new AnimationListener() {
        @Override
        public void onAnimationEnd(Animation animation) {
          *perform your own functions here when animation ends*
        }
      })
      .animate();
  ```

  4. It is also possible to play several animations in parallel using the `ParallelAnimator` class. The following example scales in a view and flips it horizontally at the same time.
  ```
    new ParallelAnimator()
      .add(new ScaleInAnimation(yourView))
      .add(new FlipHorizontalAnimation(yourView))
      .setDuration(500)
      .animate();
  ```


Including In Your Project
-------------------------

You can simply download the available jar file and include it in your project, otherwise you can download the source code and customize it according to your need. 



Coding Robos
------------

 [Umair Vatao](http://sg.linkedin.com/in/umairvatao), [Nee Si Yao](http://sg.linkedin.com/pub/si-yao-nee/7a/a62/203/), [Phu Tang](phu.tanghong@2359media.com.vn)
 
