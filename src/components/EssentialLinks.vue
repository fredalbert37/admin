<template>
    
    <q-list style="margin-bottom: auto!important; flex-direction: column; padding: 0;">
        <q-item 
        tag="router-link"
        clickable 
        v-ripple
        @click="navigateTo"
        :active="active_link"
        >
            <q-item-section v-if="icon" avatar>
                <q-icon :name="icon" />
            </q-item-section>

            <q-item-section> {{title}} </q-item-section>
        </q-item>

    </q-list>
</template>
<script>

import { computed, defineComponent, ref, toRef } from "vue"
import { useRouter } from "vue-router"

export default defineComponent({
    name: 'EssentialLink',
    props: {
        link: {
            type: String,
            default: '/'
        },
        icon: {
            type: String,
            default: ''
        },
        title: {
            type: String,
            default: ''
        },
        active:{
            type: Boolean,
            default: false
        }
    },
    setup(props){
        const router = useRouter()
        let active_link = ref(props.active);

        return {
            active_link,
            navigateTo(){
                this.active_link = true;
                console.log(props.active)
                router.push({
                    name: props.link
                })
            }
        }
    }
})

</script>