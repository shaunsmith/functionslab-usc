# Environment Setup

For convenience, each lab participant will be provided with an Oracle Cloud
Infrastructure (OCI) virtual machine configured with all the tools you'll need
for this workshop.

Your workshop instructor will provide you with the following:

1. **Workshop Participant Number**--a unique number that will be incorporated
   into your user id
2. OCI **Tenancy Name**--that you will use to log into an OCI cloud account
   (it's "**cloudnative-devrel**"!)
3. OCI **User Id/Password**--to enable you to log into the OCI Console and to
   deploy functions
4. **IP Address**--of your hosted development environment virtual machine
5. **VNC Password**--to allow you to log into your hosted development virual
   machine (it's "**workshop**"!)

> As you make your way through this lab, look out for this icon.
![user input](images/userinput.png) Whenever you see it, it's time for you to
perform an action.

## Pre-requisites

Before we get started you'll need to log into the OCI account you've been
provided to change your password from the temporary initial password.

![user input](images/userinput.png) Log into the OCI console in *Ashburn*
specifying the "**cloudnative-devrel**" tenancy.  

https://console.us-ashburn-1.oraclecloud.com

![Login Tenancy](images/login.png)

![user input](images/userinput.png) Provide your OCI username along with the
initial password you were provided.  

![Login User](images/login-user.png)

![user input](images/userinput.png) Provide a new password satisfying the
requirements and note it down.

![Login New Password](images/login-new-password.png)

## Configuring your Environment

Now that your user account is accessible, let's log into the provided VM.

To access your cloud-based development environment you'll need a VNC client
on your laptop.  You can use whatever you have previously installed or you can
use the VNC Viewer for Chrome that is extremely easy to install through the
Chrome Web Store:

https://chrome.google.com/webstore/detail/vnc%C2%AE-viewer-for-google-ch/iabmpiboiopbgfabjmgeedhcmjenhbla/related

> NOTE: If you're curious about how to setup your own machine to build functions
> and deploy them to Oracle Functions you can follow the instructions in the
> [Quick Start
> Guide](https://www.oracle.com/webfolder/technetwork/tutorials/infographics/oci_faas_gettingstarted_quickview/functions_quickview_top/functions_quickview/index.html#)

![user input](images/userinput.png) Log into your VM using the provided IP
Address and password.  The VNC port is "**5903**" so the server address you'll need
to provide will look like `n.n.n.n:5903`

Enter the provided VNC password "**workshop**" to complete your login.

![vnc login](images/vnc-login.png)


Open a terminal and type the following command to ensure you are using the
`workshop` context that points to Oracle Functions:

![user input](images/userinput.png)
>```sh
>fn ls contexts
>```

Your output should look something like the following:

```shell
CURRENT NAME      PROVIDER  API URL                                         REGISTRY
        default   default
*       workshop  oracle    https://functions.us-phoenix-1.oraclecloud.com  phx.ocir.io/cloudnative-devrel/workshop-NNN
```

Now to make sure you can be authenticated correctly and communicate with Oracle
Functions let's run a command to list all of the existing functions
applications. It doesn't matter what the results are--just that you do get a
result to confirm connectivity.

![user input](images/userinput.png)
>```sh
>fn ls apps
>```

You may see a list of applications something like this:

```shell
NAME        ID
labapp-NNN  ocid1.fnapp.oc1.us-phoenix-1.aaaaaaaaag4h7xotdzz27sp7z23ci6z4jqj4raq43ui6ouae5k2kl7irx34a
```

## All Set!

Now that you're logged into your cloud-based development machine and are able to
communicate with Oracle Functions it's time to get started!

NEXT: [*Java Functions*](1-First-Function.md)

