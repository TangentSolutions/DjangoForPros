## Urls

### Typical layout

```
. project
  |_ project/urls.py # top level urls for the project
  |_ app/urls.py # urls for an app
```

### DRF API router layout

In `{projectfolder}/api.py` we set up our project wide API

**Import**

```
from myapp1.api import FooViewSet, \
					   BarViewSet, \
					   BazViewSet, \
					   ...
from myapp2.api import AViewSet, \
					   BViewSet, \
					   CViewSet, \
					   ...
```

**Setup router**

```
router = routers.DefaultRouter()

# myapp1
router.register(r'app1/foo', FooViewSet)
router.register(r'app1/bar', BarViewSet)
router.register(r'app1/baz', BazViewSet)

# myapp2:
router.register(r'app2/a', AViewSet)
router.register(r'app2/b', BViewSet)
router.register(r'app2/c', CViewSet)
```

**NB Be consistant:**

* singular vs. plural

**urls.py**

> finally, we add our API to urls.py

```
from django.conf.urls import url, include, static
from .api import router

urlpatterns = [
    ...
    url(r'^api/', include(router.urls)),
]
```






