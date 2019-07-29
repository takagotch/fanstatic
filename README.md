### fanstatic
---
http://www.fanstatic.org/en/latest/

```py
from fanstatic import Library, Resource
bar_library = Library('bar', 'bar_resources')
a = Resource(bar_library, 'a.css')
b = Resource(bar_library, 'b.js')

from foo import b
def somewhere_deep_in_our_code():
  b.need()


from fanstatic.injector import InjectorPlugin

class MyInjector(InjectorPlugin):
  name = 'mine'
  
  def __init__(self, options):
    """
    """
  def __call__(self, html, needed, request=None, response=None):
    """
    """
    needed_html = self.make_inclusion(needed).render()
    return html.replace('<head>', '<head>%s' % neede_html, 1)

from fanstatic import Library, Resource, Inclusion
qux_library = Library('qux', 'qux_resources')
a = Resource(qux_library, 'a.css')
b = Resource(qux_library, 'b.css')

needed = fanstatic.init_needed()
Inclusion(needed, bundle=True)

c = Resource(qux_library, 'a.css', dont_bundle=True)
```

```
```

```
```


