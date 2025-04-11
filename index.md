<html>
  <body>
    <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DQy00000HIzzJ',
				'MessagingWebDeployment',
				'https://creative-bear-b8shsi-dev-ed.trailblaze.my.site.com/ESWMessagingWebDeployment1744359291863',
				{
					scrt2URL: 'https://creative-bear-b8shsi-dev-ed.trailblaze.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://creative-bear-b8shsi-dev-ed--c.trailblaze.vf.force.com/apex/ESWMessagingWebDeployment1744359291863/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>


  </body>
</html>
