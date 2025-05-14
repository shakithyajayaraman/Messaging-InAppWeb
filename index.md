<html>
 <head>
	 <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
 </head>
	
  <body>
	<div id="page"> Webpage Home </div>
	  <input type="hidden" id="custId" name="custId" value="3487">
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
   			
      window.addEventListener('message', function(event) {
	
            // Ensure the message is from a trusted source
           // if (event.origin !== 'https://your-trusted-domain.com') {
           //     return;
           // }
	    
	    console.log(event.data);
            const eventmsg = event.data;
            if (eventmsg.type === 'chasitor.sendMessage') {
                console.log('Received message:', eventmsg.message);
		const div = document.getElementById('myDiv');
		div.innerText = 'lwc:hidden '+ eventmsg.message;
 		embeddedservice_bootstrap.utilAPI.sendTextMessage(div.innerHTML);
                // Handle the message as needed
            }
        });
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	}; 
 
        const div = document.getElementById('page');

        div.addEventListener('input', function() {
            console.log('Content changed:', div.innerHTML);
	    embeddedservice_bootstrap.utilAPI.sendTextMessage(div.innerHTML);
        });
    
</script>
<script type='text/javascript' src='https://creative-bear-b8shsi-dev-ed.trailblaze.my.site.com/ESWUrsaMajorChat1744409620663/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'>
	
</script>

  </body>
</html>
