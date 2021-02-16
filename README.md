## Breadcrumb decorator for flask api

### Implementation :

- simple route:

```{ .python }
@ application.route('/my_route/')
@breadcrumb('my_route')
def my_route():

    # Do something
    return "something"
```

- route with variable:

```{ .python }
@ application.route('/my_route/my_slug')
@breadcrumb('my_route')
def my_route():
    slug = my_slug

    @breadcrumb(p)
    def call():
        return "Done"

    # for breadcrumb list

    call()

    # Do something
    return "something"
```
