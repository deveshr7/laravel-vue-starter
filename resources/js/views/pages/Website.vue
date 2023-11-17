<script setup>
//need to import the router to use $route
import { useRoute } from 'vue-router'
import Spinner from "@/views/components/icons/Spinner.vue"
import Main from '@/views/layouts/Main'


const route = useRoute()
// Access the :site param from the URL
const site = route.params.site;
</script>


    <template>
        <Main>
            <div class="flex justify-center">

                <spinner v-if="true" class="w-10 h-10 "></spinner>
                {{site}}
            </div>
        </Main>
    </template>

