<html>
 <head>
	 <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
 </head>
	
  <body>
	<div id="page"> Webpage Home </div>
	  <div id="myDiv" contenteditable="true">Edit me!</div>
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
   			console.log('load1');
      window.addEventListener('message', function(event) {
		console.log('msg evt 1');
            // Ensure the message is from a trusted source
           // if (event.origin !== 'https://your-trusted-domain.com') {
           //     return;
           // }
	    
	    console.log(event.data);
            const eventmsg = event.data;
            if (eventmsg.type === 'chasitor.sendMessage') {
                console.log('Received message:', eventmsg.message);
		document.getElementById("page").innerText = eventmsg.message;
                // Handle the message as needed
            }
        });
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	}; 
 

    <script>
        const div = document.getElementById('myDiv');

        div.addEventListener('input', function() {
            console.log('Content changed:', div.innerHTML);
        });
    </script>
</script>
<script type='text/javascript' src='https://creative-bear-b8shsi-dev-ed.trailblaze.my.site.com/ESWUrsaMajorChat1744409620663/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'>
	
</script>

  </body>
</html>
