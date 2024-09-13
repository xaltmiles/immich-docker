To start:

- rename .example.env to .env and configure environmental variables for the setup
- To mount external libraries, mount volumes in docker-compose.yml services/immich-server/volumes, e.g.  C:/data/media/photo/2023:/mnt/photos1 or C:/data/media/photo/2023:/mnt/photos1:ro
  - In this setup, external libraries must be added through immich ui (use path /mnt/photos1)
  - Mounting external volumes is explained in [](https://immich.app/docs/guides/external-library)
- database must be stored in docker-internal volume (e.g. immich_db, as configured in docker-compose.yml) for file system compatibility, as explained in here [](https://immich.app/docs/install/environment-variables#supported-filesystems)
