# submodule-engine

 * Created to explain how to use submodules whitin a project (Provider and Client)

## On the Provider side

* add the submodules

```cmd
git submodule add https://github.com/glfw/glfw.git <path/to>
git submodule add https://github.com/Dav1dde/glad.git <path/to>
```

* when u run it, you can see that it has been added as follows

* added a .gitmodules and <path/to> as submodule

```
[submodule "external/glfw"]
	path = external/glfw
	url = https://github.com/glfw/glfw.git
```

* commit to ur repo
```
git add .
git commit -m "added a submodules"
git status
git push
```

* if given "path/to" as external/libname, it will appear as follows

```cmd
└─external
    ├─glad
    │  ├─.github
    │  │  └─workflows
    │  ├─.....
    └─glfw
        ├─.github
        │  └─workflows
        ├─CMake
```

# On the Client side

* First, clone the this repo

```cmd
git clone https://github.com/ripcode0/submodule-engine.git
```

* as u can see theres the submodules is empty

```cmd
└─external
    ├─glad
    └─glfw
```

* Second, initialziing the submodule and update
```cmd
git submodule init
git submodule update
```
* or
```
git submodule update --init --recursive
```

* if u want to do it all at once during cloning without the above steps,
* you can do it as follows (is not recommended, in my oponion)

```cmd
git clone --recurse-submodules https://github.com/ripcode0/submodule-engine.git
```

* you can also create and distibute a batch(cmd) file

```cmd
submodule_update.cmd
```