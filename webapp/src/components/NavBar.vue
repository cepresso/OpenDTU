<template>
    <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">OpenDTU</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup"
                aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" ref="navbarCollapse" id="navbarNavAltMarkup">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <router-link @click="onClick" class="nav-link" to="/">Live Data</router-link>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarScrollingDropdown" role="button"
                            data-bs-toggle="dropdown" aria-expanded="false">
                            Settings
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="navbarScrollingDropdown">
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/settings/network">Network Settings</router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/settings/ntp">NTP Settings</router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/settings/mqtt">MqTT Settings</router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/settings/inverter">Inverter Settings
                                </router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/settings/dtu">DTU Settings</router-link>
                            </li>
                            <li>
                                <hr class="dropdown-divider" />
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/settings/config">Config Management</router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/firmware/upgrade">Firmware Upgrade</router-link>
                            </li>
                        </ul>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarScrollingDropdown" role="button"
                            data-bs-toggle="dropdown" aria-expanded="false">
                            Info
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="navbarScrollingDropdown">
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/info/system">System</router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/info/network">Network</router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/info/ntp">NTP</router-link>
                            </li>
                            <li>
                                <router-link @click="onClick" class="dropdown-item" to="/info/mqtt">MqTT</router-link>
                            </li>
                        </ul>
                    </li>
                    <li class="nav-item">
                        <router-link @click="onClick" class="nav-link" to="/about">About</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    methods: {
        onClick() {
            this.$refs.navbarCollapse && this.$refs.navbarCollapse.classList.remove("show");
        }
    },
}
</script>
