---
title: Friendly Tag Tutorial D
description: Trololo aksjhd iuert ncv bslirur nty
auto_validation: true
primary_tag: topic>internet-of-things
tags: [ tutorial>beginner, software-product-function>sap-btp-cockpit, products>sap-business-technology-platform, products>sap-btp--cloud-foundry-environment, tutorial>license
primary_tag: topic>internet-of-things ]
time: 864
---
## Prerequisites
 -   You have licensed SAP Internet of Things (with the new capacity unit based licensing introduced in August 2020, your company has a Cloud Platform Enterprise Agreement or Pay-As-You-Go for SAP BTP and you have subscribed to the `oneproduct` service plan)
 -   You have setup the subscription for SAP IoT in your global account in a tenant (e.g. in the DEV tenant, the guide for the basic setup is at [Get Started with Your SAP IoT Account](https://help.sap.com/viewer/195126f4601945cba0886cbbcbf3d364/latest/en-US/bfe6a46a13d14222949072bf330ff2f4.html) ).
 - You have knowledge how to [manage users](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/a3bc7e863ac54c23ab856863b681c9f8.html) and [role collections](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/9e1bf57130ef466e8017eab298b40e5e.html) in the SAP Business Technology Platform
 - Your SAP User has at a minimum the `iot_role_collection` created during onboarding of your tenant and the associated roles (see [SAP Help on Providing Authorizations in](https://help.sap.com/viewer/195126f4601945cba0886cbbcbf3d364/latest/en-US/2810dd61e0a8446d839c936f341ec46d.html) ) and all the required roles for the SAP Internet of Things Edge feature, see [Configure Role Collections for Users](https://help.sap.com/viewer/247022ddd1744053af376344471c0821/2109b/en-US/7e0ddf3d1ef24a42b68cd75fc526302c.html#5f0427eab54d467bb18871ce0d41e862.html)
 -   You have already completed the [initial setup for the Identity Authentication Service](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/31af7da133874e199a7df1d42905241b.html)
 -   You have already completed to [Onboard an Edge Node](iot-edge-onboard-node)

## Details
### You will learn
  - How to get Device Connectivity details
  - How to create an onboarding certificate

---

[ACCORDION-BEGIN [Step 1: ](Get Device Connectivity details)]

This step will show you how to get some service details to connect correctly your Edge Gateway Service to the SAP IoT tenant.

1.  Open The Business Technology Platform and navigate to the SAP IoT sub-account.

2.  Open **Instances and Subscriptions**

    !![btp](btp.png)

3.  Click in the column **Credentials** for the instance of SAP IoT on the field **X Keys** to open the service keys.

    > If there are no key available for SAP IoT, you need to create them, see [Create service keys](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cdf4f200db3e4c248fa67401937b2f78.html)

    !![servicekey](servicekey.png)

4.  A set of keys written as JSON object are shown. Scroll the list and search for the node `iot-device-connectivity`.

5.  Copy in an empty document the value of `tenantid`, you will need it later.

6.  Copy the address of the `mqtt` or `rest` field (i.e.: `XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX.eu10.cp.iot.sap`).

7.  Split the address in two parts: the `hostname` (i.e.: `XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX`) and the `domain name` (i.e.: `eu10.cp.iot.sap`) and save them in the document with the `tenantid`.

[DONE]
[ACCORDION-END]
