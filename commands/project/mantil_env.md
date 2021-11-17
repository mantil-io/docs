# mantil env

Export project environment variables
for use in other shell commands.

Mantil project is determined by the current shell folder. It can be anywhere in
the project tree.
If not specified (--stage option) default project stage is used.

### USAGE
<pre>
  mantil env [options]
</pre>
### OPTIONS
<pre>
  -s, --stage string   Target project stage
  -u, --url            Show only project api url
</pre>
### EXAMPLES
<pre>
  ==> Set environment variables in terminal
  $ eval $(mantil env)

  ==> Use current stage api url in other shell commands
  $ curl -X POST $(mantil env -url)/ping
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
