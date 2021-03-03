<template>
    <div>
        <audio src=""></audio>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                roomId: '1'
            }
        },
        name: 'Chat',
        mounted () {
            console.log('mounted')
            
            // this.$socket.emit('joined', this.roomId)
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