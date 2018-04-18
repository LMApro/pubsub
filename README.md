# pubsub
Create your own PubSub Client &amp; Server Websocket

## Js Client

```javascript

    const pubSub = new PubSubClient('ws://localhost:3001', {
      connect: true,
      reconnect: true,
    })

    const topicName = 'abc'

    pubSub.subscribe(topicName, (message) => {
      console.log(`Got message from topic ${topicName}`, message)
    })

    //publish a message to topic
    pubSub.publish(topicName,
      {title: 'Hello subscribers in the topic abc', body: 'How are you ?'})

    // Broadcast send message to subscribers but not me
    pubSub.broadcast(topicName, {body: 'this is broadcast message'})

```



## Video Tutorials
https://www.youtube.com/watch?v=iNr8VsVh_-Q
