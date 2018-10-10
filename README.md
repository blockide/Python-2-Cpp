# Usage
First, you need to install the following packages:

1.  protobuf (https://developers.google.com/protocol-buffers/?hl=en)
2.  runcython (https://github.com/Russell91/runcython)

Compile protobuf definition file for use by C++ and Python: 
```
$ protoc -I=./ --python_out=./ --cpp_out=./ objlist.proto
```

Run Cython file: 
```
$ runcython++ use_objlist.pyx '' "objlist.cpp objlist.pb.cc -lprotobuf"
```
