# Commands — Lab 04 Permissions

## Default permissions
touch testfile.txt
mkdir testdir
ls -la

## chmod numeric
chmod 755 testfile.txt
ls -la testfile.txt
chmod 644 testfile.txt
ls -la testfile.txt

## chmod symbolic
chmod u+x testfile.txt
ls -la testfile.txt
chmod u-x testfile.txt
ls -la testfile.txt

## Directory permissions
chmod 700 testdir
ls -ld testdir

## chown
sudo chown root:root testfile.txt
ls -la testfile.txt
sudo chown pushpraj:pushpraj testfile.txt
ls -la testfile.txt

## chgrp
sudo groupadd testgroup
sudo chgrp testgroup testfile.txt
ls -la testfile.txt
sudo groupdel testgroup
