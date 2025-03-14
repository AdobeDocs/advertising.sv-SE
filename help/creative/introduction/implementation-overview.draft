---
title: Overview of implementing Adobe Advertising Creative
description: Learn about the basic workflow for implementing [!DNL Creative].
feature: Creative Introduction
---
# Overview of implementing Adobe Advertising Creative

*Closed beta*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

The [!DNL Creative] operations team works with each advertiser to set up its creatives and creative experiences, either implementing the ad experiences as ads within your DSP or providing your team with the third-party ad tags to implement themselves, and validating the initial cost, click, and conversion data.

On an on-going basis, the Adobe Account Team, the agency team, or the advertiser (depending on the terms of the service level agreement) need to monitor each experience and to edit it as necessary to meet the advertiser's goals.

## Initial Setup Tasks for [!DNL Creative] Campaigns <!-- Experiences? "Campaigns" may be confusing now. -->

The implementation team and/or your agency will work with you do the following:

1. Define your personalization goals (such as whether you'll personalize ads for prospecting or retargeting); all first-, second-, and third-party data that's available, including creative assets, audience segments, and CRM data <!-- used how/where? -->; and your strategy for achieving your goals.

1. (New advertiser accounts) Set up administrative accounts:

   1. Set up the advertiser's account for [!DNL Creative]<!-- and/or DSP? -->, and also create an account in Advertising Search.
   
      The [!DNL Creative] account setup is within Advertising  DSP, even if the advertiser isn't a DSP customer.
      
      Similarly, even if the advertiser isn't a [!DNL Search] customer, the [!DNL Search] account is used to create conversion tracking tags and set up conversion columns in [!DNL Creative].

   1. (If necessary) Create user accounts for the advertiser to view and manage its creatives and ad experiences and to generate reports.

1. (Optional) If you want to create first-party audience segments to include as targets for your creatives, then create the tags in either of the following ways:

   * [Create retargeting pixels](/help/creative/pixels/retargeting-pixel-manage.md) to retarget ads to visitors with specific attributes to specific landing pages or conversion pages, and then generate tags to insert in the relevant web pages.
   
   * (Advertisers with DSP) Within DSP, [create custom audience segments](/help/dsp/audiences/custom-segment-create.md) to track all visitors to specific landing pages or conversion pages, and then generate tags to insert in the relevant web pages.

   Both types of tags are image tags, which display a 1-pixel x 1-pixel transparent image (pixel), which is invisible to end users, on the web page on which they are added. Later, you can configure creatives in an ad experience to target specific retargeting pixels or segments, so that the relevant ad elements are displayed only to users who previously visited site pages associated with the pixel or segment.
   
   The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.
   
   **Note:** You can also use your first-party audiences from Adobe Audience Manager and Adobe Analytics as creative targets. Once a visitor qualifies for an audience shared from [!DNL Analytics], the information is actionable in [!DNL Creative] in about 24-48 hours. <!--Still true? And what about AAM and DSP? -->

1. Set up ad experiences based on your advertising goals:

   * **Automation workflow:**  The [!DNL Creative] operations team can create dynamic ads for your organization using ad templates and data feeds.

     For more information, talk to your Adobe Account Team.
     
     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Manual workflow:** Manually set up ad experiences:
   
     1. Set up creatives to use in your experiences:
     
        * For creatives that [!DNL Creative] will host, upload them.<!-- Add x-ref and reword if necessary to cover all cases -->
        
        * For creatives hosted on a supported third-party ad server, [point to the creative files](/help/creative/creative-libraries/creative-third-party-manage.md).

     1. (Optional) [Group creatives into bundles](/help/creative/creative-libraries/bundle-manage.md) that you can attach to experiences in one step.
   
     1. Sequence creatives and optional ad targets as [ad experiences](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->
     
       Ad targets can include retargeting pixels that you create in [!DNL Creative]; your audience segments in Adobe Experience Cloud (including in DSP, Audience Manager, or [!DNL Analytics]); geographic targets; or specific data triggers on the web page (such as SKU=01234567890123 or Cart=empty).<!-- I don't see audience segments available, and I see radius targets (which doesn't work) but not other geo targets -- verify all these. -->

1. Set up conversion tracking for your ad experiences:


Set up conversion tracking. Depending on the implementation, this may involve adding
conversion tracking tags to the advertiser's web pages and/or setting up a daily
feed drop for conversion data that the advertiser has collected separately.


You can generate Advertising Cloud conversion tracking tags within Advertising Cloud
Search or within Adobe Dynamic Tag Manager (formerly called Dynamic Tag Manager).
Note: You must use JavaScript conversion tags, not image tags.


The advertiser's IT department or other group may need to schedule, or be informed
about, the tag deployment.


(Optional) Within Advertising Cloud Search, make each conversion (transaction property)
available as an individual column set in data views and reports.


A conversion (transaction property) is listed in Advertising Cloud Search after at
least one conversion event has been tracked.


If you don't make specific metrics available, then all conversions are consolidated
in one "Conversions" column set.


Validate the data that is tracked.


(Optional) Set up delivery of scheduled reports to specified email addresses.


For instructions, see the help chapter on "Reports."


Set up ad campaigns on Advertising Cloud DSP or another DSP, and provide JavaScript
or iframe tags for the ad experiences to the advertiser, who can implement them as
third-party ads in the DSP.


Monitor the performance of your completed ad experiences, either viewing predefined
performance details for individual experiences or creating custom performance reports.


(As needed) Update ad experiences based on performance and updated messaging.






>[!MORELIKETHIS]
>
>* [About Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
