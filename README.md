.plan
=====
A collection of all the ongoing and aspirational technical projects in the team, at least according to me.

Measure Everything
------------------

1. statsd run on Cosmos
2. UDP and HTTP endpoint for statsd
3. Responsive-Web - send back all useful info from the client using Navigation Timing API - Need a list of what we want to track
4. Responsive-Web - send back any interesting data via statsd
5. iBL - send back any interesting data via statsd
6. Visualise the data collected 

Continuous Everything
---------------------
1. Hubson trigger builds for all our projects and need to run on Cosmos
2. Must mirror code of live components from git to Forge SVN
3. SONAR needs to work again for iBL on github
4. 

Gradually morph iPlayer into a client-side web application
----------------------------------------------------------
Currently the iPlayer website is heavily dependent on response cache, i.e. Varnish, to be able to serve the amount of load we get in LIVE. As we make the product more and more personal, we will need to move more and more logic to the client side because it simply won't be scalable to produce a personalised page for every individual user.

1. Devise a set of milestones for which part of the site becomes more javascript-centric (starting with personalised content)
2. Migrate from Spectrum to Moustache as the template language (to avoid duplicated views)
3. Make iBL v2 more javascript client ready (revisit API versioning and caching behaviour)

Move everything to the cloud
----------------------------

1. Build capability to have ad-hoc environments for testing on the cloud / Cosmos
2. Audit all of our tests to make the cloud / Continuous Deployment ready
2. iBL v2 will to be built on the cloud / Cosmos
3. Responsive-web needs to be migrate over to cloud / Cosmos - some open issues to solve, e.g. PHP, sass, static assets, etc.
4. iPlayer Downloads needs to be hosted from S3
5. iPlayer plugins (Tip) need to be hosted from the cloud
6. Find replacement for Varnish (cause it's not on Cosmos at the moment) for response caching for both iBL and Responsive-web (potentially CloudFront)
7. Incorporate our current github Continuous Integration flow into the Cosmos + Jenkins system

IBL version 2 architecture
--------------------------
1. Simplify the code
2. Must be hosted on Cosmos from the get-go
3. Enforce the separation between business logic, data access, and API infrastructure
4. APIs must be validated through some form of API specification
5. The iBL Service-Level-Agreement must be decoupled from the Service-Level-Agreements of dependent services, such as Nitro (need to convince Andy)
6. In order to satisfy 5, we must move to an asynchronous / prefetch data model

Reusable web components for mobile and TVP to embed
---------------------------------------------------
Currently it's pretty much impossible to introduce an iPlayer feature across all platforms at the same time. iBL helps with that, but not much.  
Looking around the industry, companies like Facebook solve this problem by creating re-usable web components that can be easily embedded in the native mobile applications, and only write native-specific code when it's absolutely necessary.


Unify download functionality across platforms
---------------------------------------------
1. Unify the DRM solution on PlayReady
2. Mobile applications need to allow deep-linking so the responsive web download link can open the right application based on the platform
3. Signed and Audio-Described downloads should work across platforms
4. Rationalise download rights across platform

Open Source
-----------
1. Shaun's generic layout stuff for building AS3 SMP plugins
2. iBL java library
3. Responsive Web Design libraries
4. 
