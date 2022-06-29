# Direktiv

- Direktiv is a container orchestration / workflow engine

- YAML to define flows, subflows, error handling etc. 

- Keeps JSON state across states, state data can be transformed in every step (JQ and JavaScript)

- Knative Serving to execute functions / actions within the flow (serve at :8080, JSON in & out)

- (Can be) Event-driven (cloudevents) internally and integration into Knative Eventing (source & sink)

## States

- noop: No operation, used for logging and transforming
- action: Call Knative function
- consumeEvent: Waiting for a cloud e
- eventsAnd: Wait for 2+ events
- eventsOr: Wait for one event from a list
- delay: Wait
- error: Throw an error
- foreach: Loop over an array
- generateEvent: Generate a cloud event
- getter: Get variable from instance, workflow or namespace scope
- setter: Set variable from instance, workflow or namespace scope
- parallel: Run multiple actions in parallel
- switch: Decision making
- validate: Validate current state or input for flow
