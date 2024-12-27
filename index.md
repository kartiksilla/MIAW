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
            identityToken:"eyJraWQiOiIxMjM0NSIsImFsZyI6IlJTMjU2In0.eyJpc3MiOiJ0ZXN0SXNzdWVyIiwic3ViIjoia3NpbGxhQHNhbGVzZm9yY2UuY29tIiwiZXhwIjoxNzM1Mjg4NDk3LCJpYXQiOjE3MzUyODI0OTd9.W-9U1MckGQkpqRde2eApQWqtjIN5GJ0LD0aKCU6RbMaE7p14mdVYAeKBMaZ7jfc2XOoEILPrbpkUFZCBtPBpUwyKlCZCa_aIJ0Qd-tHnz-8MdtFv2JdJ0cI2WlIHNNrYAM54a32xAkX9DmJrVIJcK3UbfH0vPxSND90GyEEdvWO9aIlmMTuU3qWnqudOH2eRETfqItPlGxAGFTy9q9Dw_f9c075KcAD7YbUY1TiGbdjkAcdGMOuim0ZHvPQ49Vt2oTdXc5nbn31nu2N7v9SuknXlzltviSj3m_k-caSXClvDKOxHOAaHbs52Bh8HEkZJCgmoT5lDvcopB8Hj5Dk39w"
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
