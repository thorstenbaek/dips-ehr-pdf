<script>
    import {oauth2 as Smart} from 'fhirclient';
	import {onMount} from 'svelte';

    onMount(async () => {
		Smart.authorize({
			// clientId: 'dips-ehr-pdf',			
			// clientSecret: 'SuperSecretPassword',
			// scope: 'openid launch online_access fhirUser launch/patient patient/DocumentReference.write patient/DocumentReference.read patient/Patient.read patient/encounter patient/resource',						
			// redirectUri: './app',			

			/*iss:		  'https://launch.smarthealthit.org/v/r3/sim/'
			  			+ 'eyJoIjoiMSIsImIiOiJmMDQ2MjkzNi1lYjRiLTRkYT'
			  			+ 'EtYjQ1YS1mYmQ5NmViZjhjY2IiLCJlIjoic21hcnQt'
			  			+ 'UHJhY3RpdGlvbmVyLTcxNjE0NTAyIn0/fhir',*/
			iss: 'https://vt-selecta-b.dips.local/DIPS-WebAPI/HL7/FHIR-R4',
			// iss: 'https://localhost:5001',
			launch: 'cdp2010025::DocumentReference/ako1005527',

			clientId: "openehr-client",
			redirectUri: "http://localhost:8080/app",	
            //iss: 'https://localhost:44308',
            scope: "openid profile",
            // launch: "patient:encounter:resource",
		});
	});
</script>        