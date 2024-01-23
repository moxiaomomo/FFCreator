
### install error

```
npm ERR! code CERT_HAS_EXPIRED
npm ERR! errno CERT_HAS_EXPIRED
npm ERR! request to https://registry.npm.taobao.org/zrender/-/zrender-5.1.1.tgz failed, reason: certificate has expired

npm ERR! A complete log of this run can be found in:
npm ERR!     /home/xiaomo/.npm/_logs/2024-01-23T07_04_58_363Z-debug-0.log

== Solution
npm cache clean --force
npm config set strict-ssl false
npm install
```


### pkg-config

```
# update apt sources
https://blog.csdn.net/weixin_46538207/article/details/132411122
# install lib
https://blog.csdn.net/qq_38292379/article/details/106637451
```

### gyp ERR

```
npm ERR! In file included from /usr/include/c++/11/algorithm:62,
npm ERR!                  from ../angle/src/libANGLE/HandleAllocator.cpp:12:
npm ERR! /usr/include/c++/11/bits/stl_algo.h:3467:5: note: ‘std::max’ declared here
npm ERR!  3467 |     max(initializer_list<_Tp> __l, _Compare __comp)
npm ERR!       |     ^~~
npm ERR! ../angle/src/libANGLE/HandleAllocator.cpp:29:43: error: expected primary-expression before ‘(’ token
npm ERR!    29 |     mUnallocatedList.push_back(HandleRange(1, std::numeric_limits<GLuint>::max()));
npm ERR!       |                                           ^
npm ERR! ../angle/src/libANGLE/HandleAllocator.cpp:29:52: error: ‘numeric_limits’ is not a member of ‘std’
npm ERR!    29 |     mUnallocatedList.push_back(HandleRange(1, std::numeric_limits<GLuint>::max()));
npm ERR!       |                                                    ^~~~~~~~~~~~~~
npm ERR! ../angle/src/libANGLE/HandleAllocator.cpp:29:73: error: expected primary-expression before ‘>’ token
npm ERR!    29 |     mUnallocatedList.push_back(HandleRange(1, std::numeric_limits<GLuint>::max()));
npm ERR!       |                                                                         ^
npm ERR! ../angle/src/libANGLE/HandleAllocator.cpp:29:76: error: ‘::max’ has not been declared; did you mean ‘std::max’?
npm ERR!    29 |     mUnallocatedList.push_back(HandleRange(1, std::numeric_limits<GLuint>::max()));
npm ERR!       |                                                                            ^~~
npm ERR!       |                                                                            std::max
npm ERR! In file included from /usr/include/c++/11/algorithm:62,
npm ERR!                  from ../angle/src/libANGLE/HandleAllocator.cpp:12:
npm ERR! /usr/include/c++/11/bits/stl_algo.h:3467:5: note: ‘std::max’ declared here
npm ERR!  3467 |     max(initializer_list<_Tp> __l, _Compare __comp)

# install g++-10
sudo apt install -y build-essential g++-10 libxi-dev libxext-dev libpixman-1-dev libcairo2-dev libpango1.0-dev libjpeg8-dev libgif-dev libjpeg-dev librsvg2-dev mesa-common-dev
# using g++-10
CXX=g++-10 npm install
```
