# Overview

This Charm deploys [Eclipse Che](http://www.eclipse.org/che/) version 6.0.0-M4 with integration for **developing Juju Charms from your browser**. Eclipse Che is a Next-Generation IDE with a developer workspace server.

Your browser becomes your IDE, your workspaces are docker containers. All the development tools, dependencies and libraries are already installed in the workspace. The only thing you have to do is surf to the url and start coding. To top it all off, you get an in-browser terminal right into your workspace.

# Usage

To deploy the Charm run `juju deploy cs:~tengu-team/eclipse-che`.

Watch it being deployed using `watch -c juju status --color` (close using <kbd>ctrl</kbd>-<kbd>c</kbd>).

```
Model    Controller         Cloud/Region   Version
default  mycontroller       aws/us-east-1  2.0.2

App          Version  Status  Scale  Charm        Store       Rev  OS      Notes
eclipse-che           active      1  eclipse-che  local         2  ubuntu  exposed

Unit            Workload  Agent  Machine  Public address  Ports                     Message
eclipse-che/0*  active    idle   4        56.174.83.54    8080/tcp,32768-65535/tcp  Ready

```

When Che is ready, expose the GUI with `juju expose eclipse-che` and surf to [http://CheIP:8080]().

# Contact Information

## Authors

This software was created in the [IDLab research group](https://www.ugent.be/ea/idlab) of [Ghent University](https://www.ugent.be) in Belgium. This software is used in [Tengu](https://tengu.io), a project that aims to make experimenting with data frameworks and tools as easy as possible.

 - Merlijn Sebrechts <merlijn.sebrechts@gmail.com>
