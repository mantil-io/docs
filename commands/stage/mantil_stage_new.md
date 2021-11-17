# mantil stage new

Create a new stage

This command will create a new stage with the given name. If the name is left empty it will default to "dev".

If only one node is set up in the workspace, the stage will be deployed to that node by default.
Otherwise, you will be asked to pick a node. The node can also be specified via the --node option.

### USAGE
<pre>
  mantil stage new <name> [options]
</pre>
### OPTIONS
<pre>
  -n, --node string   Node in which the stage will be created
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
