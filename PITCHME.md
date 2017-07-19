# AWS X-Ray

<br>
<span style="color:gray">Intro to Lambda function tracing</span>
<br>
<span style="color:gray">(Node.js)</span>

---

## Which part of your (micro)service is...
  - slow?
  - generating error responses?
  - using a particular AWS service?

---

!(assets/sample-servicemap.png)


---


```javascript
from time import localtime

activities = {8: 'Sleeping', 9: 'Commuting', 17: 'Working',
              18: 'Commuting', 20: 'Eating', 22: 'Resting' }

time_now = localtime()
hour = time_now.tm_hour

for activity_time in sorted(activities.keys()):
    if hour < activity_time:
        print activities[activity_time]
        break
else:
    print 'Unknown, AFK or sleeping!'
```
@[1](Python from..import statement)
@[3-4](Python dictionary initialization block)
@[6-7](Python working with time)
@[9-14](Python for..else statement)
