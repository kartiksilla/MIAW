<html>
  <body>
    <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DHu00000Daj8e',
				'SDO_Messaging_for_Web',
				'https://storm-881b6713f7d5bd.my.site.com/ESWSDOMessagingforWeb1732706091110',
				{
					scrt2URL: 'https://storm-881b6713f7d5bd.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://storm-881b6713f7d5bd.my.site.com/ESWSDOMessagingforWeb1732706091110/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

  </body>
</html>
