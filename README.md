<!---
    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.
-->
cordova-ios-navigationbar
=========================


> The `Navigation bar` object provides some functions to customize the iOS NavigationBar.



Methods
-------

- NavigationBar.create
- NavigationBar.setTitle
- NavigationBar.setLogo
- NavigationBar.show
- NavigationBar.hide
- NavigationBar.init
- NavigationBar.setupLeftButton
- NavigationBar.setupRightButton
- NavigationBar.setLeftButtonEnabled
- NavigationBar.setLeftButtonTint
- NavigationBar.setLeftButtonTitle
- NavigationBar.showLeftButton
- NavigationBar.hideLeftButton
- NavigationBar.setRightButtonEnabled
- NavigationBar.setRightButtonTint
- NavigationBar.setRightButtonTitle
- NavigationBar.showRightButton

Init project
-----------------
cordova plugin add com.karab.cordova.plugin.navigationbar

Exemple JS
----------------

  navBar = cordova.require("cordova/plugin/iOSNavigationBar");

                        navBar.init();    

                        navBar.create('BlackOpaque', {tintColorRgba: '255, 255, 255, 1'});
                        navBar.setTitle("TITLE");
                        navBar.setLogo("www/img/logo.png");

                        navBar.setupLeftButton("Back", null, function () {
                            $window.history.back();
                        }
                         navBar.setLeftButtonTint('75, 70, 95, 25');
                           navBar.setupRightButton(null, "www/img/profil.png",
                            function () {
                                $location.url("/account");
                                scope.$apply();
                            }, {
                                useImageAsBackground: true
                            });
                        navBar.show();



Supported Platforms
-------------------
- iOS


