  
  <template>
    <div class="container bg-warning">
        <div v-for="(mensaje, index) in mensajes" :key="index">

            <p
                :style="{ backgroundColor: mensaje.color, textAlign: mensaje.id === usuarios[0].id.value ? 'left' : 'right' }">
                <small>{{ mensaje.nombreCompleto }}</small><br> {{ mensaje.texto
                }}
            </p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'ChatUsers',
    props: {
        mensajes: Array,
        usuarios: Array
    },
}
</script>
<style scoped>
#chat {
    max-height: 80vh;
    overflow-y: scroll
}
</style>