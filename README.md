# IBM Verify SDK for iOS

[![SDK Version](https://img.shields.io/badge/version-2.0.2-lightgray.svg)](https://ibm.biz/ibmsecuritymobileaccesssdk)
![Swift Version](https://img.shields.io/badge/swift-4.2-orange.svg)

This repository contains sample apps and code snippets to showcase and provide guidance when developing mobile applications with the IBM Verify SDK. The following steps will help you get started.

[Looking for the Android version?](https://github.com/ibm-security/verify-sdk-android)

<br/>

## ① Getting the SDK

To access the SDK you need to sign in with an IBM ID account.  Create your free [IBM ID](https://www.ibm.com/account/us-en/signup/register.html) and navigate to [IBM AppExchange](https://exchange.xforce.ibmcloud.com/hub/IdentityandAccess) to download the SDK.


<table>
  <tr>
    <th>SDK Version</th>
    <th>iOS 9</th>
    <th>iOS 10</th>
    <th>iOS 11</th>
    <th>iOS 12
    <th>Xcode</th>
    <th>Swift</th>
    <th>End of Target Build Support</th>
    <th>Comments</th>
  </tr>
   <tr>
    <td><a href="CHANGELOG.md">v2.0.2</a></td>
    <td>No</td>
    <td><b>Yes (Targeted)</b></td>
    <td>Yes</td>
    <td>Yes</td>
    <td>>10.0.0</td>
    <td>>4.2</td>
    <td></td>
    <td>Tested on iOS 12.  For access to the SDK or to report a problem with the build, use the GitHub repository <a href="https://github.com/IBM-Security/verify-sdk-ios/issues">issues</a>.</td>
  </tr>
</table>

<br/>

## ② Configuring your environment

The SDK can be used in Xcode.

See our [instructions on configuring your project with the SDK](samples/configuring-your-environment.md).

<br/>

## ③ Deploying your app

The SDK is a Universal Framework that may require some additional steps before deploying to the Apple AppStore.

See our [instructions for deploying your project with the SDK](samples/deploying-your-app.md).

<br/>

## ④ Sample apps and code snippets

> NOTE: Samples are built against v2.0.2 of the SDK.

Available [samples](samples/README.md) and [snippets](snippets/README.md) include:

<table>
    <tr>
        <th width="300px">Name</th>
        <th>Type</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>OAuth token using ROPC grant</td>
        <td><a href="samples/oauth">Sample</a></td>
        <td>This example demonstrates acquiring and refreshing an OAuth token.</td>
    </tr>
    <tr>
        <td>QR code scanning</td>
        <td><a href="samples/qrscan">Sample</a></td>
        <td>This example demonstrates scanning a QR code for one-time password (OTP) generation or multi-factor authentication (MMFA) with ISAM or Clould Identity Verify (CIV).</td>
    </tr>
    <tr>
        <td>Secure key</td>
        <td><a href="samples/securekey">Sample</a></td>
        <td>This example demonstrates generating a private and public key with access control to protect access to the private key.</td>
    </tr>
    <tr>
        <td>Get OAuth token</td>
        <td><a href="snippets#oauthtoken">Snippet</a></td>
        <td> The SDK supports the ROPC grant flow.</td>
    </tr>
    <tr>
        <td>Certificate pinning</td>
        <td><a href="snippets#certpin">Snippet</a></td>
        <td>Compares a certificate stored in the mobile app as being the same certificate presented by the web server that provides the HTTPS connection.</td>
    </tr>
    <tr>
        <td>Key pair generation</td>
        <td><a href="snippets#keypairgen">Snippet</a></td>
        <td>TKey pairs are used in the SDK to sign challenges, coming from IBM Security Access Manager. The private key remains on the device, whereas the public key gets uploaded to the server as part of the mechanisms enrollment.</td>
    </tr>
     <tr>
        <td>Signing data</td>
        <td><a href="snippets#signdata">Snippet</a></td>
        <td>The public key would be stored on a server and provide the challenge text to the client. The client uses the private key to sign the data which is sent back to the server. The server validates the signed data against the public key to verify the keys have not been tampered with.</td>
    </tr>
</table>
<br/>

## &#x2784; IBM Verify

IBM Verify is a mobile app for multi-factor authentication (MFA) with IBM Security Access Manager (ISAM).  IBM Verify features:
- One-time password (OTP)
- Device registration and enrolment
- Multi-tenant services for push notification
- Built on the IBM Security Mobile Access SDK

For more information about IBM Verify, navigate to the [user guide](http://www-01.ibm.com/support/docview.wss?uid=swg27048979).

[![Download on the App Store](res/download-on-the-app-store.png)](https://itunes.apple.com/au/app/ibm-verify/id1162190392?mt=8)
[![Get it on Google Play](res/get-it-on-google-play-store.png)](https://play.google.com/store/apps/details?id=com.ibm.security.verifyapp)

<br/>

## Terms of Support
The Mobile Access SDK for iOS will support continuous delivery for features and security vulnerabilties and defects into the latest stream. Security vulnerabilties and critical defects will be backported into Older SDK Versions. 
_Support_ is defined as fixing of critical security vulnerabilties and defects. _Support_ does not imply new feature enhancements.

| Support Statement | Latest SDK Versions (Xcode 10.0) | Older SDK Versions (Xcode 9.0) |
|-------------------------------------------------------|-----------------|----------------|
| Xcode updates                                         | Yes             | No             |
| Swift updates                                         | Yes             | No             |
| New features                                          | Yes             | No             |
| Security Vulnerabilties                               | Yes             | Yes            |
| Critical Defects                                      | Yes             | Yes            |
| iOS version updates                                   | Yes             | No             |

<br/>

## Security Testing Process
IBM has an internal development and release process for ensuring code quality and to mitigate the risk of vulnerabilities.   As part of the development process, all products are scanned by security vulnerability scanning tools to mitigate the risks of at least the following:  

https://www.ibm.com/support/knowledgecenter/en/SSW2NF_9.0.3/com.ibm.ase.help.doc/topics/r_sans_cwe_top25_report.html

In addition, IBM Security products are developed and tested according to the best practices outlined in the IBM Secure Engineering Framework 

http://www-03.ibm.com/security/secure-engineering/

We do not provide external security certifications for the SDK.  IBM recommends professional security scanning be performed on all mobile apps built with the ISAM SDK.

<br/>

# License

The contents of this repository are open-source under the Apache 2.0 licence. The SDK itself is closed-source.

```
Copyright 2018 International Business Machines

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

```
These sample apps are intended solely for use with an Apple iOS product and intended to be used in conjunction with officially licensed Apple development tools and further customized and distributed under the terms and conditions of your licensed Apple developer program.
```
