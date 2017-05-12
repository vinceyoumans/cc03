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


The documented CURL command is wrong...
but this is working to individual phones...


curl -X POST -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqdGkiOiI2Mzc5MTM0MC01MmNiLTRmOWQtYTM5YS1lYjQ5ZDliNDQxN2EifQ.k4madyXfkzWfWP9libaPhLJM20Ak0pUEkY-hwy3nnOI" -H "Content-Type: application/json" -d '{
    "tokens": ["e08b46bd0ce07b3a755d71018f397b1982505a8ee86b06288f84f0bf9b0393e6"],
    "profile": "develios",
    "notification": {
        "message": "This is my demo push!"
    }
}' "https://api.ionic.io/push/notifications"



eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqdGkiOiI2Mzc5MTM0MC01MmNiLTRmOWQtYTM5YS1lYjQ5ZDliNDQxN2EifQ.k4madyXfkzWfWP9libaPhLJM20Ak0pUEkY-hwy3nnOI

e08b46bd0ce07b3a755d71018f397b1982505a8ee86b06288f84f0bf9b0393e6

This works for iOS




