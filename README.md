usage:

```python
from PIL import Image
import requests

url = "https://sueszli.github.io/assets/cat_1966.jpeg"
img = Image.open(requests.get(url, stream=True).raw).convert("RGBA")
img = img.crop((0, img.height - img.width, img.width, img.height))
img.show()
```
