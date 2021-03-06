# Distributed loaded dice algorithm

Voting systems are most of the cases never ideal - that's proven by maths - and times may come when a particular voting system gets abused by some rouge politicians or parties. In such times people can optimize their voting power to deviate from rather randomly scattered voting to pre-election based and with various goals. Most of the time however that rouge government will try to hinder this process so it might not seem a bad idea to do it privately safely just by being able to run an offline application on a mobile phone which helps the masses organise themselves according to some rule of thumb rather than just failing to change the system! Let's see a proof of concept for an app to help unite voters in a single round voting system with a fragmented opposition by an offline computable pseudo-random function.

In a single round voting system, where the strongest party's candidate wins irrespective of whether s/he has >50% majority, a fragmented opposition automatically yields that votes cast on them get more or less statistically distributed among the oppositions' candidates, thus enabling a party with relative majority retain its power even if its popularity is <50% among the voters' entire population.

One way of tackling this problem is if the opposition holds pre-elections to agree upon a single candidate for each district, so that people's votes can't scatter. A simpler and faster one is throwing a dice to select a candidate in districts without sufficient funds to hold pre-elections for. A more fair one is doing one big public poll - like an EU referendum - to see the public support for each oppositional party and throwing with an adequatly loaded dice to choose the single oppositional candidates for each and every voting district.

However this would need politicians who know how to gamble, and that has already been proven not to be the best idea. So we people of any Democratic Republic of a Single Rounded Voting System with Fragmented Opposition, need to take the situation in our hands, and do it personally... ;)

How can a decentralizied pseudo random algorithm help with that?

First lets stay with the non-loaded, regular dice concept. If all voters would vote for the oppositional candidate in every district with a name first in alphabetical order among all candidate names, that would be a deterministic yet equally random selection among the competing parties. However it would make up a funny parliament if most representatives' names would start with 'A' or 'B' rarely 'C' sometimes 'D' etc.. So it is better to compute a pseudo random function, a so called hash of the candidates' names with a smart phone app offline, and then let the largest hash be selected from that list. This has further benefits too, because it opens the door to the distributed version of the loaded dice concept, that is capable of representing the diverse parties actual public support! All that the application needs to do is simply ask for the weight of the load, i.e. how much chance one oppositional party's candidate needs to have based on the previously polled nation wide popularity, and then create proportionally many hashes for each candidate of the respective parties in every voting district by adding a counter value to the names. Meaning for example if a party won 4 seats in the EU parliament, that party's candidates should be assigned 4x as many hashes as candidates of a party with 1 EU seat. This is easy to accomplish, just a chance counter needs to be added to the hash input, that runs from 1...4 in case of the candidates of the stronger party in this example.

In other words the applications compute the results of card games where the strongest card wins. The cards' setup is as follows: each local candidate of a particular party gets proportionally many cards as their respective party's nation wide popularity, but the cards themselves are generated by calculations involving the names list of the particular voting district as changing random input. This results in the same suggestion in any given district, but changes from district to district - because of the semi-random nature of the applied hash function - so that each party's candidates have chances relating to the number of how many cards they have. Thus the final setup of the parliament is better going to represent each party according to their popularity because of probability.

The joker number, named after one of the Hungarian lottery games, is a real life random number, generated publicly not so much before election day, any lottery number does the trick. It is needed for several reasons:
1) by not being able to forecast the people finally suggested by the algorithm, the governments don't have enough time to provoke or politically attack them dedicatedly
2) due to statistical dispersion and the finite number of districts, some parties are going to be slightly over represented, others under compared to their measured popularity, and how this eventually turns out depends mostly on the lottery number entered
3) the distortion based fluctuations from 2) are going to be different at every election, as long as the current law is in power, and this algorithm is being applied by voters
4) if the same software is used for several elections throughout years, but at some small districts the names list wouldn't change, still everyone will always have a new a chance to win

Of course the entire offline distributed process is very sensitive to
 - application of the exact same algorithm by every voter
 - people entering proper data into their phones: locally candidate names, nationwide the same popularity results
 - selecting the common random number source that can't be silenced, censored at the very last moment yet is still widely accessable
 
As stated the process works offline, doesn't require any collection of voters' data and doesn't require more centralized coordination than named in the last list.

In case of the existence of multiple diversely working applications, that split oppositional voters' influence without coordination on which to use, the _fallback plan_ is to vote to the _first_ relevant oppositional candidate in the voting district in _alphabetical order_...


## The hungarian election system

There are 199 seats altogether in the single house parliament. 93 of these are distributed proportionally to the nationwide popular vote, which can't be anymore fair.

Yet 106 come from 106 geographical municipalities in each of which, the popular vote is "rounded" up to 1 single person per district(!). This rounding isn't mathematical, it doesn't mean if nobody reached 50%, then the municupality sent no representatives at all. Instead it works so, that the owner of the largest number of votes always wins, irrespective of whether s/he only possesses the largest minority, if all the others are so fragmented, that each and every one of them won even less. This is where second round voting should come in. In a second round, where only the 2 strongest first round candidates competed, any strongest minority's candidate stood a chance to loose. Yet this second round does not exist, and thus Orban has always won nearly all the 106 "rounded" districts, eversince he changed the election law in 2011, at the very first opportunity after he gained his 1st supermajority in the previous, 2 rounded election system in 2010, that was considered more democratic.

## The role of 71 municipalities...

...that any party has to fill obligatorily in order to be granted a position on the nationwide list.

If each party is to have its own list, let there be two for simplicity's sake: a left-wing and a right-wing opposition coalition (just so the coalition is not so "slimy" - the term applied in the campaign against the united single bulk opposition.). So, if two different parties with independent lists want to run in 71 districts by default, with a total of 106 districts available, they can only take the largest district, close to two-thirds, if they run their independent candidates against Fidesz in 35-35 districts, while in 36 - "overlapping" - districts they also run against each other, thus sharply dividing the opposition voter camp in this latter group of districts. And in those districts where the opposition camp is almost evenly split, Fidesz is largely in the lead*.

So let's calculate what this would mean if the opposition had just twice as many voters as the Fidesz camp, i.e. it would have to win exactly 2/3 of the parliamentary majority: 2/3 of the 93 national list seats are 62; and of the 106 districts, the opposition can take 70*, for a total of 132.

Whereas a 2/3 majority starts from 133(!).

(*) That only holds if in districts where at least 3 candidates are competing: 1 Fidesz, 1 left opposition and 1 right opposition; and if the opposition voter camp is split about 50%, so that the candidates would get about 1/3 - 1/3 - 1/3 of the vote, plus a few more percent taken away from the opposition by a couple of fake and joke parties, while Fidesz voters would cast 1/3 of their votes in a disciplined manner. Alternatively, it can be assumed that the opposition will split up the strongest opposition districts to run 1 to 1 against Fidesz in them, and Fidesz will naturally be stronger in the remaining double opposition districts.

Another notable problem is if the opposition parties want districting that takes into account their real social support. For in order to bargain some districts to each other without reducing the number of candidates per party below the required number (71 in the '22 election), they would have to run against each other in more districts. In other words, the need for a more precise representation of public support is also a mill for Fidesz.

In the case of three or more opposition parties, Fidesz, with its 1/3 of the voter base, would almost unconditionally win the 4 or more districts, of which more and more are needed as the number of parties or groups increases.
