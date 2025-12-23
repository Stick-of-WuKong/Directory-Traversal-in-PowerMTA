# Directory-Traversal-in-PowerMTA

## Directory Traversal in PowerMTA

In the Configuration page, it is possible to view some files of pmta.

![image-20251221172039507](README.assets/image-20251221172039507.png) 

After capturing packets and examining the request path, it was found to be an absolute path, and `../` can be used for directory traversal.

![image-20251221172047718](README.assets/image-20251221172047718.png) 

However, accessing other directories requires root user privileges.

In the configuration, change the permission to root user (yes).

![image-20251221172331514](README.assets/image-20251221172331514.png) 

Once the pmta service restarts, arbitrary file reading can be performed with root user privileges.

