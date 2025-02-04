---
title: "MDVA-39923: Search by SKU in B2B quick order functionality is case-sensitive"
labels: QPT patches,Quality Patches Tool,QPT,QPT 1.1.2,Magento Commerce 2.4.4,Adobe Commerce 2.4.4,error message,on-premises,cloud infrastructure,SKU,B2B,2.4.1,2.4.1-p1,2.4.2,2.4.2-p1,2.4.2-p2,search
---

The MDVA-39923 patch fixes the issue where customers get an error when they search the order by SKU in B2B quick order functionality with a different case than the one with which the name is saved. This patch is available when the [Quality Patches Tool (QPT)](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching.html#mqp) 1.1.2 is installed. The patch ID is MDVA-39923. Please note that the issue is scheduled to be fixed in Adobe Commerce 2.4.4.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

Adobe Commerce (all deployment methods) 2.4.1-p1

**Compatible with Adobe Commerce versions:**

Adobe Commerce (all deployment methods) 2.4.1 – 2.4.2-p2

>![info]
>
>Note: the patch might become applicable to other versions with new Quality Patches Tool  releases. To check if the patch is compatible with your Adobe Commerce version, run `./vendor/bin/magento-patches status`.

## Issue

Searching by SKU in B2B quick order functionality is case-sensitive and shows an error when a different case is used than the one with which the SKU is saved.

<ins>Prerequisites</ins>:

B2B modules must be installed.

<ins>Steps to reproduce</ins>:

1. Log in to the admin and go to **Stores** > **Configuration** > **B2B**.
1. Enable **Shared Catalog** and **Quick Order**.
1. Create a product with uppercase SKU, e.g., TEST20-1234
1. Assign created product to the **Shared Catalog**.
1. Log in as a customer and click on **Quick Order**.
1. Enter the SKU in lowercase, e.g., test20-1234.

<ins>Expected results</ins>:

The product should be found irrespective of the case used.

<ins>Actual results</ins>:

The following error message is received: *1 product(s) require(s) your attention*.

## Apply the patch

To apply individual patches, use the following links depending on your deployment type:

* Adobe Commerce or Magento Open Source on-premises: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation. 

## Related reading

To learn more about quality patches for Adobe Commerce, refer to:

* [Quality patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492).
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252).

For info about other patches available in QPT, refer to the [Patches available in QPT](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-QPT-tool-) section.
