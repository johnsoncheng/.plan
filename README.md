ThePlan
=======

This is where I make public all the technical strategy / technical projects in my head at the moment.

Measure Everything
------------------

1. statsd run on Cosmos
2. UDP and REST endpoint for statsd
3. Responsive-Web - send back all useful info from the client using Navigation Timing API - Need a list of what we want to track
4. Responsive-Web - send back any interesting data via statsd
5. iBL - send back any interesting data via statsd

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
6. Find replacement for Varnish for response caching for both iBL and Responsive-web (potentially CloudFront)
7. Incorporate our current github Continuous Integration flow into the Cosmos + Jenkins system


