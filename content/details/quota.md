+++
next = "/next/path"
prev = "/prev/path"
weight = 20
title = "Quota"
date = "2017-03-04T20:38:40-05:00"
toc = true

+++
<script type="text/javascript"
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>


**Quota** is the term used for the smallest number of votes that will guarantee the
election of a candidate.

In a first-past-the-post election, where there is one and only one winner, quota is
the well-known 50% + 1.  Expressed mathematically, it's \(1/2*v + 1\) where *v* is the
total number of votes.  A candidate with that many
votes can't be beaten by anyone else; there simply aren't enough votes left.

In a region where we elect two winners, quota is \(1/3*v + 1\).  If candidates A and
B both have just over 1/3 of the votes, no other candidate can obtain more than 1/3
to beat them.

Similarly, in an election with three winners, quota is \(1/4*v + 1\) and for four winners
quota is \(1/5*v + 1\).

The general formula is $$\frac{1}{n+1} v + 1$$
where *n* is the number of people to be elected and *v* is the number of votes.

There are actually several different ways to calculate quota.  This approach is known
as [Droop](https://en.wikipedia.org/wiki/Droop_quota) quota.