<script setup lang="ts">
const showSettings = ref(false)
</script>
<template>
    <div class="settings-toggler z-50">
        <v-btn icon color="primary" variant="elevated" @click="showSettings = !showSettings">
            <span class="i-iconoir-settings text-2xl"></span>
        </v-btn>
        <Transition name="fade">
            <div v-if="showSettings">
                <ThemeToggler color="secondary" />
                <LocaleToggler />
            </div>
        </Transition>
    </div>
</template>

<style scoped>
.settings-toggler {
    bottom: 1rem;
    right: 1rem;
    position: fixed;
}
.theme-toggler {
    bottom: 5rem;
    right: 1rem;
    position: fixed;
}

.locale-toggler {
    z-index: 1000;
    bottom: 9rem;
    right: 1rem;
    position: fixed;
}

.fade-enter-active,
.fade-leave-active {
    transition: all 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

/* CSS HSL */
--yinmn-blue{ color:hsla(212, 64%, 35%, 1); }
--yellow{ color:hsla(60, 93%, 53%, 1); }
--eerie-black{ color:hsla(171, 27%, 10%, 1); }
--chili-red { color:hsla(6, 82%, 53%, 1); }
--amber{ color:hsla(45, 91%, 50%, 1); }
--seal-brown{ color:hsla(21, 53%, 25%, 1); }
--beige{ color:hsla(90, 34%, 86%, 1); }
--pear{ color:hsla(67, 81%, 49%, 1); }
--drab-dark-brown{ color:hsla(48, 52%, 13%, 1); }
--forest-green{ color:hsla(117, 41%, 37%, 1); }


/* SCSS Gradient */
--gradient-top{ background: linear-gradient(0deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-rightcolor{ background: linear-gradient(90deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-bottom{ background: linear-gradient(180deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-left{ background: linear-gradient(270deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-top-right{ background: linear-gradient(45deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-bottom-right{ background: linear-gradient(135deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-top-left{ background: linear-gradient(225deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-bottom-left{ background: linear-gradient(315deg, #215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}
--gradient-radial{ background: radial-gradient(#215694ff, #F6F518ff, #13211Fff, #E93823ff, #F4BA0Cff, #61351Eff, #DCE8D0ff, #C9E218ff, #332C10ff, #3C8538ff);}



</style>
