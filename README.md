# Download Image

## Description

Create an in-memory image file, in the specified format, from a remote URL for saving to a django ImageField.

## Installation

```python
pip install download-image
```

or

```python
pipenv install download-image
```

## Methods

1. download\_image\_as\_gif(url, file_name)
2. download\_image\_as\_png(url, file_name)
3. download\_image\_as\_jpeg(url, file_name)
4. download\_image\_as(url, file\_format, file\_name)

## Usage

```python
from django.db import models
from download_image.utils import download_image_as_gif

class ExampleModel(models.Model):
    picture = models.ImageField(upload_to="/path/to/upload/")

instance = ExampleModel()
instance.picture = download_image_as_gif("https://url.to.file", "optional_file_name.gif")
instance.save()
```
