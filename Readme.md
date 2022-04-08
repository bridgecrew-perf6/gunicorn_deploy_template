# Gunicorn systemd configuration

Put this files to ```/etc/systemd/system/```.

Add user to group ```www-data```

```bash
sudo usermod -a -G www-data django
```

Create ```django.conf``` file:
```bash
sudo nano /etc/nginx/conf.d/django.conf
```

Start gunicorn and nginx:
```bash
sudo systemctl enable gunicorn
sudo systemctl start gunicorn
sudo systemctl start nginx
```
