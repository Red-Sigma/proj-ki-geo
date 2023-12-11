```mermaid
flowchart TD
  A[Start]--> I{thirsty?}
  I -->|no| J[DoRandomWalk]
  I -->|yes| D{Move Toward Water}
  D -->|Water Nearby, Distance < 100m| E[Drink Water]
  D -->|No Water Detected| Q[Wandering for Water Search]

```
# 
```mermaid
flowchart TD
  A[Start]--> I{hunger?}
  I -->|no| J[DoRandomWalk]
  I -->|yes| D{Move Toward Food}
  D -->|Food Nearby, Distance < 100m| E[Eat Grass]
  D -->|No Food Detected| Q[Wandering for Food Search]

```
#
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
```mermaid
flowchart TD
  A[Start]--> I{Nighttime?}
  I -->|no| J[Continue Daily Activities]
  I -->|yes| D{Rest/Sleep}
  D -->|Sleep for 7-9 hours| E[Resting/Sleeping]
  D -->|Not Ready to Sleep| J

```
#