## 0.8.5 2023-06-06 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.85.0


## 0.8.4 2023-05-26 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.84.1


## 0.8.3 2023-05-23 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.84.0


## 0.8.2 2023-05-10 <dave at tiredofit dot ca>

   ### Added
      - Alpine 3.18 base


## 0.8.1 2023-05-09 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.83.0


## 0.8.0 2023-04-26 <dave at tiredofit dot ca>

   ### Added
      - Add support for _FILE environment variables


## 0.7.5 2023-04-25 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.82.0


## 0.7.4 2023-04-11 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.81.0


## 0.7.3 2023-04-05 <dave at tiredofit dot ca>

   ### Changed
      - Continued yq fun against max_image_size


## 0.7.2 2023-04-05 <dave at tiredofit dot ca>

   ### Changed
      - Fix some yq oddities


## 0.7.1 2023-04-05 <dave at tiredofit dot ca>

   ### Changed
      - Fix for MAX_IMAGE_PIXELS variable


## 0.7.0 2023-04-05 <dave at tiredofit dot ca>

   ### Added
      - Add ENABLE_MEDIA_REPO environment variable
      - Add MEDIA_DYNAMIC_THUMBNAILS environment variable
      - Impose limits for Maximum upload size, maximum image pixels and maximum spider size
      - Add local and remote media retention capabilities


## 0.6.8 2023-03-30 <dave at tiredofit dot ca>

   ### Added
      - S3 Provider 1.2.1


## 0.6.7 2023-03-28 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.80.0


## 0.6.6 2023-03-14 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.79.0


## 0.6.5 2023-03-08 <dave at tiredofit dot ca>

   ### Changed
      - Fix new installation breaking on backticks in the sample config file


## 0.6.4 2023-02-28 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.78.0


## 0.6.3 2023-02-14 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.77.0


## 0.6.2 2023-01-31 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.76.0


## 0.6.1 2023-01-21 <dave at tiredofit dot ca>

   ### Changed
      - Fix to allow LOG_LEVEL_SHARED_SECRET_AUTHENTICATOR to be updated


## 0.6.0 2023-01-21 <dave at tiredofit dot ca>

   ### Added
      - Add support for Shared Secret Authentication module


## 0.5.0 2023-01-20 <dave at tiredofit dot ca>

   ### Changed
      - Fix x_forwarded header for listeners


## 0.4.0 2023-01-17 <dave at tiredofit dot ca>

   ### Added
      - Add py3-icu from package manager


## 0.0.3 2023-01-17 <dave at tiredofit dot ca>

   ### Added
      - Synapse 1.75.0
      - S3 Provider 0.2.0


## 0.0.2 2022-12-23 <dave at tiredofit dot ca>

   ### Added
      - Add persistence for SECRET_ variables
      - Properly rewrite configuration on restart with yq
      - Save version information for later usage


## 0.0.1 2022-12-22 <dave at tiredofit dot ca>

   ### Added
      - Initial Release
      - Synapse 1.74.0
      - Alpine 3.17 Base
      - Included LDAP3 Provider
      - Included S3 Filesystem Provider
      - Included Rest Password Provider
      - Automatic generation of config, keys, and log information

