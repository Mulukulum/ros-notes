##  Catkin is the build system for ROS

For a package to be considered a catkin package it must meet a few requirements:

 - The package must contain a catkin compliant package.xml file.
   - That package.xml file provides meta information about the package.
- The package must contain a CMakeLists.txt which uses catkin.
   - If it is a catkin metapackage it must have the relevant boilerplate CMakeLists.txt file.

- Each package must have its own folder
  - This means no nested packages nor multiple packages sharing the same directory.

## Recommended way of making packages
```
- workspace_folder/        -- WORKSPACE
      src/                   -- SOURCE SPACE
        CMakeLists.txt       -- 'Toplevel' CMake file, provided by catkin
        package_1/
          CMakeLists.txt     -- CMakeLists.txt file for package_1
          package.xml        -- Package manifest for package_1
        ...
        package_n/
          CMakeLists.txt     -- CMakeLists.txt file for package_n
          package.xml        -- Package manifest for package_n
```

### Create a Package Using `catkin_create_pkg`

`catkin_create_pkg <package_name> [depend1] [depend2] [depend3]`

### To build your packages go to the workspace folder and run this command
```
cd <workspace_folder>
catkin_make
catkin_make --source my_src_folder # for building packages outside of src/ folder
```
### To add the workspace to your ROS environment you need to source the generated setup file

`<workspace_folder>/devel/setup.bash`

### You can now find your packages and their dependencies using rospack
```
rospack depends1 YOUR_PACKAGE
```
To show all dependencies and not just first order ones, use `rospack depends <package>`

