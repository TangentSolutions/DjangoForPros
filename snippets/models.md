## Models

### A basic started model:

```
from django.db import models
from django.contrib.auth import get_user_model
from django.conf import settings

class ModelName(models.Model):
    """..."""

    user = models.ForeignKey(settings.AUTH_USER_MODEL, related_name='appointments')
    fk = models.ForeignKey('..', blank=True, null=True, default=None, related_name='...')
    name = models.CharField(max_length=200)
    ...
    created_date = models.DateTimeField(auto_now_add=True, db_index=True)
    modified_date = models.DateTimeField(auto_now=True, db_index=True)
```

#### CommonFieldTypes


### Resourcces

