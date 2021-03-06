# Copyright (c) 2020, The Vulkan Developers.
#
# This file is part of libnetutils.
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in all
# copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
# SOFTWARE.
#
# You should have received a copy of the MIT License
# along with libnetutils. If not, see <https://opensource.org/licenses/MIT>.

set(LIBNETUTILS_TESTS_SOURCE_FILES
  buffer_tests.cpp
  main.cpp
)

set(LIBNETUTILS_TESTS_HEADER_FILES

)

add_executable(unittests ${LIBNETUTILS_TESTS_SOURCE_FILES}
                         ${LIBNETUTILS_TESTS_HEADER_FILES})

target_include_directories(unittests PRIVATE ../src)
target_link_libraries(unittests gtest gtest_main libnetutils)
