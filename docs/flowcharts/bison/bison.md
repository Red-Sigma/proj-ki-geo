#
# Check during the tick if bison thirsty
```mermaid
flowchart TD
  A[Start]--> I{thirsty?}
  I -->|no| J[DoRandomWalk]
  I -->|yes| D{Move Toward Water}
  D -->|Water Nearby, Distance < 100m| E[Drink Water]
  D -->|No Water Detected| Q[Wandering for Water Search]

```
#
# Check during the tick if bison is hungry 
```mermaid
flowchart TD
  A[Start]--> I{hunger?}
  I -->|no| J[DoRandomWalk]
  I -->|yes| D{Move Toward Food}
  D -->|Food Nearby, Distance < 100m| E[Eat Grass]
  D -->|No Food Detected| Q[Wandering for Food Search]

```
#
# Check during the tick if it is mating season
```mermaid
flowchart TD
  A[Start]--> I{isMatingSeason?}
  I -->|no| J[DoRandomWalk]
  I -->|yes| D{Search partner for mating}
  D -->|check for partners nearby, Distance < 50m| E[Mate]
  D -->|No available partners| Q[Change Location and continue searching]
  Q -->|walk| D[Change Location and continue searching]

```
#
# Check during the tick if bison is tired and should get some rest
```mermaid
flowchart TD
  A[Start]--> I{Nighttime?}
  I -->|no| J[Continue Daily Activities]
  I -->|yes| D{Rest/Sleep}
  D -->|Sleep for 7-9 hours| E[Resting/Sleeping]
  D -->|Not Ready to Sleep| J

```
# 
# Chart for social interaction 
```mermaid
flowchart TD
    A[Social Interaction] -->|Initiate Interaction| B[Greetings and Sniffing]
    B -->|Friendly Interaction| C[Continue Grazing Together]
    B -->|Unfriendly Interaction| D[Separate and Wandering]

    D -->|Rejoin Herd After a While| E[Rejoin Herd]
    D -->|Solitary Movement| F[Wander Alone]

    C -->|Continue Grazing Together| G[More Socializing]

    G -->|Playful Interaction| H[Chasing and Play]
    G -->|Restful Interaction| I[Resting Together]
    
```