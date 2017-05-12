# cc03
This is an IONIC v2 Example of integrating PUSH into iOS.
Android is not included in this documentation, but I predict it should eb the same.

The routine to get to this point is different than official Documents.

The specific changes include...

removing the default IOINC-iOS library as the default 4.1.1 version is not compatible with the latest phone-gap version.

Re-add iOS support to get to at least 4.3.1.  In this case, using 4.3.3

The new Phone gap is actually using CocoPods.
Thus, from xCode you should launch from cc03.xcworkspace  NOT the normal cc03.xcodeproj


The third warning is that the IONIC documented way of manually provisioning credentials did not work for me.  Infact, it messed my certs up more.  Instead, use the xCode Automatic Cert provisioning, which is a new feature in xCode.

This sums up the main differences from the Docs...  but I also added additional code features.



My Curl Commands look like this...
But not working...   thougths?
curl -u PRIVATE_API_KEY: -H "Content-Type: application/json" -H "X-Ionic-Application-Id: 2be74c3c " https://push.ionic.io/api/v1/push162 -d '{"tokens": "df902aff9cf46bd9078854f442fc711092da76dfcb5a7fd5482e4d7e51b051f0"],"notification":{"alert":"I come from planet Ion."}}'


curl -u PRIVATE_API_KEY: 
-H "Content-Type: application/json" 
-H "X-Ionic-Application-Id: 2be74c3c " https://push.ionic.io/api/v1/push162 -d '{"tokens": "df902aff9cf46bd9078854f442fc711092da76dfcb5a7fd5482e4d7e51b051f0"],"notification":{"alert":"I come from planet Ion."}}'





