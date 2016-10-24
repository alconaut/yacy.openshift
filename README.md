# yacy.openshift
Dockerfile for running YaCy, a peer to peer search engine, on OpenShift Online platform.

### HowTo
#### 1. Create a new project.
#### 2. Open it, and click "Add to Project".
![Project Dashboard](https://github.com/alkchr/yacy.openshift/raw/master/images/001.png)
#### 3. Select "Deploy Image" tab and enter `alkchr/yacy.openshift` as image name.
![Deploy Image](https://github.com/alkchr/yacy.openshift/raw/master/images/002.png)
#### 4. Press "enter" and set a name.
![Name of an Image](https://github.com/alkchr/yacy.openshift/raw/master/images/003.png)
#### 5. Open "Application/Routes" tab and create a new Route.
![Routes Page](https://github.com/alkchr/yacy.openshift/raw/master/images/004.png)
#### 6. Use `8443` as a Target Port, configure "secured routes".
![New Route](https://github.com/alkchr/yacy.openshift/raw/master/images/005.png)
#### 7. Visit your newly installed YaCy instance web-site.
If you have used `passthrough` "TLS Termination mode" in the previous step,
custom unsigned certificates generated by YaCy will be used by default.
So, you may have to add a security exception in your browser.
#### 8. Login using default credentials and change them at `/ConfigAccounts_p.html`.
Default username is `admin` and password is `docker`.
**Note:** *OpenShift Guidline does not encourage to use default credentials
when creating images, however, YaCy uses a custom version of hashing algorithm for passwords
making it impractical to get a hash without running a node of YaCy first.*
*So, login using default user/password pair and don't forget to change them.*
![Changing Credentials](https://github.com/alkchr/yacy.openshift/raw/master/images/006.png)

### License
Distributed under the BSD 2-clause "Simplified" License unless otherwise noted.
