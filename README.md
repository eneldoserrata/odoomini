# odoomini



# Install
```
# apt-get install python-setuptools python-dev
# easy_install pip
# pip install virtualenv
# apt-get install -y zlib1g-dev libxslt1-dev libxml2-dev
# apt-get install -y libsasl2-dev libldap2-dev libssl-dev
# apt-get install -y libtiff5-dev libjpeg8-dev zlib1g-dev libfreetype6-dev liblcms2-dev libwebp-dev 
# apt-get install -y libpq-dev
```

```
$ cd odoomini
$ virtualenv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
$ cp debian/odoo.conf .
```

edit your odoo.conf
```
[options]
; This is the password that allows database operations:
; admin_passwd = admin
db_host = 127.0.0.1
db_port = 5432
db_user = odoo10
db_password = odoo10
addons_path = addons
data_dir = data
```

install db
```
apt-get install postgresql-9.3 postgresql-server-dev-9.3  -y
sudo -u postgres psql
=# create user "odoo10" with password 'odoo10' createdb;
=# \q 

```

run server
```
$ python odoo-bin -c odoo.conf
```
