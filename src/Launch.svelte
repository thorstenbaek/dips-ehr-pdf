<script>
    import {oauth2 as Smart} from 'fhirclient';
	import {onMount} from 'svelte';

    onMount(async () => {
		Smart.authorize({
			clientId: 'dips-ehr-pdf',			
			scope: 'launch launch/patient patient/DocumentReference.write patient/DocumentReference.read patient/Patient.read patient/encounter patient/resource online_access openid fhirUser',			
			redirectUri: './app',			

			/*iss:		  'https://launch.smarthealthit.org/v/r3/sim/'
			  			+ 'eyJoIjoiMSIsImIiOiJmMDQ2MjkzNi1lYjRiLTRkYT'
			  			+ 'EtYjQ1YS1mYmQ5NmViZjhjY2IiLCJlIjoic21hcnQt'
			  			+ 'UHJhY3RpdGlvbmVyLTcxNjE0NTAyIn0/fhir',*/
			iss: 'https://vt-selecta-b.dips.local/DIPS-WebAPI/HL7/FHIR-R4',
			launch: '6c5d9ca9-54d7-42f5-bfae-a7c19cd217f2::DocumentReference/c1c5fdad-eda4-4e9d-89b0-2a7d8eed45cb'

		});
	});
</script>        