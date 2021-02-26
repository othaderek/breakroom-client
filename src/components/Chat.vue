<template>
    <div>Chat</div>
</template>

<script>
    export default {
        name: 'Chat',
        mounted () {
            console.log('mounted')
            this.$socket.emit('mounted', 'Message from client')
            this.$socket.emit('join-room', Object.keys(this), 11)
            },
        sockets : {
            test(data) {
                console.log('test triggered: ', data)
                },
            connect() {
                console.log('connected')
                },
            disconnect() {
                console.log("server disconnected");
                }
            }

    }
</script>