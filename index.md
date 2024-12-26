<html>
  <body>
   <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
	 window.addEventListener("onEmbeddedMessagingReady", () => 
        {
            console.log("Received the onEmbeddedMessagingReady event…");

            // Send token to Salesforce
    
            embeddedservice_bootstrap.userVerificationAPI.setIdentityToken
            ({
            identityTokenType : "JWT", 

            //identityToken :"{The JWT token key value that we created in Stage 4}"
            identityToken:"eyJraWQiOiIxMjM0NSIsImFsZyI6IlJTMjU2In0.eyJpc3MiOiJ0ZXN0SXNzdWVyIiwic3ViIjoia3NpbGxhQHNhbGVzZm9yY2UuY29tMSIsImV4cCI6MTczNTIyODcxMywiaWF0IjoxNzM1MjIyNzEzfQ.gWtJ0qhNY3z6J89rsiM451f-WYTjp1vmftIWttlfaKAg-ziWzLMLJxdgA_cCjQ74zhe7GVkLB6opgCxfsBoZeyF8-uP_qXS4anaGZF6nOCbxKfzyDGonickcKVB29KX6pBPMMTzLYt-BsxmL8BePvn1i875NQv6_TkSME15EUgLGBX5m-V_hwzuXqfLqLeU0u9kZieNjBuw44eGPy5BrcjPCHjHs5t5slQLcTe2k_Cxm6xbsNPb2DTBajm4AqtnzbOyyoZE1LtMkbgt2Y8Fmt5rZMAea8SXyIKf37QzS0rN0gm7jCB7Fx77rqCTzfDN-K5gj3nwX5hfPuG5aPYpQ1A"
            });
        });
			embeddedservice_bootstrap.init(
				'00DHu00000Daj8e',
				'Web_chat_test',
				'https://storm-881b6713f7d5bd.my.site.com/ESWWebchattest1734514330164',
				{
					scrt2URL: 'https://storm-881b6713f7d5bd.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://storm-881b6713f7d5bd.my.site.com/ESWWebchattest1734514330164/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>


  </body>
</html>
