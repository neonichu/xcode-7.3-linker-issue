This project demonstrates an issue regarding Xcode 7.3 and
linking an OS X CLI target using Swift. 

If `-ObjC` is passed as a linker flag, linking will fail with
errors like:

```
duplicate symbol _OBJC_CLASS_$__SwiftNativeNSError in:
    /Applications/Xcode-7.3.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/swift_static/macosx/libswiftRuntime.a(ErrorObject.mm.o)
    /Applications/Xcode-7.3.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/swift_static/macosx/libswiftCore.a(ErrorObject.mm.o)
```

Linking works fine if `-ObjC` is not being passed.

