<template>
  <sidebar-menu :menu="menu" />
</template>
 
 <script>
 import AUTH from 'services/auth'
    export default {
        data() {
            return {
                auth: AUTH,
                menu: [
                    {
                        header: true,
                        title: 'Main Navigation',
                        hiddenOnCollapse: true
                    },
                    {
                        href: '/dashboard',
                        title: 'Dashboard',
                        icon: 'fa fa-user'
                    },
                    {
                        href: '#',
                        title: 'Personal Information',
                        icon: 'fa fa-user'
                    },
                    {
                        href: '#',
                        title: 'Add Course & Subjects',
                        icon: 'fa fa-chart-area',
                        child: [
                            {
                                href: '/charts/sublink',
                                title: 'Edit'
                            }
                        ]
                    },
                    {
                        href: '/login',
                        title: 'Log Out',
                        icon: 'fa fa-chart-area',
                        // AUTH.logout()
                    
                    }
                ]
            }
        },
        methods:{
        //     onToggleCollapse(collapsed) {},
        //     onItemClick(event, item) {}
        }
    }
</script> 
   