# Registrar
<code>firebase.database().ref('personas').push().set({
  nombre:'Roberto'
	fecha:'22/08/1994'
  });
	</code>
 # Actualizar
firebase.database().ref("personas/"+key+"/").set({
 nombre:'Antonio'
 });
 # Listar
firebase.database().ref("personas/").orderByChild("fecha").on('value', function(snapshot) {
  	$.each(snapshot.val(), function( index, value ) {
  		console.log(value);
     });
 });
 
