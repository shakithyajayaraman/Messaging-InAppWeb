<html>
  <body>
    <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DQy00000HIzzJ',
				'Ursa_Major_Chat',
				'https://creative-bear-b8shsi-dev-ed.trailblaze.my.site.com/ESWUrsaMajorChat1744409620663',
				{
					scrt2URL: 'https://creative-bear-b8shsi-dev-ed.trailblaze.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://creative-bear-b8shsi-dev-ed.trailblaze.my.site.com/ESWUrsaMajorChat1744409620663/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'>
</script>
  </body>
</html>
