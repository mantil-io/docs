---
title: "mantil logs"
linkTitle: "logs"
weight: 11
description: Fetch logs for a specific function/api
hide_summary: false
---

Fetch logs for a specific function/api

Logs can be filtered using Cloudwatch filter patterns. For more information see:
https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html

If the --tail option is set the process will keep running and polling for new logs every second.

### USAGE
<pre>
  mantil logs <function> [options]
</pre>
### OPTIONS
<pre>
  -p, --filter-pattern string   Filter pattern to use
  -s, --since duration          From what time to begin displaying logs, default is 3 hours ago (default 3h0m0s)
      --stage string            Name of the stage to fetch logs for
  -t, --tail                    Continuously poll for new logs
</pre>
### GLOBAL OPTIONS
<pre>
      --help       Show command help
      --no-color   Don't use colors in output
</pre>
### LEARN MORE
<pre>
  Visit https://team.mantil.com/docs/ to learn more.
  For further support contact us at hello@mantil.com.
</pre>
