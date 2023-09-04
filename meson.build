project('tdd-cpp', 'cpp')

add_project_arguments('-std=c++17', language : 'cpp')

src = []
inc = []

thread_dep = []
# thread_dep = dependency('thread')
gtest_dep = dependency('gtest', main : true, required : true)
gmock_dep = dependency('gmock', main : true, required : true)


subdir('inc')
subdir('src')
subdir('tests')