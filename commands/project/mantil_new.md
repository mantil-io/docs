---
title: "mantil new"
linkTitle: "new"
weight: 3
description: Initializes a new Mantil project
hide_summary: false
---

Initializes a new Mantil project

This command will initialize a new Mantil project from the source provided with the --from option.
The source can either be an existing git repository or one of the predefined templates:
excuses - https://github.com/mantil-io/template-excuses
ping - https://github.com/mantil-io/go-mantil-template

If no source is provided it will default to the template "ping".

By default, the go module name of the initialized project will be the project name.
This can be changed by setting the --module-name option.

### USAGE
<pre>
  mantil new <project> [options]
</pre>
### OPTIONS
<pre>
      --from string          Name of the template or URL of the repository that will be used as one
      --module-name string   Replace module name and import paths
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
