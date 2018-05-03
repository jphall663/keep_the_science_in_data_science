# Keep the Science in Data Science

#### Patrick Hall, 2014

Data science is a phrase that is used too often. It has no clear definition because it has been defined differently by so many different people and organizations. Moreover, simply labeling something a science doesn’t make it so.

With the phrase “data science” being applied to so many different kinds of pursuits, isn’t there a danger that the burgeoning field could become more pseudo-science rather than real science? Those of us who practice the discipline seriously and professionally have a responsibility to ensure that data science is more than nominally scientific.

To transform an informal practice into something that is widely regarded as a science requires the diligent efforts of numerous people over the span of years, if not decades. One short article is an infinitesimal effort toward that end, but I’d still like to present a few lessons I’ve learned, usually the hard way, in an attempt to use the scientific method in my work.

**Form a measurable hypothesis**

Forming a measurable hypothesis has two direct corollaries:
* Work from a previously measured, or somehow quantifiable, benchmark or control.
* Use an appropriate assessment method.

When faced with a data-oriented problem or task, formulate that problem or task into a measurable hypothesis. Otherwise you risk wasting time or even making the situation worse.

Here’s an example of how an unmeasurable hypothesis could get you into trouble. Let’s say your data science startup is launching a new web service. You may think, “A new recommendation system will definitely increase the usage of our new web service,” but there are several issues with that unmeasurable hypothesis.

First, since both the service and the recommender would be brand new, you have no benchmark or control to measure whether adding a recommendation system to your new service is actually increasing the use of the service.

Second, maybe your recommendations wouldn’t be so great at first and they might actually drive people away from your website and service.

Third, you will probably derive more revenue from advertisements on your website than from people using your service, so increased revenue is probably a better measure of success than increased use of your web service.

If you followed through with this unmeasurable hypothesis, you could never know if a recommendation system actually increased the use of your service. More importantly, you could never know if the recommendation system increased your revenue.

A better approach would be to launch your web service and record revenue without the recommendation system. Once a benchmark has been established, you could form the more measurable hypothesis, “A recommendation system will increase revenue.”

**Gather information**

Gathering information usually means conducting a literature review. Data science *might* be new, but applied math, statistics, machine learning and optimization have been around for a long time. Most likely, someone really smart has already done a really good job at whatever it is you are trying to do. If so, use their approach first as benchmark or control. If not, you should still read about subjects related to your task or problem to avoid the pitfalls and leverage the discoveries of the scientists who came before you.

Continuing with the recommendation system example, you and your team might save time in the short-term by starting to code a recommendation system from scratch immediately and hoping for the best later. However, you should probably read some peer-reviewed journal papers and look for proven recommendation system methodologies that could be applied to your problem domain.

A recommendation system that is based on the prior successes of others should be less likely to cause time-consuming problems in the future. Also, an approach based on the prior successes of others will be more defensible to supervisors if problems do occur in the future.

**Conduct an experiment to test the hypothesis**

When conducting experiments, test only one hypothesis at a time or use accepted experimental design practices for testing multiple experimental treatments. Otherwise you will confound and invalidate experimental results.

When conducting experiments, take notes and make sure your work is repeatable. Don’t let the R, Python or Bash session history on someone’s personal laptop be the only recording of an experiment. Instead, try to take digital or written notes and comment your code. Better yet, code the experiment into a dedicated program that can be rerun and understood by others and store that program, along with some sample data, in a shared, version-controlled repository.

When conducting experiments, also try to use similar test environments for all aspects of the experiment. If this is impossible due to real-world time and resource constraints, at least try to be aware of outside factors that could influence experimental results.

In the context of the recommendation system example, it would be a bad idea to immediately deploy a combination content-based and collaborative filtering recommender. It would be better to separately test a content based-recommender, a collaborative filtering recommender and a combination recommender, all against an established benchmark.

The recommenders should also be tested in similar environments. For instance, it would be misleading to test one recommender at a time when site traffic is high and another recommender at a time when site traffic is low. It would also be a good idea to make sure that more than one data scientist can repeat the results of each experiment and understand the code used to implement the each system.

**Objectively analyze the results of the experiment**

The results of an experiment (as measured by a pre-established assessment method) validate or invalidate a hypothesis. Sometimes an assessment is easy to understand and accept. Sometimes a scientific assessment can be complicated or obscured by technical problems, personal emotions or organizational culture.

If there is any technical uncertainty about the meaning of experimental results, reformulate a simpler experiment and try again. If you invest a lot of time and energy in a project, you naturally want it to succeed. Data scientists have to be objective, even in the face of discouraging results. You must avoid the many tempting and irresponsible cheats that make negative results look like positive results, including:

* Over-fitting or over-training a learning algorithm on a small set of examples.
* Using old, simple, small or otherwise unrealistic data as the subject of an experiment.
* Failing to record or acknowledge human input, i.e., parameter tuning or feature engineering, into an experiment.
* Choosing the most favorable assessment measure for an experiment after an experiment has been completed.
* Changing the guiding hypothesis of an experiment after an experiment has been completed to obtain positive results.

Data science experiments can also expose problems in organizations. As a data scientist, be wary of organizational cultures that alter or suppress problematic findings from data science experiments.

To complete the recommendation system example, let’s say that after conducting a set of experiments, the data science team finds that a standard, widely used content-based recommender is generating the most revenue by driving site visitors to advertisements, while a novel, sophisticated collaborative filtering recommender that the data science team spent months implementing is increasing the use of your website’s service platform, but not increasing revenue. Of course the team would be tempted to reformulate the hypothesis and measurement assessment so that their own project looks more successful. However, the better option is probably to cut their losses on the collaborative filtering recommender and move on to new problems, tasks and experiments, while the simpler recommender continues to generate revenue for the organization.

Finally, I’ll conclude with a request.

If your job title is data scientist or you call yourself a data scientist, try to use the scientific method in your work. We'll all be better off in 20 years if data science is a vibrant and respected branch of the mathematical sciences rather than a stale marketing term.
