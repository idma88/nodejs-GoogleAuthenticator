#nodejs-GoogleAuthenticator

**Google身份验证器node端**

## Installation

``````
npm install google_authenticator --save
``````

## Usage

``````
var googleAuth=require('google_authenticator').authenticator;
var nya=new googleAuth();
``````

# API
## Class:    googleAuth([codeLength=6])
The main class.

 - codeLength:optional,the length of the verifiction code,defaults to 6.



## googleAuth.createSecret([secretLength=16])
To create a random secret string.
> return the secret string.

 - secretLength:optional,the length of the secret string,defaults to 16。




## googleAuth.getCode(secret[,timeSlice])
get the code
> return a string of code consists by numbers.

 - secret:the secret string.
 - timeSlice:optional,specifies the time slice.



## googleAuth.verifyCode(secret,code[,discrepancy=1,currentTimeSlice])
verify the code.
> if verified,return true,otherwise return false.

 - secret:the secret string.
 - code:the verifiction code.
 - discrepancy:the allowed time discrepancy.
 - currentTimeSlice:you know.

## googleAuth.getQRCodeGoogleUrl(name,secret[,title])
get the QR code image using google api.
> return the url of the image.

 - name:the name to display in the GoogleAuthenticator client.
 - secret:the secret string.
 - title:optional,I can't find if this is displayed anywhere.....