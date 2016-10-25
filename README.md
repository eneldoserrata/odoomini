# odoomini



# Install
```
$ cd odoomini
$ virtualenv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
$ cp debian/odoo.conf ..
```

edit your odoo.conf
```
[options]
; This is the password that allows database operations:
; admin_passwd = admin
db_host = 127.0.0.1
db_port = 5432
db_user = odoo
db_password = odoo
addons_path = addons
data_dir = data
```

run server
```
$ python odoo-bin -c odoo.conf
```