# Registrar
<pre><code>
firebase.database().ref('personas').push().set({
  nombre:'Roberto'
	fecha:'22/08/1994'
});
</code></pre>

# Actualizar
<pre><code>
firebase.database().ref("personas/"+key+"/").set({
 	nombre:'Antonio'
});
</code></pre>

# Listar
<pre><code>
firebase.database().ref("personas/").orderByChild("fecha").on('value', function(snapshot) {
  	$.each(snapshot.val(), function( index, value ) {
		console.log(index)
  		console.log(value);
	});
});
</code></pre>


