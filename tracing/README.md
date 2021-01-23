# RPC Responses as Tracing


## Example 

`$> OTEL_RESOURCE_ATTRIBUTES="service.name=besu-dev" OTEL_EXPORTER_OTLP_METRIC_INSECURE=true OTEL_EXPORTER_OTLP_SPAN_INSECURE=true ./gradlew run --args="--network=dev --rpc-http-enabled --metrics-enabled --metrics-protocol=opentelemetry"`

Try interacting with the JSON-RPC API. Here is a simple example using cURL:

`$> curl -X POST --data '{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":53}' http://localhost:8545`

Open the Zipkin UI by browsing to http://localhost:9411/

You will be able to see the detail of your traces.

## References:

* [OpenTelemetry Environment Variable Specification](https://github.com/open-telemetry/opentelemetry-specification/blob/master/specification/sdk-environment-variables.md)