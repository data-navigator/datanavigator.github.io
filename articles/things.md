# Dreaming about Data, Thinking about Things

When considering the 'Internet of Things', 'Things' themselves are is still an ill-defined concept in many respects, despite standardization efforts. Most commercial development thus far has been towards relatively small, household objects: Coffee pots, phones, thermostats, even cars. Protocols have largely been designed to support this vision, thus far. Sometimes these Things just provide sensed data - like the pedometer on a smart phone, or a security camera's video feed. Sometimes they are interactive - you can turn the AC on during the commute home. Maybe even automated - your fridge orders ingredients from an online delivery service when it senses the latest batch is almost used up. All certainly useful features which make life easier or safer. However thinking about 'Things' to this extent does not fully realize the potential of the concept. The scale of application appears to be much larger; an aggregation of modern technologies which coalesces into an epoch-shifting economic, financial, government, military and societal overhaul which can greatly redefine humanity's potential.

## Things

If we think of the entire world around us as a single entity, made up of a hierarchical graph of individual components whose aggregative effect compose the entities above them, then 'Things' can be of vastly varying shapes, sizes and properties. For the purpose of this document we're discussing a one-way hierarchy with the Earth as the topmost entity. Theoretically the concept extends upwards to planetary systems, solar systems and beyond in addition to refining down to the subcomponents of each entity, again in theory all the way to the subatomic. With that in mind, the system described below is extensible in either direction but presently focuses on the size range between a single sensory device, and the planet Earth.

The Earth itself is a thing - its properties the total aggregation of those properties of it's subcomponents. For a simplified example, a 'schema' applied to a query on an 'EarthThing' object could define its surface as the sum of the surface of both Oceans ('PacificOceanThing', 'AtlanticOceanThing', IndianOceanThing etc - each with their own nebulae of properties and components) and Land. Another 'schema' could define its human population as the sum of all nation's population('USAThing', 'ChinaThing' etc), and their average life expectancy as the mean of all known ages at time of death. These queries can also be filtered or aggregated by a time dimension - worth noting that things may have an inherent time domain. Non-temporal properties of a thing can be used in queries outside its time domain ie: Percent of 'OrlandoThing' city limits in 2016 that were swamp in 1850.

## Metadata

In these examples, it is really an Internet of Data-about-Things that is being discussed. The things sense a datum about their environments, and report it to the network. A tamper-proof network which provides the inherent ability to record discrete units of sensory data emitted by a 'Thing', which is searchable/filterable by schemas as suggested above, would allow for proof of ownership for each piece of data created within the Internet of Things. If this data is consumed by subsequent queries then transactional metadata is generated about the consumption, which then chains to subsequent consumptions. In this way, the owner of the data can be awarded income - derived from the rarity of the data and/or its precision in comparison to other measurements of the same discrete phenomenon.

This aspect may be thought of as a 'competitive data market' ie: multiple sensors of similar quality (and potentially multiple owners) attuned to a single phenomenon - this just means the value of the data is split between the offerings which fit within the constraints (ie: filter by precision, filter by owner etc) on a query. For example several people living in a house can all own thermometers and provide data about the temperature in the back yard - if someone a few houses down queries the temperature outside and is returned with an average value which includes readings from those thermometers, each person is rewarded.

However, if one of those thermometers provided the temperature only in Fahrenheit and the query was in Celsius then only the two owners who provided suitable data would be rewarded, and it would be a slightly larger proportion of the overall reward. The conversion between the two isn't particularly difficult, but requires two additional things above a direct retrieval of data: a function, and computing time.

## Functionality

Functions themselves are data. In the thermometer example, a function to convert between Fahrenheit and Celsius can be stored as functional metadata. A switch within the thermometer can then return either the temperature value, or temperature value wrapped in a conversion function. Since the thermometer is only returning a value, or function and value and not recording it in this example, it can only provide it's real-time value to a query that happens to be asking for it at that exact moment in time. Since this is unlikely, it is a suboptimal method of deriving value from a Thing. Additionally, since the cost of computation is on the consumer, it lowers the market value of that datum. The derived data and income earned for it's further consumption is then owned by the former consumer, with a fraction going to the former owner as well - this effect chains, until eventually the datum is multiple derivations away from the origin at which point the original owner no longer receives income from its use.

A superior approach for the owner of the thing then, is to consistently record the data from their Things, allowing it to be consumed immediately, or later on. In the present example, the temperature value can be committed at regular intervals to a version-controlled repository. The thermometer then acts as a pointer to the repository, so when queried the latest static value is returned, or value(s) within a specified temporal extent. Functions can then be applied either at the time of commitment, to immediately generate a spectrum of derived values from the original datum, or only upon query. Perhaps the most efficient approach here is a lazy evaluation, the function being computed by the datum's owner at the time of a query, as opposed to allowing the consumer to execute the function and assume ownership of the derived datum. However if the function is not offered by the provider then a consumer is fully able to consume the raw datum, compute the derivation with their function and offer the derived datum as a product.

Queries themselves are function, which can also embed the functionality required to execute them. This functionality is limited to a read-only permission level on the queried data, however the derived output then becomes accessible and ownership changes. Subsequent uses then reward the owner of the function, and in diminishing amounts the previous owners in the chain of transformations upon the datum. This should encourage innovation in the realm of functionality and ensure that each producer is rewarded from the genesis of that datum.

## Location

Embedding functionality for computation at the source is important, as derived data should initially remain stored (in a spatial sense) closer to the source as opposed to being stored near the consumer, as we can assume it is more likely that subsequent queries involving that Thing originate from nearby. Storing at the consumer introduces latency between a Thing and it's metadata and would make queries become slower over time; the data becoming sparser as the amount of consumers and complexity of queries increased.

If a Thing's data is being consumed frequently by multiple consumers who are far away from the Thing itself but nearby to one another, then a computationally intensive 'clone' function can be applied to the entire dataset - this function is performed at the consumer, the copy then residing at their spatial location so that nearby consumers begin to utilize the clone as opposed to the original source. To decrease the computational resource requirements of a clone (copying and verifying the entire dataset), the operation could be subdivided and distributed to a cluster of nearby consumers or non-consumers offering available storage for cloned data as opposed to just an individual consumer, if usage patterns and/or dataset size deemed it necessary.

Clone operations are expensive for the consumer and introduce the largest per-operation amount of network traffic, but are both potentially profitable and beneficial to the overall state of the network if well used. The operation can therefore be devalued or inflated based off traffic patterns to encourage efficient cloning.

## Relationships

Relationships themselves are datum which define ways in which Things interact with one another. Location is an example of a relationship, possibly the most important between two physical objects, or an object and its metadata. SomeThing's location is defined by its position on it's parent Thing, or in relation to it's sibling Thing(s). Another relationship to consider in this system is the frequency with which a consumer consumes from a producer. This is with a given confidence which is derived from the consistency of that frequency pattern over time.

Both of these relationships, in addition to others, are analyzed when determining the value of clone operation. So not only are the Things themselves valuable and consumable, but also information taken from aggregating the data from these relationships.