---
title: Manage ad templates
description: Learn about xxxx.
feature: Creative Templates
---
# Manage ad templates

<!-- It looks like you need a separate template for each combination of ad type (static or dynamic), ad size, and set of ad attributes for a subset of feed files. For example, if you have two feed files, one for Acme Casual Shoes and another for Acme Work Shoes, then create a separate template for dynamic 300x200 ads that use   -->

>[!NOTE]
>
>Once you create an ad template, you can manually create [dynamic ads](/help/creative/creative-libraries/creative-dynamic-manage.md)<!-- and [static ads](/help/creative/creative-libraries/creative-standard-manage.md)--> for an ad template from [!UICONTROL Creative Libraries] > [!UICONTROL Creatives].<!-- How is this different; when would you do it? Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.


opens list

1. **[!UICONTROL Create Ad Template]**

1. Enter the [ad template metadata details](#ad-template-details), including optionally uploading an ad template file that was created externally.<!-- wording -->

1. (If you didn't upload an ad template file) Manually create a static ad or a dynamic ad:<!-- Huh? What's in the uploaded template file? Or do you have the option to either upload a template (such as an existing DCO template) or manually create one? And is this necessary for both types of templates (I see it for dynamic HTML templates but haven't seen a static template yet.)? -->

   1. Enter the basic ad details, and then click **[!UICONTROL Process]**.

   1. Enter the dynamic attributes for the ad, and then click **[!UICONTROL Save]**.

The ad<!-- should usually be multiple, right? --> is generated from template-and-feed file combination and is listed in Creative Libraries > Creatives > Dynamic Ads tab. <!-- huh???? I thought that the generated ads appear as "Catalogs"? -->

## Ad template details {#ad-template-details}

<!-- metadata about the ad template -->

**[!UICONTROL Advertiser]**: The advertiser that can use the ad template.

**[!UICONTROL Ad Template Name]**: A unique name for the ad template.

**[!UICONTROL Ad Template Type]**: The ad template format: *Static HTML* or *Dynamic HTML*. <!-- Define these better. I assume that static is just as-is, and dynamic HTML creates dynamic ads, but verify. -->

**[!UICONTROL Ad Template Size]**: The dimensions of the ads created by the template.<!-- verify -->

**[!UICONTROL Description]**: A description of the ad template. <!-- Use a name that makes it xxx easy to find xxxx ?  -->

**[!UICONTROL Ad template zip]**: The ad template file. Drag and drop a file into the box, and then click **[!UICONTROL Upload]**.<!-- I guess there's no option to browse for a file on your device or network. --> 



## Dynamic ad details {#ad-dynamic-details}

<!-- rename bookmark? -->

### Basic details

**[!UICONTROL Advertiser]**: The advertiser for which ads will be generated.

**[!UICONTROL Library]**: The creative library to which the generated ads will be added.

**[!UICONTROL Dynamic Ad Name]**: The <!-- Clarify -- is this a base name that is incremented with a number or such for each ad that's created? -->

**[!UICONTROL Ad Template Size]**: (Read-only) The ad template format: *Static HTML* or *Dynamic HTML*.

**[!UICONTROL Ad Template Size]**: (Read-only) The dimensions of the ads created by the template.

**[!UICONTROL Ad Template]**: (Read-only) The name of the ad template.

**[!UICONTROL All Catalogs]**: Generates ads from all available feeds for the specified advertiser.<!-- verify -- should this be called "Feeds" or "Feed files?" -->

**[!UICONTROL Catalogs]**: (When [!UICONTROL All Catalogs] isn't selected) One or more of the specified advertiser's feeds from which to generate ads. <!-- Should this be "Feeds?" -->

**[!UICONTROL Advanced Details]**: The types of XXX that can be used XXXX: *[!UICONTROL Profile]*, *[!UICONTROL Geography]*, *[!UICONTROL Segment]*, and/or *[!UICONTROL Datapass]*.<!-- ????? -->

**[!UICONTROL Number of offers]**: The number of XXXXX that can be created for each ad.<!-- Clarify this -- is this the frequency cap (max number of times an ad may be served)? -->

### Attribute details

Identify the names of the columns in the specified catalogs <!-- feed files? --> that correspond to the following attributes.<!-- verify --><!-- will these necessarily all be dynamic?  If static, then no formatting, I guess. -->

**[!UICONTROL backgroundimage]**: The column in the feed file that represents the `backgroundimage` variable. For dynamic values, use the XXX format <!-- ??? --><!-- Demo shows her using `!{background_image}` -- not sure if the actual column name includes the symbols or if it's just `background_image` but the formatting indicates that we're plugging in cell data to create the ads? --> For a static background image that will be used for all ads created, enter <!-- what? How would you indicate this?-->

<!-- I think we'll be listing the column names from the specified feed file, and we'll accept only specific column names for this attribute, so the user will get a small drop-down list to choose from. -->

**[!UICONTROL description]**: The <!-- default? --> ad description.<!-- used how? -->

**[!UICONTROL ctaText]**: <!-- default? --> The text for the ad's call to action<!-- necessarily a call to action button? -->.

**[!UICONTROL clickUrl]**: The variable that allows click-tracking redirects from the generated<!-- ?? --> ads.<!-- Or is this the default landing page for all ads? --> The default landing page URLs are populated from the uploaded feed file creative unit, but you can change the default URLs.

Note: When you include the creative in an experience, you can replace the default
value for any of the click URLs with a custom landing page URL to generate a derivation
of the base creative.

Note: A click tag allows [!DNL Creative] to assign a tracking code to the ad and report
the click-through data.



## Static ad details {#ad-static-details}

<!-- rename bookmark? -->

**[!UICONTROL Advertiser]**:  The advertiser for which ads will be generated.

