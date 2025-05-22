# Predicting Avalanche Incidents in Colorado
Every year, approximately 27 people die from an avalanche in the United States, with hundreds more being non-fatally buried and likely many going unreported. In regions that pose high risks of avalanches, this threat is more prevalent than any other natural event. If we could analyze the conditions that lead up to an avalanche occurrence, we can attempt to predict regions where an avalanche is imminent and issue warnings before another incident takes place.

  To attempt this feat, we are going to take a look at Colorado, a state that occupies a third of the avalanche incidents in the United States. Colorado models an environment that simultaneously is avalanche-prone and contains a wide range of varying weather conditions. They have high-elevation areas, an acceptable amount of precipitation, and an erratic amount of wind. The Colorado Avalanche Information Center also offers freely available data on each reported avalanche sighting for the past ~70 years, with details on their locations, avalanche type, date, and more. We can use this data alongside external weather data to try to predict and visualize why these avalanches are occurring. 

  There are several types of avalanches that each have certain conditions that exemplifies their potential as a threat. I was interested in understanding which avalanche types are most relevant and whether they change throughout the season: 

![Avalanche Proportion](aval_prop.png)

  Through this graph, we can see that Colorado experiences a steady level of mostly Soft Slab (SS) avalanches and a lower amount of Hard Slab (HS) avalanches through the winter. However, starting around in April, the proportion of Wet Loose (WL) avalanches started to spike as Spring arrived. Moving forward, I will only consider these three avalanche types during analysis, given that they compose an overwhelming proportion of the avalanche incidents in the data. But knowing the difference between these avalanche types is crucial in getting the full picture of why this may have happened.

  <ins>Slab Avalanches:</ins>

  Slab avalanches occur when a large “slab” of compacted snow is separated from the ground or other snow. While this is often triggered by added weight by a person, it is also notably primed by wind compacting the snow together, and can be triggered by various external factors as well. Soft and hard slab avalanches are differentiated by the quality of the compacted snow that the avalanche was composed of. Soft slab avalanches are typically low density and vice versa.

  <ins>Wet Loose Avalanches:</ins>

  Wet Loose avalanches occur as a result of some form of external factor weakening the snow’s surface and resulting in a large amount of snow falling down a slope. It is important to note that this often requires steep elevation since a larger slope makes it easier for the snow to lose cohesion and start tumbling. Also, these avalanches are typically as a result of warmer temperatures, which explains why they started to make a meaningful appearance starting around springtime.

  Upon understanding the avalanche types of interest, we can see that there are particular variables that have potential to act as a trigger to these avalanche incidents. Slab avalanches, while often started by human weight, are supported by wind-compacted snow and can also be started by factors like precipitation adding pressure onto the slabs where humans may not, or elevation accentuating the previous two factors. Wet Loose avalanches on the other hand can find issues in any factor that may cause snow to lose cohesion, like radiation and higher temperatures. Moving forward, I will look to analyze the effects of precipitation, surface solar radiation downwards (SSRD), temperature, wind magnitudes, and elevation affect the occurrence of an avalanche. 

<ins>Weather Data Organization</ins>
  
  I have obtained data on the first four variables from the European Centre for Medium-Range Weather Forecasts (ECMWF). For example, below is a map of precipitation measured across February 1st, 2025 in Washington.
 