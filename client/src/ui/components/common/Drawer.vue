/**
 * BetterDiscord Drawer Component
 * Copyright (c) 2015-present Jiiks/JsSucks - https://github.com/Jiiks / https://github.com/JsSucks
 * All rights reserved.
 * https://betterdiscord.net
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
*/

<template>
    <div :class="['bd-drawer', {'bd-drawer-open': open}]">
        <div class="bd-form-header bd-drawer-header" @click="() => open = !open">
            <span class="bd-form-header-text">{{ label }}</span>
            <span class="bd-form-header-button bd-drawer-open-button">
                <span class="bd-chevron-1"><MiChevronDown /></span>
                <span class="bd-chevron-2"><MiChevronDown /></span>
            </span>
        </div>
        <div class="bd-drawer-contents-wrap">
            <div class="bd-drawer-contents">
                <slot />
            </div>
        </div>
    </div>
</template>

<script>
    import { MiChevronDown } from './MaterialIcon';

    export default {
        props: [
            'label'
        ],
        components: {
            MiChevronDown
        },
        data() {
            return {
                open: false
            }
        }
    }
</script>
