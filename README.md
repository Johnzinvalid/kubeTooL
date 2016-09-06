# How to use

### Clone this repository to your home directory

```
git clone https://github.com/Johnzinvalid/kubeTooL.git
cd kubeTooL
cp -r .kube ~/.kube
```
The corresponding command line tool kubectl is inside one of the three
folders: _win_, _macOS_, _linux_. add the proper one to your $PATH by
edit .bashrc or .bash_profile.

**Dont forget to use absolute path.**

For Example:
```
export PATH=$PATH:path_to/kubeTooL/corresponding_OS
source .bashrc (or .bash_profile)
```
### Add your password to config file under .kube
use your favorite editor to edit the file _config_ in .kube under your
home directory
```
users:
- name: DOCuser
  user:
    username: DOC login
    password: YourSECRETpassword
...
- context:
    cluster: cluster-sslskip
    namespace: DoC login
```
change the username and password to your DoC login and password,<br>
change the namespace into your login also then save and exit.

Now you can try the command `kubectl get nodes` to check, if it shows
like following then you are ready to go:

```
NAME             STATUS    AGE
146.169.45.206   Ready     33d
146.169.45.207   Ready     33d
