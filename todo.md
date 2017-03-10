
1. Make "Counting Votes: Level 3" initially hidden
1. Add Lev's example to fairness FAQ  (see below)
1. Move to a different domain

## Vote trace (from Lev)
Not surprised, heck of a job Byron. A few small tweaks when you have
a chance:

1) in a dropbox or some such, explain the assumptions you used for
distributing votes beyond first choice parties (ie once a voter's preference for all regional candidates of their first choice party
was exhausted)

1b) Also, for the sake of Green support, please state that this model
is based on 20?? election results and does not take into account expected
changes in distribution when votes are freed from strategic pressures.
I'm guessing/hoping that Greens will get more seats under LPR than any modelling based on past elections would show.

2) At top, explain that "P" means protected win for last candidate in riding.

3) For each riding, show the quota

4) At top, explain/define "party vote and Eff vote". Does former include all votes transferred following primary party preference?

5) on the how votes transferred page, had a head line:
votes     party    Canadidate          riding code

For the sake of making the riding code clear, easy to figure out
but always nice to have a webpage that minimizes deciphering,





## Lev's Fairness Example
1.	Can you give another example where neighbouring ridings have different voting patterns?


	This example is by Lev Tarasov.

	Suppose there are three urban ridings and one rural riding, each with 100 votes. Further,
	suppose that everyone votes for their own party across all ridings.  The following table gives
	the assumed first choice votes.


	<table class="numbers">
		<thead>
		<tr><th>Party</th><th>Urban A</th><th>Urban B</th><th>Urban C</th>
			<th>Rural D</th><th>Total</th></tr>
	</thead>
		<tr><td>Con</td><td>25</td><td>25</td><td>25</td><td>40</td><td>115</td></tr>
		<tr><td>Lib</td><td>39</td><td>39</td><td>39</td><td>30</td><td>147</td></tr>
		<tr><td>NDP</td><td>21</td><td>21</td><td>21</td><td>20</td><td>83</td></tr>
		<tr><td>Green</td><td>15</td><td>15</td><td>15</td><td>10</td><td>55</td></tr>
	</table>

	Quota is 1/5*400 + 1 = 81, the number of votes that guarantees a candidate's election.

	Looking at the totals column, the Liberals, Conservatives, and NDP all have in excess
	of 81 votes and should get one seat each based on first choice votes.  Who gets the
	last seat will depend on 2nd and perhaps 3rd choice votes.

	The Liberals have enough votes in urban areas alone to secure a seat.  The Conservatives
	and the NDP both need votes from across the region to secure a seat because the
	rural votes alone are less than 81 and the urban votes alone are less than 81 for both
	parties.

	Because we're assuming that everyone will vote for their own party across the ridings,
	all of the Green votes will eventually transfer to one of the urban ridings.  That's 
	because the candidate in the rural riding has the fewest votes and get's dropped first.

	One possible series of candidate transfers would go like this, where "Green[D]" means 
	"the Green candidate in Riding D".

	Green[D] --> Green[C]; Green[A] --> Green[C]; Green[B] --> Green[C].  (Green[C] now 
	has all 55 of the Green votes.)

	NDP[D] --> NDP[B]; NDP[C] --> NDP[B]; NDP[A] --> NDP[B].  NDP[B] now has 83 votes
	which is more than quota and is declared the winner in Riding B.  That means that 
	both Lib[B] and Con[B] are dropped and their votes are transferred.

	### To be completed...
	So,
Suppose 3 urban ridings of 100 votes, and 1 rural of 100 votes, and
that everyone preferentially votes for their own party across all
ridings: with 39/25/21/15 Lib/Con/NDP/Green Urban %, and 30/40/20/10
rural

      Lib   Con   NDP  Gr
urban: 117   75    63   45
rural: 30    40    20   10
#quota is 400/5 + 1 = 81
#Lib, Con, and NDP each get 1 first choice seat
# Note that NDP and Con seats depend on rural vote

#surplus allocation,
urban  36    0     0  45
rural  30    34    2  10
total  66    34    2  55
# NDP is dumped, say their votes go to Greens
total 66     34    0  57
# Conservatives dumped. Final seat will depend
# on whom Conservative voters indicate as the next choice
# If conservatives only vote for their own party, Libs get
# in. If 10 more conservative voters vote for Greens than
# for Liberals, Greens get in.


# NOTE, without assumptions about whom urban voters would
# pick as their second choice (urban or rural), it is not
# possible to determine which party gets the rural seat.

What sticks out for me is that all four parties will have to court the
rural vote. Three parties need it to get a seat.  One party needs it
to get a second seat (for the above scenario).

Perhaps more useful, if someone has the time, is to create an online
calculator so that anyone can submit their own scenario...



