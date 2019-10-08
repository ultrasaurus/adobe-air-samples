
```
mkdir hello && cd hello
touch hello-app.xml
touch hello.html
cp ../frameworks/libs/air/AIRAliases.js .

# test
../bin/adl hello-app.xml 

# build
../bin/adt -certificate -cn SelfSigned 1024-RSA sampleCert.pfx samplePassword
../bin/adt -package -storetype pkcs12 -keystore sampleCert.pfx hello.air hello-app.xml hello.html AIRAliases.js
```