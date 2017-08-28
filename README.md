
# Tensorflow for Lego object detection

## Prepare Training images

Create video of a specific brick, e.g. brick2x4.mov

Move to training-data/brick2x4

Create images (3 per second):
```ffmpeg -i brick2x4.mov -vf fps=3 img%03d.jpg
```

## Start training
```./learn.sh
```

## Predict recognition
```python label_image.py evaluation-data/eval2x2.png
brick2x2 (score = 0.67055)
brick2x3 (score = 0.28938)
brick2x4 (score = 0.03470)
brick1x2 (score = 0.00537)
```
## Resources

- See also https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/#0

- The retrain.py script is part of the tensorflow repo

```curl -O https://raw.githubusercontent.com/tensorflow/tensorflow/r1.1/tensorflow/examples/image_retraining/retrain.py
```
-
