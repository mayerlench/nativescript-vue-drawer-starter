##### Create a keystore
`keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000`

##### Create Android App Bundle
```
tns build android --release --key-store-path C:\Users\mykey.keystore --key-store-password <pass> --key-store-alias <alias_name> --key-store-alias-password <pass> --aab --copy-to aab.aab
```
##### Run aab on device
```
tns run android --key-store-path C:\Users\mykey.keystore --key-store-password <pass> --key-store-alias <alias_name> --key-store-alias-password <pass> --aab
```

##### Generate key for app siging in google
```
java -jar pepk.jar --keystore=C:\Users\mykey.keystore --alias=<alias_name> --output=encrypted_private_key_path --encryptionkey=<getThisFromGoogle>
```


