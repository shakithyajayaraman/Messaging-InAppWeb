<html>
 <head>
	 <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
 </head>
	
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
	window.addEventListener('message', function(event) {
            // Ensure the message is from a trusted source
            if (event.origin !== 'https://your-trusted-domain.com') {
                return;
            }

            const message = event.data;
            if (message.type === 'chasitor.sendMessage') {
                console.log('Received message from chatbot:', message);
                // Handle the message as needed
            }
        });
</script>

  </body>
</html>
