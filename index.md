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
            identityToken:"eyJraWQiOiIxMjM0NSIsImFsZyI6IlJTMjU2In0.eyJpc3MiOiJ0ZXN0SXNzdWVyIiwic3ViIjoia3NpbGxhQHNhbGVzZm9yY2UuY29tIiwiZXhwIjoxNzM1MjE4Nzg0LCJpYXQiOjE3MzUyMTI3ODR9.hv2SRfFIpKUwZ6r_hcSNqPFnj8pbkKDsFNtSKaJ4RMWjMK2CgC3GGwGxXDLWSbPwRVtemokTCjNPYyZr3RV30BpYUql2ESLcgqeB4WalUOy5cmoTulqXyGX1XcCddI7TCy0S1HAyuAzlZ1aOeLVtrDp9094AOQMlXHQkVd91tMTDyrbslqDBnE_4ULaHhGk7eE92gYlM8DQyFyRwVHlj2uVgRYqTjEx3X5pOLPXSJi0suoJsW7RtycqZrRgkfm0n8AIntPOSRR_LfNiNz2fszzvwF0yaDg52-6kxo_76wK0VP5Y6kwgKwyaCwqL7Hy2Vo5GvCgbv4fBoEPT_Mp46wg"
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
