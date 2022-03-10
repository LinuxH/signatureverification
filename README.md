# The Signature Verification Project

**The Signature Verification Project researches the verification of digital handwritten signatures on commonly used mobile devices.** 

As part of the [contributions](#contributions) of our work, we introduce the worlds largest publicly available mobile signature databases and usability studies that we know of with over 10400 signatures by 73 participants, provide open-source scientific signature recording applications for two platforms, and propose a multi-staged processing toolchain and verification algorithm. 

With our research documented in the corresponding master’s thesis, we [answer](#summary-of-results) multiple open [research questions](#research-questions) on a) the viability of notebook touchpads as a signing platform, b) the value of additional hand-movement information obtained while signing on smartphones for verification performance, and c) the comparative usability of signing on a notebook touchpad vs. signing on a smartphone.

## Overview

_This is the main repository for The Signature Verification Project. It provides an overview and contains the full-text thesis detailing our research and results, links to the repositories of each individual part of the project, and a download link and instructions for the signature database. **Currently, a scientific paper is in preparation that will also be made available here after its publication later this year (2022).**_

To learn more about our approach, our dataset, and our results, start with the masters thesis provided in this repository, which discusses every aspect in great detail.

To use our applications for your own research, please take a look at the repositories for the Android mobile recording app and the touchpad recording application, as well as our toolchain and verification algorithm implemented in python. All our applications are well documented and built to be easily use- and adaptable. Links are provided below.

To use our signature and/or usability datasets for your own research, please contact **linus dot heimboeck at gmail dot com** and briefly describe the goals and purpose of your project. If it is a non-profit project and your results will be made publicly available, we will happily give you access to any data you need.
  
Repository Links:
-	[Touchpad Signing](https://bitbucket.org/linuspersonal/touchpad-signing/)
-	[Verification Algorithm and Processing Toolchain](https://bitbucket.org/linuspersonal/sig-rec-impl/)
-	[Android Signing Application](https://bitbucket.org/linuspersonal/recording-app-android/)
  
A ready-to-use version of the Android recording application is available for download on the [Play Store](https://play.google.com/store/apps/details?id=at.fhooe.mc.linusheimboeck.recordingapp)

Our fully processed signature database is available for download [here](https://drive.google.com/file/d/1PnUdYPjuBTDTqQh5GfnsPXLBVE7W0sUm/view?usp=sharing). For additional data, other versions of the database, or access to the raw, unprocessed signature files, please contact us directly.

## Purpose

A person’s handwritten signature is a unique behavioral biometric trait that is legally and culturally accepted worldwide as proof of identity and consent. 

If we are able to reliably verify handwritten signatures on commonly used mobile devices such as smartphones and notebook touchpads, signatures have the potential to be used for authentication just like a fingerprint. This enables a wide variety of use cases, from simple unlocking mechanisms, over password-less logins with legal significance (eg. for banks, government administration, etc.) to secure handwritten document signing and much more.

## Research Questions

The work in The Signature Verification Project is organized around the following research questions that are answered in chapter 8.3 of the thesis ([very briefly summarized here](#summary-of-results)):
- How does the verification performance of signatures drawn with a finger on an integrated notebook touchpad compare to signatures drawn on a smartphone screen?
- Does the combination of image-based and movement-based dynamic features of a signature drawn on a mobile device improve verification performance over only image-based or only movement-based systems, and how do the individual features contribute to the final performance?
- How is the usability of signing with a finger on an integrated notebook touchpad, especially with regard to the indirect visual feedback and the narrow shape of the touchpad, and how does it compare to signing on a mobile phone screen?

In addition to the research questions stated above, this work also contributes to or answers further questions that have been asked in related work:
- It explores the size of the finger contact area on screen (touchsize) as a potential additional screen-based feature, something that has been suggested as a potential substitute for pressure [122] and not been considered so far [36, 64].
- It studies the interoperability of signature templates and individual signature features between devices [64].
- It considers the influence of different signing positions and enrollment scenarios, which have not been evaluated in time-series based signature verification yet.

## Contributions

The Signature Verification Project contributes to signature verification on mobile devices with five interconnected parts that can be summarized as follows:
  
- _**The creation of a multi-modal extensible mobile signature database:**_ To the best of our knowledge, there is currently no other publicly available signature database that comprises both time-series signature information and time-series movement information from different embedded sensors acquired while signing. The lack of such a database on which to conduct research has also been pointed out in related work [64], and its recording and publishing is part of the thesis.
- _**The development and open-source publication of recording tools and classification algorithm:**_ We designed a) the first publicly available scientific signature recording applications for phones and notebook touchpads that we are aware of, and b) the Multi-Dimensional Dynamic Time Warping (MD-DTW) algorithm as a method of distance calculation between signatures. Both our implementations and our database are made available open source.
- _**The evaluation of integrated notebook touchpads as a platform for signature verification:**_ This thesis is the first to explore the authentication of finger-drawn handwritten signatures on notebook touchpads. The only similar work we know of has investigated the classification of made-up paraphs in 2008 [6] on a resistive touchpad. We compare our results to the verification performance on handheld mobile devices and evaluate touchpads as a platform for digital signing.
- _**The execution of comparative usability studies on handwritten mobile signing:**_ We conducted the first usability study on touchpad signatures, and with 71 respondents the largest one on mobile phones. We demonstrate the viability of touchpads a possible platform for dynamic signature verification, point out differences between the device categories, and discuss both their potential benefits and problems.
- _**The evaluation of movement data as additional biometric information for signature verification:**_ We systematically evaluate movement data as a biometric feature in the context of handwritten signatures. The data is recorded unobtrusively from the phones embedded sensors while the user is drawing their signature on the device screen as time series. It is then used on its own and in different combinations of signature image and individual sensor features in local and global scenarios for classification and the difference in performance is measured.

## Summary of Results

Our evaluation shows that touchpads and mobile phones perform equally well under the same conditions, at about 5.75% EER against skilled forgeries. However, mobile phones have the potential to perform better in when used in different positions and when using additional features. We find that the inclusion of movement information results in improvements of 0.6% to 2% EER over only image-based signature data. The best average result under ideal conditions on combined data against skilled forgeries is at 2.59% EER, the best individual result at 1.79% EER. 

Our usability studies on both device classes show that while most users prefer signing on a mobile phone, 25% find the touchpad more comfortable, and an additional 13% did not have a preference. Over 55% reported that they would be likely to use touchpad signing in their daily life for signing digital documents. Overall, we find that movement data is valuable as additional biometric information for verification, and that the touchpad is a viable platform for digital signing.

