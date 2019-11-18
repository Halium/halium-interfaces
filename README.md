Halium interfaces
=================

This repository contains the interface of Halium's Android. To make sure that everyone is on the same page, the interface is set so that everyone knows what's provided by Halium's Android.

How Halium interface documents work
-----------------------------------

As mentioned in [Halium's scope](https://docs.halium.org/en/latest/project/Scope.html), Halium's interfaces are devided into 3 categories:
  1. Native Android interfaces.
  2. Libhybris compat layer.
  3. Custom interfaces.

In each category, the interfaces are listed. Each interface will contain the following entries:
  - Description: describe what the interface does.
  - Defined by: if the interface can be provided by multiple providers (such as native HALs from device manufacturers), a link to the interface definition(s) should be provided.
  - Provided by: link to repository or path within the repository that provides such interface.
  - Consumed by: the middleware which comunicates with this interface. If the consumer varies between distributions, a couple of examples should be enough. Only one of "Defined by", "Provided by" or "Consumed by" is required.
  - Note: can be provided to document the additional dependency(ies), the reason this (custom) interface is required, or any other kind of notes.

As Android base system can involve significantly between releases, each version of Halium's Android will have its own version of interface document. Distributions that use Halium's Android can support more than 1 version at a time. In many instances, such a support is provided in the middleware itself. For some instances, distributions may have to use other technique (such as multiple rootfs or multiple binaries of the same software) to do the job.

Distributions are discouraged to use something else not documented by the interface. If a distrubution would like to take advantage of something provided by the Android system image but isn't documented in the interface, such distribution should take some time to document it.

Currently, the version defined in this repository is:
  - [Halium 7.1](/interfaces/halium-7.1.md)
