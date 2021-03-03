# Event-orientation
## Concepts
### Durability
Message durability is the ability to store message details out-of-process so they will not be lost before processing.

Message durability is accomplished by persisting the message details to something with higher reliability until receipt is assured.  To disk, for example, is considered more reliable than in memory.
#### See Also
[Durable Subscriber Pattern](#durable-subscriber-pattern)
[Guaranteed Delivery Pattern](#guaranteed-delivery)
### Publish-Subscribe (Pub-Sub)
Publish-subscribe is a means by which to *broadcast* (publish) information to a varying number of receivers (subscribers) without the publisher being affected by subscriber details.
#### See Also
[Enterprise Integration Patterns - Publish-Subscribe Channel](https://www.enterpriseintegrationpatterns.com/patterns/messaging/PublishSubscribeChannel.html)
### Idempotency
In mathematics, idempotent means *denoting an element of a set which is unchanged in value when multiplied or otherwise operated on by itself.*

With [Event Messages](#event-message-pattern) this means that the processing of an event message has the same effect whether it's received once or multiple times.

While a [consumer](#message-consumer-pattern) is responsible for processing an event message, the [producer](#message-producer-pattern) must produce an event message that *can be* processed idempotently. An *event* is a fact; it's the details of something that happened in the past.  A *command* instructs something how to change state.  An event message that describes how the change was made (e.g. how a account balance was changed: +50.00) is a command message *masquerading* as an event message.

#### Accepted Practices
The *type* of the event message should describe *what* happened and the contents should describe the state after the event rather than *how* the state changed.
```csharp
	public enum BalanceUpdateMethod {
		Unknown, Credit, Debit
	}
#nullable disable
public class AccountBalanceUpdatedEvent {
	public string OccurredUtcDateTime {get;set;}
	public string MessageId {get;set;}
	public string? CorrelationId {get;set;}
	public string? TransactionId {get;set;}
	public string AccountId {get;set;}
	public string AccountBalance {get;set;}
}
```
If more domain detail about and event is required then it should be represented in the name of the event.  e.g. providing detail about the *type* of update
```csharp
#nullable disable
public class AccountBalanceDebitedEvent {
	public string OccurredUtcDateTime {get;set;}
	public string MessageId {get;set;}
	public string? CorrelationId {get;set;}
	public string? TransactionId {get;set;}
	public string AccountId {get;set;}
	public string AccountBalance {get;set;}
}
public class AccountBalanceCreditedEvent {
	public string OccurredUtcDateTime {get;set;}
	public string MessageId {get;set;}
	public string? CorrelationId {get;set;}
	public string? TransactionId {get;set;}
	public string AccountId {get;set;}
	public string AccountBalance {get;set;}
}
```
#### See also
[Qtweet Standards - Naming](https://git.rockfin.com/Rocket-Technology-Architecture/qtweet-standards/wiki/Naming)
#### Synchronous Messaging
#### Asynchronous Messaging
## Patterns
### Message Channel
A message "channel" is a logical abstraction of how a message is transported providing a place put messages for transport.

As with Dependency Injection, the "channel" would be the interface to be used and the chosen implementation would be performed separately and made available by a service or Dependency Inversion container.
#### See Also
[Enterprise Integration Patterns - Message Channel](https://www.enterpriseintegrationpatterns.com/patterns/messaging/MessageChannel.html)
### Message Types
#### Event Message Pattern
An *event message* represents a fact; it's the details of something that happened in the past and the resultant state.
##### See Also
[Enterprise Integration Patterns - Event Message](https://www.enterpriseintegrationpatterns.com/patterns/messaging/EventMessage.html)
#### Command Message Pattern
A *command message* represents the instructions that detail how to change state.
##### Accepted Practices
Command Messages are communicated via Point-To-Point Channels (not Publish-Subscribe Channels).
##### See Also
[Enterprise Integration Patterns - Command Message](https://www.enterpriseintegrationpatterns.com/patterns/messaging/CommandMessage.html)
### Guaranteed Delivery Pattern
With guaranteed delivery, a messaging system persists messages until they are received by the receiver or by all of the subscribers.
#### See Also
[Enterprise Integration Patterns - Guaranteed Delivery](https://www.enterpriseintegrationpatterns.com/patterns/messaging/GuaranteedMessaging.html)
#### At Least Once
#### At Most Once
#### Exactly Once
### Dead Letter Channel
AKA Dead Leader Queue
Use a dead letter channel as a means of diverting undeliverable messages to process out-of-band.
#### See Also
[Enterprise Integration Patterns - Dead Letter Channel](https://www.enterpriseintegrationpatterns.com/patterns/messaging/DeadLetterChannel.html)
### Message Consumer Pattern
#### See Also
[Enterprise Integration Patterns - ]()
### Event Subscriber Pattern
A type of message consumer that...
#### See Also
[Enterprise Integration Patterns - ]()
### Durable Subscriber Pattern
#### Accepted Practices
When designing subscribers, default to the Durable Subscriber Pattern.  It's rare that subscriber doesn't expect to *receive all* sent messages.
#### See Also
[Durable Publish-Subscribe Channel Pattern](#durable-publish-subscribe-channel-pattern)
[Enterprise Integration Patterns - Durable Subscriber](https://www.enterpriseintegrationpatterns.com/patterns/messaging/DurableSubscription.html)
### Durable Publish-Subscribe Channel Pattern
### Message Producer Pattern
#### See Also
### Event Publisher Pattern
#### See Also
### Idempotent Consumer Pattern
AKA Idempotent Receiver Pattern
#### See Also
[Enterprise Integration Patterns - Idempotent Receiver](https://www.enterpriseintegrationpatterns.com/patterns/messaging/IdempotentReceiver.html)
#### See Also
[Enterprise Integration Patterns - Event Message](https://www.enterpriseintegrationpatterns.com/patterns/messaging/EventMessage.html)
### Event Bus Pattern
AKA Message Bus Pattern
#### See Also
[Enterprise Integration Patterns - Message Bus](https://www.enterpriseintegrationpatterns.com/patterns/messaging/MessageBus.html)
### Event Stream Pattern
#### See Also
[]()
### Schema Sharing Pattern
This pattern applies equally as well to Command Messages as it does Event Messages.  It's more important with Event Messages
 due to many loosely coupled subscribers (consumers).
#### See Also
[Conﬂuent & Apache Kafka: Patterns / Anti-patterns](https://www.confluent.io/online-talks/patterns-anti-patterns/)
### DTO Sharing Anti-pattern
#### See Also
[]()
### Normalization Pattern
#### See Also
[Enterprise Integration Patterns - Normalizer](https://www.enterpriseintegrationpatterns.com/patterns/messaging/Normalizer.html)
