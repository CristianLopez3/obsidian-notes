

### Dependencies 

* Migrate all the `javax` usages for `jakarta usages`.
* `info.app.version` pass to be `info.application.version`
* `net.sf.cache` now it's `org.cache` and the **JMX** is no longer needed here.
* Use `jupiter` instead of `junit`.
* For the controllers advisers (exceptions) use `HttpStatusCode` instead of `HttpStatus`

### Tracing

Be ware of the use of open tracing, specially if you have a custom set up - you may find a problem with the `message_id` header filter that might be included in each event, for this you may have to add a custom class to add the `message_id` before the filter validate this or you may want to deactivate the `opentracing.rabbitmq.enabled` property (it may a little bit different).