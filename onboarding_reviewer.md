# Onboarding Guide for Reviewers

<div class="summaryblock">
<p>Thanks for accepting to review a package for rOpenSci! This chapter consists of our guidelines to <a href="#preparereview">prepare</a>, <a href="#submitreview">submit</a> and <a href="#followupreviewer">follow-up</a> on your review.</p>
<p>You might contact the editor in charge of the submission for any question you might have about the process or your review.</p>
<p>Please strive to complete your review within 3 weeks of accepting a review request. We will aim to remind reviewers of upcoming and past due dates. Editors may assign additional or alternate reviewers if a review is excessively late.</p>
</div>

## Preparing your review {#preparereview}

### General guidelines

To review a package, please begin by copying our [review template](#reviewtemplate) and using it as a high-level checklist.  In addition to checking off the minimum criteria, we ask you provide general comments addressing the following:

- Does the code comply with general principles in the [Mozilla reviewing guide](https://mozillascience.github.io/codeReview/review.html)?
- Does the package comply with the [rOpenSci packaging guide](#building)?
- Are there improvements that could be made to the code style?
- Is there code duplication in the package that should be reduced?
- Are there user interface improvements that could be made?
- Are there performance improvements that could be made?
- Is the documentation (installation instructions/vignettes/examples/demos) clear and sufficient?
- If you you have your own relevant data/problem, work through it with the package. You'll find rough edges and use-cases the author didn't.

Please be respectful and kind to the authors in your reviews. Our [code of conduct](#code-of-conduct) is mandatory for everyone involved in our review process. We expect you to submit your review withing 3 weeks, depending on the deadline set by the editor. Please contact the editor directly or in the submission thread to inform them about possible delays.

We encourage you to use automated tools to facilitate your reviewing.  These include:

-  Checking the package's logs on its continuous integration services (Travs-CI, Codecov, etc.)
-  Running `devtools::check()` and `devtools::test()` on the package to find any errors that may be missed on the author's system.
-  Using the **covr** package to examine the extent of test coverage.
-  Using the [**goodpractice**](https://github.com/MangoTheCat/goodpractice) package (`goodpractice::gp()`) to identify likely sources of errors and style issues. Most exceptions will need to be justified by the author in the particular context of their package.
-  Using `devtools::spell_check()` to find spelling errors in DESCRIPTION and manual files, and RStudio's spellchecker to find spelling errors in vignettes and README files.

### Experience from past reviewers

First-time reviewers may find it helpful to read (about) some previous reviews. In general you can find submission threads of onboarded packages [here](https://github.com/ropensci/onboarding/issues?q=is%3Aissue+is%3Aclosed+label%3A6%2Fapproved). Here are a few chosen examples of reviews (note that your reviews do not need to be as long as examples):

* `rtika` [review 1](https://github.com/ropensci/onboarding/issues/191#issuecomment-367166658) and [review 2](https://github.com/ropensci/onboarding/issues/191#issuecomment-368254623)

* `NLMR` [review 1](https://github.com/ropensci/onboarding/issues/188#issuecomment-368042693) and [review 2](https://github.com/ropensci/onboarding/issues/188#issuecomment-369310831)

* `bowerbird` [pre-review comment](https://github.com/ropensci/onboarding/issues/139#issuecomment-322713737), [review 1](https://github.com/ropensci/onboarding/issues/139#issuecomment-342380870), [review 2](https://github.com/ropensci/onboarding/issues/139#issuecomment-342724843).

* `rusda` [review](https://github.com/ropensci/onboarding/issues/18#issuecomment-120445737) (from before we had a review template)

You can read blog posts written by reviewers on our blog [via this link](https://ropensci.org/tags/reviewer/). In particular, in [this blog post by Mara Averick](https://ropensci.org/blog/2017/08/22/first-package-review/) read her take about the "naïve user" role a reviewer can take to provide useful feedback even without being experts of the package's topic or implementation, by asking themselves _"What did I think this thing would do? Did it do it? What are things that scare me off?"_. In [another blog post](https://ropensci.org/blog/2017/09/08/first-review-experiences/) Verena Haunschmid explains how she alternated between using the package and checking its code.

As both a former reviewer and package author [Adam Sparks](https://adamhsparks.github.io/) [wrote](https://twitter.com/adamhsparks/status/898132036451303425) wrote "[write] a good critique of the package structure and best coding practices. If you know how to do something better, tell me. It’s easy to miss documentation opportunities as a developer, as a reviewer, you have a different view. You’re a user that can give feedback. What’s not clear in the package? How can it be made more clear? If you’re using it for the first time, is it easy? Do you know another R package that maybe I should be using? Or is there one I’m using that perhaps I shouldn’t be? If you can contribute to the package, offer."

### Feedback on the process

We encourage you to ask questions and provide feedback on the review process on our [forum](https://discuss.ropensci.org). 

## Submitting the Review {#submitreview}

- When your review is complete, paste it as a comment into the package onboarding issue.
- Additional comments are welcome in the same issue as a package onboarding request. We hope that package reviews will work as an ongoing conversation with the authors as opposed to a single round of reviews typical of manuscripts.
- You may also submit issues or pull requests directly to the package repo if you choose, but if you do, please comment about them and link to them in the onboarding repo comment thread so we have a centralized record and text of your review.
- Please include an estimate of how many hours you spent on your review at the end of your review.

## Review follow-up {followupreviewer}

Authors should respond to the review within 2 weeks with their changes to the package in response to your review.  At this stage, we ask that you respond as to whether the change sufficiently address any issues raised in your review. We encourage ongoing discussion between package authors and reviewers, and you may ask editors to clarify issues in the review thread, as well.