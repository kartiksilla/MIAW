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
            identityToken:"eyJraWQiOiIxMjM0NSIsImFsZyI6IlJTMjU2In0.eyJpc3MiOiJ0ZXN0SXNzdWVyIiwic3ViIjoia3NpbGxhQHNhbGVzZm9yY2UuY29tIiwiZXhwIjoxNzM1MjI5ODk1LCJpYXQiOjE3MzUyMjM4OTV9.Serb07kbNgPCjU_RIR1U8v78B53dScchzym5OmTdrWQTR4u095YyKfkFMebe29imSMark8JJKxBDeejsDanLyJMndTjlkzXqn1MZitmm2MALmS3NNaF5kBvGigLhhoceaKWIRkw2Ih1ZVQQx5NYje_dDr-hT5Oetw_vBzTf_-qqLRo0-3rt1E_-XtV9WhQSTfPGc-5MxB9piukK_18Ld7Y2L8ybElYHYQ6fYmVy_Kzlb9jV4EG9ao6Y-O_xl-kZz4KjoFQoX9KdHgHdsftv21gY57O6-uXVhj41b8w6KcggN295q-Fz0DexkL5kVPM56k1AXzjxfFudFC336UJvXEg"
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
