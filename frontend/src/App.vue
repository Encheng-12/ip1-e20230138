<script setup lang="ts">
import { ref, computed } from 'vue'
import LoginPage from './page/LoginPage.vue'
import MyRoomPage from './page/MyRoomPage.vue'
import InvoicesPage from './page/InvoicesPage.vue'
import ReportIssuePage from './page/ReportIssuePage.vue'
import LandlordDashboardPage from './page/LandlordDashboardPage.vue'

// Temporary screen switcher for Check 1. Replaced by Vue Router in Check 2.
const screens = {
  login: { label: 'Login', icon: '⏻', comp: LoginPage },
  room: { label: 'My room', icon: '⌂', comp: MyRoomPage },
  invoices: { label: 'Invoices', icon: '$', comp: InvoicesPage },
  issue: { label: 'Report issue', icon: '✎', comp: ReportIssuePage },
  landlord: { label: 'Dashboard', icon: '▦', comp: LandlordDashboardPage },
} as const
type Key = keyof typeof screens
const current = ref<Key>('login')
const tenantKeys: Key[] = ['room', 'invoices', 'issue']
const landlordKeys: Key[] = ['landlord']
const view = computed(() => screens[current.value].comp)
</script>

<template>
  <div v-if="current === 'login'" class="login-bg">
    <LoginPage />
    <button class="btn ghost" style="position:fixed;bottom:1rem;right:1rem" @click="current = 'room'">Preview app</button>
  </div>
  <div v-else class="shell">
    <aside class="sidebar">
      <div class="logo">Room<span>Rent</span></div>
      <div class="side-title">Tenant</div>
      <button v-for="k in tenantKeys" :key="k" class="side-btn" :class="{ active: k === current }" @click="current = k">
        <i>{{ screens[k].icon }}</i>{{ screens[k].label }}
      </button>
      <div class="side-title">Landlord</div>
      <button v-for="k in landlordKeys" :key="k" class="side-btn" :class="{ active: k === current }" @click="current = k">
        <i>{{ screens[k].icon }}</i>{{ screens[k].label }}
      </button>
      <div class="side-title">Account</div>
      <button class="side-btn" @click="current = 'login'"><i>⏻</i>Sign out</button>
    </aside>
    <div class="main">
      <header class="topbar">
        <input type="search" placeholder="Search rooms, invoices…" aria-label="Search" />
        <div class="user"><span class="avatar">SC</span>Sokha Chan</div>
      </header>
      <component :is="view" />
    </div>
  </div>
</template>