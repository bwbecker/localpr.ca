+++
date = "2017-03-04T20:24:27-05:00"
toc = true
next = "/details/quota"
prev = "/details/ballots"
weight = 15
title = "Counting Votes"

+++

Counting votes is an important part, perhaps the most important part,
of any electoral system.  Here, we explain it for Local Proportional
Representation in increasing levels of detail.

The overall goal of the count is to identify the best set of candidates
for the region with the constraint that exactly one of them is in each
riding.

### Counting Votes: Level 1

Counting proceeds in steps.  At each step a candidate is either proclaimed
a winner or a candidate is eliminated.  We're careful to not eliminate the last candidate in
a riding and to avoid proclaiming more than one winner in a riding.  
This continues until we have one winner in each riding.

### Counting Votes: Level 2

To flesh out the procedure, it's useful to identify three groups of candidates:

* *Elected*: candidates that have reached [quota](/details/quota/) and are declared winners
* *Hopeful*: candidates that could still be elected
* *Not Elected*: candidates that have been eliminated from the race

All of the candidates start out as *Hopeful*.

We'll start by tracing what happens to one particular ballot during the counting 
process in an imaginary election.

![Ballot](/static/ballot-general.png)

Imagine one pile for each candidate's ballots.  Our ballot 
goes on Gord Miller's pile because Miller was ranked number 1.  

Suppose that Miller is the candidate with the fewest ballots on his pile.  
That signals that he is the next person to be eliminated (*Not Elected*).  This ballot will
then be placed on the pile of the next highest ranked *Hopeful* candidate, David Doel.

At some point Doel becomes the candidate with the smallest pile of ballots and is
eliminated (*Not Elected*).  This ballot then goes to Andrew Seagram's pile.  Likewise, 
Seagram is eventually eliminated and the ballot goes to Lloyd Longfield.

Imagine that Longfield is popular and there are now 50,000 ballots on his pile but
he only needs 40,000 votes to win.  That number, 40,000, is called the 
[quota](/details/quota/). Quota is the equivalent of 50% + 1 in a FPTP election, the
minimum number of votes to guarantee victory (although it could be less with vote
splitting). 
Longfield is now declared *Elected*.<sup>1</sup>  

Unfortunately for the remaining *Hopeful*
candidates in Longfield's riding, they can't be elected without breaking the one MP in
each riding rule.  They are therefore declared *Not Elected*.

Those surplus votes are transferred fairly to the remaining hopeful candidates.  In this case,
the ballot is transferred to Michael Chong.  But 4/5 of this ballot (40,000/50,000)
was needed to elect Longfield, so Chong only gets the remaining 1/5.

Suppose that Chong has the fewest votes of any *Hopeful* candidate and is also the
last *Hopeful* candidate in his riding.  As the last *Hopeful* in his riding, he'll be protected
from being eliminated.

This proceeds until one MP has been elected for each riding.

  <div class="footnotes">
    <p><sup>1</sup> In the unlikely event that two candidates go over quota in the same riding,
the one with more votes becomes elected.</p>
  </div>


### Counting Votes: Level 3

{{% clickToReveal %}}

To be yet more rigorous in describing the procedure, we can express it as pseudocode for
a computer algorithm:

```python
while (some seats remain unfilled) {
  if (a hopeful candidate, C, reaches quota) {
    C.state = Elected
    for all hopeful candidates, H, in Cs riding 
        H.state = NotElected
    transfer any surplus votes to remaining hopeful candidates
  } else {
    let C be the unprotected candidate having the fewest votes
    if (C is the last candidate in their riding) 
      C.protected = true
    else {
      C.state = NotElected
      transfer Cs votes at full value to remaining hopeful candidates
    }
  }
}
```


{{% /clickToReveal %}}


<script>
  // Only works for one per page :()
  $(document).ready(function() {
    $(".more").on("click", function() {
      console.log("Click!");

      $(".fadeDiv").hide();
      $(".fadedContent").css("overflow", "auto").css("height", "100%");
      $(".more").hide();
    });
  });
</script>



