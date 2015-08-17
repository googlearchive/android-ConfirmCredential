
Android Confirm Credential Sample
===================================

A sample that demonstrates how to use device credentials (PIN, Pattern, Password) in your app

Introduction
------------

This sample demonstrates how you can use device credentials (PIN, Pattern, Password) in your app
to authenticate the user before they are trying to complete some actions.

First you need to create a symmetric key in the Android Key Store using [KeyGenerator][1]
which can be only be used after the user has authenticated after the user is authenticated
with their device credentials and pass [KeyGenParameterSpec][2].

By setting an integer value to the
[KeyGeneratorSpec.Builder.setUserAuthenticationValidityDurationSeconds][3], you can consider the
user as authenticated if the user has been authenticated with the device credentials
within the last x seconds.

Then by calling [KeyguardManager.createConfirmDeviceCredentialIntent][4], you can show a screen
to confirm device credentials to the user.

[1]: https://developer.android.com/reference/javax/crypto/KeyGenerator.html
[2]: https://developer.android.com/reference/android/security/KeyGenParameterSpec.html
[3]: https://developer.android.com/reference/android/security/KeyGenParameterSpec.Builder#setUserAuthenticationValidityDurationSeconds().html
[4]: https://developer.android.com/reference/android/app/KeyguardManager.createConfirmDeviceCredentialIntent().html

Pre-requisites
--------------

- Android SDK v23
- Android Build Tools v23.0.0
- Android Support Repository

Screenshots
-------------

<img src="screenshots/1-purchase.png" height="400" alt="Screenshot"/> <img src="screenshots/2-show-confirm-credential.png" height="400" alt="Screenshot"/> <img src="screenshots/3-already-authenticated.png" height="400" alt="Screenshot"/> 

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.

Support
-------

- Google+ Community: https://plus.google.com/communities/105153134372062985968
- Stack Overflow: http://stackoverflow.com/questions/tagged/android

If you've found an error in this sample, please file an issue:
https://github.com/googlesamples/android-Confirm Credential

Patches are encouraged, and may be submitted by forking this project and
submitting a pull request through GitHub. Please see CONTRIBUTING.md for more details.

License
-------

Copyright 2014 The Android Open Source Project, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
