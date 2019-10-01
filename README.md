# Python-Code-Snippet


## Code to convert base64 string to image. 
```python

def getI420FromBase64(codec, image_path="c:\\"):
    # get codec from http
    # codec = codec.encode()
    base64_data = re.sub('^data:image/.+;base64,', '', codec)
    byte_data = base64.b64decode(base64_data)
    image_data = BytesIO(byte_data)
    img = Image.open(image_data)
    t = time.time()
    img.save(image_path + str(t) + '.png', "PNG")
    
  ```

## Usefull links to follow :
### https://github.com/ageitgey/face_recognition/issues/556
### https://github.com/ageitgey/face_recognition/issues/351
