# Migrating from v2 to v3 images

Important changes:

- v2 images are based on a Debian Stretch. v3 images are based on **Ubuntu 18.04**.
- Interally, v3 images are built from the [Ondrej PPA](https://launchpad.net/%7Eondrej/+archive/ubuntu/php/+index?batch=75&memo=75&start=75).
  This is a radical change from v2 that was built from the official PHP Docker image.
  As a result, the v3 image do not have PECL installed, nor a build environment. This makes the v3 images ~200MB lighter. 

Changes in extensions:

- The following extensions are now **enabled by default**: `calendar exif pcntl shmop sockets sysvmsg sysvsem sysvshm wddx zip`
- The `sqlite3` extension was previously enabled by default, but must now be enabled manually
