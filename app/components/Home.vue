<template>
    <Page>
        <ActionBar class="action-bar" title="Оплата покупки">
            <ActionItem @tap="onReload"
                        ios.systemIcon="9" ios.position="right"
                        android.systemIcon="ic_menu_share" android.position="actionBar"></ActionItem>
        </ActionBar>
        <ScrollView>
            <WebView ref="webView"  >

            </WebView>
        </ScrollView>
    </Page>
</template>

<script>
    const webViewInterfaceModule = require('nativescript-webview-interface');

    export default {
        data () {
            return {
                scripts: [
                    "https://widget.cloudpayments.ru/bundles/cloudpayments",
                    "https://lmdev.ru/api/payment/27/script.js",
                ],
                oWebViewInterface: null,
            };
        },
        mounted () {


        },
        methods: {
            onReload() {
                console.dir(11111111);
                var webView = this.$refs.webView.nativeView;
                console.dir(222222222);
                this.oWebViewInterface = webViewInterfaceModule.WebViewInterface(webView);

                console.dir(4444444);
            }
        },
    };
</script>
