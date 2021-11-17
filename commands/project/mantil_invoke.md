# mantil invoke

Invoke api method for current project and stage

Makes HTTP request to the gateway endpoint of the project stage. That invokes
lambda function of that project api. If api method is not specified default
(named Default in Go code) is assumed.

Mantil project is determined by the current shell folder. It can be anywhere in
the project tree.
If not specified (--stage option) default project stage is used.

During lambda function execution their logs are shown in terminal. Each lambda
function log line is preffixed with λ symbol. You can hide that logs with the
--no-log option.

This is a convenience method and provides similar output to calling:
$ curl -X POST https://<stage_endpoint_url>/<api>[/method] [-d '<data>'] [-i]

### USAGE
<pre>
  mantil invoke <api>[/method] [options]
</pre>
### OPTIONS
<pre>
  -d, --data string    Data for the method invoke request
  -i, --include        Include response headers in the output
  -n, --no-logs        Hide lambda execution logs
  -s, --stage string   Target project stage
</pre>
### EXAMPLES
<pre>
==> invoke Default method in Ping api
$ mantil invoke ping
200 OK
pong

==> invoke Hello method in Ping api with 'Mantil' data
$ mantil invoke ping/hello -d 'Mantil'
200 OK
Hello, Mantil

==> invoke ReqRsp method in Ping api with json data payload
$ mantil invoke ping/reqrsp -d '{"name":"Mantil"}'
200 OK
{
   "Response": "Hello, Mantil"
}
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
