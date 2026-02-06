- name: Configure CMake
        run: |
          cmake -B build \
            -DCMAKE_BUILD_TYPE=Release \
            -DCMAKE_SYSTEM_NAME=iOS \
            -DCMAKE_OSX_SYSROOT=iphoneos \
            -DCMAKE_OSX_ARCHITECTURES=arm64 \
            -DGEODE_TARGET_PLATFORM=ios \
            -DGEODE_BINDINGS_REPO_PATH=$GITHUB_WORKSPACE/bindings-repo \
            -DCMAKE_XCODE_ATTRIBUTE_CODE_SIGNING_ALLOWED=NO \
            -DCMAKE_XCODE_ATTRIBUTE_CODE_SIGN_IDENTITY="" \
            -DCMAKE_XCODE_ATTRIBUTE_CODE_SIGNING_REQUIRED=NO
