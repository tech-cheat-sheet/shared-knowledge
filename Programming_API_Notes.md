- [REST vs gRPC vs SOAP](#rest-vs-grpc-vs-soap)
# REST vs gRPC vs SOAP
| Aspect              | REST (HTTP/1.1)                  | gRPC (HTTP/2 + Protobuf)         | SOAP (XML + WS-*)                                 |
|---------------------|----------------------------------|----------------------------------|---------------------------------------------------|
| Protocol            | HTTP/1.1                         | HTTP/2                           | HTTP, SMTP, XMPP (transport-agnostic)             |
| Data Format         | JSON, XML, HTML, Plain Text      | Binary (Protobuf)                | XML only                                          |
| Streaming           | Polling / WebSockets (addon)     | Unary & server/client/bidi streams | Request-response only (no native streaming)     |
| Schema Enforcement  | Optional (OpenAPI/Swagger)       | Mandatory (.proto definitions)   | Mandatory (WSDL)                                  |
| Browser Support     | Universal                        | Limited (needs gRPC-Web proxy)   | Limited (requires SOAP client or WS-* libs)       |
| Performance         | Higher latency, text parsing     | Lower latency, efficient parsing | Higher overhead (XML verbosity & parsing)         |
| Contract Generation | Manual / documented              | Auto-generated client/server stubs | Auto-generated via WSDL (tooling)              |
| Best Fit            | Public APIs, broad clients       | Internal microservices, real-time | Enterprise systems, strict compliance, legacy reuse |
