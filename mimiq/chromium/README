
Check out Chromium and build via [these instructions](https://chromium.googlesource.com/chromium/src/+/main/docs/linux/build_instructions.md).


Then, check out v79.0.3934.0 to apply the patch against:

```
git fetch --tags
git checkout tags/79.0.3934.0
gclient sync --with_branch_heads --with_tags
```

Apply the patches. Assuming working directory is `chromium/src/`.
```
git apply net_build.patch
cd net/third_party/quiche/src/ && git apply quiche.patch && cd ../../../..
```

Then build:
```
gn gen out/Debug
ninja -C out/Debug quic_server quic_client
```


---

This folder contains all the modified files in the chromium source code.
This Readme will tell you where each file should go in the chromium source. 

BUILD.gn
\chromium\src\net\BUILD.gn

quic_toy_client.h
\chromium\src\net\third_party\quiche\src\quic\tools\quic_toy_client.h

quic_toy_client.cc
\chromium\src\net\third_party\quiche\src\quic\tools\quic_toy_client.cc

The entire 'dhcp' folder
\chromium\src\net\third_party\quiche\src\quic\dhcp


