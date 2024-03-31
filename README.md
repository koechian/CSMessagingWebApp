# CSMessagingWebApp

A messaging web application built as a take away assignment for Branch International Junior Backend Role.

## Key Facets

### 1. Agents

- Agents are created using a name only. This creates a new record in the database with the following fields:\
  `name:Agent Name`, \
  `uuid:Unique Agent Identification`,\
  `isOccupied:A boolean to indicate weather the agent is free or not`
- Agents can be attached to one or many conversations, to a maximum of 3.
- Agents are destroyed on logout. Meaning they are no longer available for conversations. The messages that they sent will persist in the `Conversations` collection for non-repudiation.

### 2. Messaging

- Initially, a message will be unattached. Meaning that the sender exists but the recepient does not. A message will remain un attached until it is replied to be an Agent. At which point the message will evolve to become a conversation with two parties.
- The message will be deleted from the `Messages` collection and moved to the `Conversations` collection.
