### Recommender Systems
========================
Some recos systems ask you to personalize your interest profile
Should not be required, should guess based on viewing behavior
A lot can be inferred from where a user comes from, what device (outdated, not tech savvy)
Use what browser they use to get to your service

All this needs to happen in ~50ms, so no disk lookups allowed. everything has to be preprocessed and cached and ready to go

#### Formal definition
-----------------------
User requests content
Objects (displayed as results)
context (device, location, time)
Interface (mobile browser, tablet, viewport) (UI is important)
	- interface also decides how the consumption order changes for the user, how the recos are presented

#### Challenges
----------------
Scalability (millions of objects in catalog and millions of users)
Cold start (new user, no prior knowledge)
Imbalanced dataset (user activity and reivews follow power laws)
Power law: p(x) = (x+a)^-b (referred to as the long tail)

Caching of frequently requested movies is favorable
Latency hiding can also be done for these cases (pre-request something)

Important factor to consider: yardstick for measuring reco perf
Netflix uses Least mean squares prediction error
The inherent problem here is that die hard fan will only be shown more die hard movies but not a diverse collection of similar movies


##### Nearest Neighbor based Collaborative Filtering (CF)
----------------------------------------------------------
User-user similarity, movie-movie similarity
if you watched x, so reco movie y that's similar to x
Oldest known cf method
similarity scores between movies 1-3 and 1-6 = 0.2 and 0.3 respectively
take weighted average of scores and ratings ==> (0.2*2 + 0.3*3) / (0.2+0.3) = 2.6
This method is not accurate and doesn't scale very well
Problems of Bias:
	- unusually high ratings for movies
	- unusually low ratings from users
	- ratings change over time
	- bias correction is important
	- need to offset user and movie biases

