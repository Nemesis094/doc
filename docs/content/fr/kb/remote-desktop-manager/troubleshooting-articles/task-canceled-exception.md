---
eleventyComputed:
  title: TaskCanceledException - a task was canceled
---
One or more errors occurred in {{ en.RDM }} with a {{ en.DVLS }} data source.

AggregateException: TaskCanceledException - A task was canceled
![!!KB4752](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4752.png)
## Solution
1. Go to ***File - Data sources - Edit Data Source - Advanced*** and change the ***Connection timeout*** to 30 seconds.
1. Click ***OK***.
![!!KB4751](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4751.png)
