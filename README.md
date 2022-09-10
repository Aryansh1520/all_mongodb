# Mongodb installation ON Ubuntu 22.04 LTS
## ACTUAL INSTALLATION
### STEP 1: INSTALL gnup if not installed<br/>

```sudo apt-get install gnupg```<br/>

### STEP 2: IMPORT PUBLIC KEY<br/>

```wget -qO - https://www.mongodb.org/static/pgp/server-6.0.asc | sudo apt-key add -```
<br/>
### STEP 3: CREATE A LIST FILE:<br/>

```echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list```
<br/>
### STEP 4: RELOAD PACKAGE DATABASE:<br/>

```sudo apt-get update```<br/>

### STEP 5: SOME ADDITIONAL STEPS (UNSTABLE 22.04 LTS) NOT REQUIRED FOR UBUNTU 20.04 AND BELOW<br/>

```wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2_amd64.deb```<br/>

### STEP 5 : INSTALL THE DOWNLOADED PACKAGES<br/>
```sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2_amd64.deb```<br/>

### STEP 6 : PROCEED WITH INSTALLATION<br/>
```sudo apt-get install -y mongodb-org```<br/>
<br/><br/><br/>
## RUNNING MONGODB
### STEP 1: CHECK
```ps --no-headers -o comm 1```

### STEP 2: IF systemd THEN
```sudo systemctl start mongod```<br/><br/>
```mongosh```

IF init THEN

```sudo service mongod start```<br/><br/>
```mongosh```


