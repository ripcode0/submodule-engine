# submodule-engine

 * how to set the submodule

# add submodules
```cmd
git submodule add https://github.com/glfw/glfw.git <path/to>
```

* when u run it, you can see that it has been added as follows

* added a .gitmodules and <path/to> as submodule

```
[submodule "external/glfw"]
	path = external/glfw
	url = https://github.com/glfw/glfw.git
```
