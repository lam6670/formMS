<template>
  <div class="body-left">
        <div class="sidebar">
            <div class="toggle"></div>
            <div class="logo"></div>
        </div>
        <div class="menu">
            <div class="menu-item">
                <div class="icon overview"></div>
                <div class="item-name">Tổng quan</div>
            </div>
            <div class="menu-item">
                <div class="icon report"></div>
                <div class="item-name">Báo cáo</div>
            </div>
            <div class="menu-item">
                <div class="icon dashboard"></div>
                <div class="item-name">Mua hàng</div>
            </div>
            <div class="menu-item">
                <div class="icon employee"></div>
                <div class="item-name">Danh mục khách hàng</div>
            </div>
            <div class="menu-item">
                <div class="icon employee"></div>
                <div class="item-name">Danh mục nhân viên</div>
            </div>
            <div class="menu-item">
                <div class="icon setting"></div>
                <div class="item-name">Thiết lập hệ thống</div>
            </div>
        </div>
    </div>
</template>

<script>


export default {
}
</script>

<style scoped>
.body-left {
    background-color: #ffffff;
    width: 200px;
    height: 100%;
    border-right: 1px solid #bbbbbb;
    display: flex;
    flex-direction: column;
}

    .body-left .sidebar {
        height: 50px;
        display: flex;
    }

        .body-left .sidebar .toggle {
            width: 50px;
            height: 50px;
            background-image: url('../assets/toggle.png');
            background-repeat: no-repeat;
            background-size: 22px;
            background-position: 18px center;
            cursor: pointer;
        }

        .body-left .sidebar .logo {
            width: 138px;
            height: 50px;
           background-image:url('../assets/cukcuk-logo.png') ;
            background-size: 126px;
            background-repeat: no-repeat;
            background-position: 0px 9px;
            cursor: pointer;
        }

    .body-left .menu {
        position: relative;
        flex: 1;
    }

        .body-left .menu .menu-item {
            display: flex;
            align-items: center;
            cursor: pointer;
        }

            .body-left .menu .menu-item:hover {
                background-color: #E9EBEE;
            }

            .body-left .menu .menu-item .icon {
                width: 50px;
                height: 45px;
                background-repeat: no-repeat;
                background-size: 22px;
                background-position: 18px center;
            }

                .body-left .menu .menu-item .icon.overview {
                    background-image: url('../assets/dashboard.png');
                }

                .body-left .menu .menu-item .icon.report {
                    background-image: url('../assets/report.png');
                }

                .body-left .menu .menu-item .icon.dashboard {
                    background-image: url('../assets/dashboard.png');
                }

                .body-left .menu .menu-item .icon.employee {
                    background-image: url('../assets/dic-employee.png');
                }

                .body-left .menu .menu-item .icon.setting {
                    background-image: url('../assets/setting.png');
                }
            .body-left .menu .menu-item .item-name {
                width: 150px;
            }
</style>