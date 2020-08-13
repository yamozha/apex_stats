# apex_stats
an api-wrapper for https://apex.tracker.gg/

### recentlyPlayed(username/id, userplatform (optional) )
Shows you your recently played legends.

userplatform is, by default, origin, but you can choose from 'origin', 'xbl', 'psn'.  
username/id is - the desired username to be checked.

```
apexStats = apex.recentlyPlayed(your-tracker.gg-api-key)
apexPrint = apexStats.recentlyPlayed(username/id)
print(apexPrint)
>>> ['your', 'last', 'played', 'characters']
```
