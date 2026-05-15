<div id="lightning"></div>

<script src="https://crm.vax.co.uk/lightning/lightning.out.js"></script>
<script>
let flowNameWeb = "SF_ProductDiagnostic_Website";
let params = new URLSearchParams(document.location.search);
let source = params.get("id") ?? "none";
$Lightning.use(
    "c:ProductDiagnosticAppDependencies", // name of the Lightning app
    function() { 
        // Callback once framework and app loaded
        $Lightning.createComponent(
            "c:productDiagnosticApp", // top-level component of your app
            {
                flowName: flowNameWeb,
				source: source
            }, // attributes to set on the component when created
            "lightning", // the DOM location to insert the component
            function(cmp) {
                // callback when component is created and active on the page
            }
        );
    },
    'https://crm.vax.co.uk' // Community endpoint                                            
);
</script>
