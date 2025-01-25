# SQL Server

To generate a password, run the following command:

```bash
openssl rand -hex 16
```

Set the permissions of the volume path:

```bash
sudo chown -R 10001:0 ${VOLUME_PATH}
sudo chmod -R 755 ${VOLUME_PATH}
```

Now, to connect, use the `sa` user and the password generated previously.
