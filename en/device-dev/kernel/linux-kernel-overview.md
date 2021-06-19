# Linux Kernel Overview<a name="EN-US_TOPIC_0000001076415984"></a>

-   [Linux Kernel Versions](#section152847516485)
-   [OpenHarmony Kernel Version Selection](#section2716416191715)

OpenHarmony adopts the Linux kernel as the basic kernel for standard-system devices \(reference memory ≥ 128 MB\)  so that appropriate OS kernels can be selected for the devices subject to resource limitations and therefore provide basic capabilities for upper-layer apps.

## Linux Kernel Versions<a name="section152847516485"></a>

Linux kernel versions are classified into the stable version and long-term support \(LTS\) version.

The stable version is released approximately every 3 months to support the latest hardware, improve performance, and fix bugs. Its disadvantage is that the overall maintenance lifespan is short, making long-term stable support unavailable for software.

The LTS version provides long-term kernel maintenance \(in fixing bugs and security vulnerabilities\). Generally, the maintenance lifespan is six years. By contrast, non-LTS kernel versions whose maintenance lifespan ranges from six months to two years cannot cover the entire lifespan of their products and may leave the products open to security vulnerabilities. In addition, new features are not added in the LTS version update, which ensures the version stability. Therefore, LTS versions are more suitable for commercial products that pursue stability and security.

## OpenHarmony Kernel Version Selection<a name="section2716416191715"></a>

You can select an appropriate LTS kernel version as the Linux kernel for OpenHarmony. Currently, LTS version 4.19 is used on most devices. LTS versions 4.4 to 4.14 are old and do not support new features. Additionally, these versions will no longer be maintained in 2023 as planned. In this regard, they can be adopted only by the systems for short-term use but are not suitable for the systems of the first release. The more up-to-date LTS version 5.4 has not been widely used in released products. In comparison, version 4.19 is more well-recognized and can shorten the kernel adaptation period. New versions will be released continuously.

In OpenHarmony, the Linux kernel is recommended for devices whose memory is greater than or equal to 128 MB.

