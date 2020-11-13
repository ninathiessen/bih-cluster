# The Open OnDemand Portal

!!! important "Status / Stability"

    OnDemand Support is currently in **beta** phase on the BIH HPC.
    In case of any issues, please send an email to hpc-helpdesk@bihealth.de.

To allow for better interactive works, BIH HPC administration has setup an  [Open OnDemand (OOD)](https://openondemand.org/) portal web server.

- https://portal.research.hpc.bihealth.org

## Background

OOD allows you to access cluster resources using a web-based graphical interface in addition to traditional SSH connections.
You can then connect to jobs running graphical applications either to virtual desktops (such as Matlab) or to web apps (such as Jupyter and RStudio Server).

The following figure illustrates this.

![](figures/ondemand-overview.png){: style="width:60%;" .center}

The primary way to the cluster continues to be SSH which has several advantages.
By the nature of the cluster being based on Linux servers, it will offer more features through the "native" access and through its lower complexity, it will offer higher stability.
However, we all like to have the option of a graphical interface, at least for time to time :tv:.

The main features are:

- **Easy web-based access to Jupyter and RStudio Server on the cluster.**
- Generally lower the entry barrier of using the HPC system.

## Logging into the Portal

The first prerequisite is to have a cluster account already (see [Getting Access](/admin/getting-access/)).
Once you have done your first SSH connection to the cluster successfully you can start using the portal.
For this you perform the following steps:

1. Go to https://portal.research.hpc.bihealth.org - you will be redirected to the login page shown below.
   If you have an account with Charite (ends in `_m`) then please use the "Charité - Universitätmedizin Berlin" button, for MDC Accounts please use the "Max Delbrück Center Berlin" button.

    ![](figures/ondemand-hpc-sso.png){: style="width:30%;" .center}
2. Login with your home organization's SSO system.
   Please note that depending on whether you are accessing the system via the wired network in your home organization or via VPN the SSO might look differently.

    !!! help "Clicked the Wrong Login Button?"

        If you clicked the wrong button then please clear your cookies to force a logout of the system.

## Portal Dashboard

!!! help "Problems with Open OnDemand?"

    First try to log out and login again.
    Next, try to clear all cookies for the domain `portal.research.hpc.bihealth.org`.
    Finally, try the `Help > Restart Web Server` link to restart the per-user nginx (PUN) server.

You will then be redirected to the dashboard screen.

![](figures/ondemand-dashboard.png){: style="width:60%;" .center}

Here you have access to the following actions.
We will not go into detail of all of them and expect them to be self-explanatory.

!!! important

    Please note that when using the portal then you are acting as your HPC user.
    Use standard best practice.
    Consider carefully what you do as you would from the command line (e.g., don't use the portal to browse the web from the cluster).

- **Files** - access a file browser
    - **Quotas** - display quota information.
- **Jobs** - list your jobs or start a new one
- **Clusters** - shell access in your browser
- **Interactive Apps**
    - **Mate and Xfce Desktops** - start virtual desktops on the HPC.
    - **Matlab** - run a virtual desktop that has Matlab installed.
    - **MaxQuant** - run a virtual desktop that has MaxQuant installed
    - **Jupyter** - run Jupyter on the HPC and easily connect to it from your browser without setting up any SSH tunnels
    - **RStudio Server** - run RStudio Server on the HPC and easily connect to it from your browser without setting up any SSH tunnels
- **My Interactive Sessions** - see details of your currently running interactive sessions
- **Help**
    - **Online Documentation** - links to this documentation.
    - **Contact Support** - links ot the "Getting Help" page in this documentation.
    - **Restart Web Server** component. Try this if the portal acts weird before contacting the helpdesk. OnDemand runs a web server per user, so this does not affect any other user.
- **Log Out** - log out of the system.