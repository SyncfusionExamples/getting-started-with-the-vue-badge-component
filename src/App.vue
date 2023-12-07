<script setup>
import { ButtonComponent as EjsButton } from "@syncfusion/ej2-vue-buttons";
import { ToolbarComponent as EjsToolbar, ItemsDirective as EItems, ItemDirective as EItem } from "@syncfusion/ej2-vue-navigations";
</script>

<template>
      <div class="container_div badge-toolbar ">
       <ejs-toolbar id="toolbar" width="400">
         <e-items>
          <e-item prefixIcon="e-icons e-menu"></e-item>
          <e-item text="Notification"></e-item>
          <e-item type="Separator"></e-item>
          <e-item prefixIcon="e-icons e-search"></e-item>
	        <e-item :template=" 'messageTemplate'">
            <template v-slot:messageTemplate>
              <div class="badge-block">
                <div class="message icons">
                  <span class="e-badge e-badge-notification e-badge-overlap e-badge-primary">99</span>
                </div>
              </div>
            </template>
          </e-item>
	    <e-item :template=" 'userTemplate'">
        <template v-slot:userTemplate>
          <div class="badge-block">
           <div class="user-profile icons">
            <span class="e-badge e-badge-notification e-badge-overlap e-badge-success">10</span>
           </div>
		  </div>
        </template>
      </e-item> 
      <e-item :template=" 'loveTemplate'">
        <template v-slot:loveTemplate>
          <div class="badge-block">
            <div class="love icons">
              <span class="e-badge e-badge-notification e-badge-overlap e-badge-info">43</span>
            </div>
          </div>
        </template>
      </e-item>
        </e-items>
       </ejs-toolbar>
    </div>
<!-- <ejs-button cssClass="e-btn">Inbox
  <span class="e-badge e-badge-overlap e-badge-primary e-badge-dot
               e-badge-bottom"></span>
</ejs-button> -->
</template>

<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-vue-buttons/styles/material.css";
@import "../node_modules/@syncfusion/ej2-vue-notifications/styles/material.css";
@import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
@import "../node_modules/@syncfusion/ej2-vue-navigations/styles/material.css";
.e-btn
{
  position: relative;
}
.container_div.badge-toolbar {
        overflow: auto;
        display: table;
        margin: auto;
        margin-top: 117px;
        padding-top: 20px;
        padding-bottom: 20px;
    }

    .e-icons {
        font-size: 20px;
        font-weight: bolder;
    }

    @media only screen and (max-width: 550px) {
        .container_div.badge-toolbar #toolbar .header {
            display: none;
        }

        .material .container_div.badge-toolbar .e-toolbar .e-toolbar-items:first-child > .e-toolbar-item:last-child {
            margin-right: 9px;
        }

        .bootstrap .container_div.badge-toolbar .e-toolbar .e-toolbar-items:first-child > .e-toolbar-item:last-child {
            margin-right: 10px;
        }
    }

    .container_div.badge-toolbar .badge-block {
        position: relative;
        display: inline-block;
        margin: 12px 12px 10px 10px;
        width: 28px;
        height: 20px;
    }

    .container_div.badge-toolbar .e-toolbar-items {
        align-items: center;
    }

    .header {
        font-size: 18px;
    }

    .icons {
        width: 20px;
        height: 20px;
        display: inline-block;
    }
    /* SVG Icons */
    .love {
     
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='%23a6a5a6' d='M8.532.81c3.029 0 5.932 1.668 7.468 4.521 2.139-3.97 6.922-5.644 11.008-3.726 4.289 2.012 6.177 7.212 4.218 11.617C29.273 17.614 16 31.19 16 31.19 15.916 31.137 2.727 17.614.774 13.222-1.186 8.817.703 3.617 4.993 1.605A8.299 8.299 0 0 1 8.532.81z'/%3E%3C/svg%3E") no-repeat 100% 100%;
    }

    .message {
      position: relative;
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='%23a6a5a6' d='M0 5.126h.024l7.547 7.393 8.405 8.252 8.405-8.252 7.547-7.393H32v22.6H0zm1.902-.852h28.195l-7.048 5.929L16 16.132l-7.049-5.929z'/%3E%3C/svg%3E") no-repeat 100% 100%;
    }

    .user-profile {
      position: relative;
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='%23a6a5a6' d='M8.772 18.363a11.978 11.978 0 0 0 7.229 2.416c2.71 0 5.214-.899 7.229-2.416 4.71.593 8.354 4.61 8.354 9.481V32H.416v-4.156c0-4.871 3.646-8.888 8.356-9.481zM16.001 0a8.727 8.727 0 1 1-.003 17.455A8.727 8.727 0 0 1 16.001 0z'/%3E%3C/svg%3E") no-repeat 100% 100%;
    }
</style>
