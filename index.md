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
            identityToken:"eyJraWQiOiIxMjM0NSIsImFsZyI6IlJTMjU2In0.eyJpc3MiOiJ0ZXN0SXNzdWVyIiwic3ViIjoia3NpbGxhQHNhbGVzZm9yY2UxLmNvbSIsImV4cCI6MTczNTIxODc4NCwiaWF0IjoxNzM1MjEyNzg0fQ.nDSY2eTyYpWx2Vl7bXLV2cpkuGuhO_PxPGiUu-v9Y-8Zsi4sCZeI0JwK0og4pBg1hP5EpntOKGfYEdytzTyJJrVz3XEuyiAILTkY_VvMa5yECkgp9ShuzZYvsdcDrjSd4-PDmv1GLlTpcZjGEKYQ24TQ8PTDyIziTPvMB5fiKwuz9EMEtaWl2e9gSwybzSpOJIdUqemoMk6GxyF4rpqbLZ4GArw7Ijnj815vwLqBfk6Kgds0P1o0LhXzDjYg682anWlveM_AA8xdBvUGPoaYk_4IqP08lt0qLvIs8o1OEcdVRjgUw8-60zo8ECJTunrZyMm8PQ2rqbepz6kk8zmQMw"
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
