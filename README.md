# C++ Devcontainer example project 
Default, simple hosted C++ project using meson/ninja and gtest/gmock

## Project config

This is a very simple project using C++, meson/ninja as the build system and Google Test/Mock as the test framework.
```
.
├── LICENSE
├── README.md
├── inc
│   └── meson.build
├── meson.build
├── src
│   ├── Widget.cpp
│   ├── Widget.h
│   └── meson.build
└── tests
    ├── meson.build
    └── widget_tests.cpp
```
## To build and run

First create the meson project
```
# meson builddir && cd builddir
```
Then build and run the tests
```
# ninja test
```

## To collect coverage statistic

First create the meson project with the `b_coverage=true` directive set
```
# meson -Db_coverage=true builddir && cd builddir
```
Then build and run the tests
```
# ninja test
```
Finally generate the coverage statistics:
```
# ninja coverage
```
```
Xml  coverage report can be found at ./builddir/meson-logs/coverage.xml
Text coverage report can be found at ./builddir/meson-logs/coverage.txt
Html coverage report can be found at ./builddir/meson-logs/coveragereport/index.html
```
