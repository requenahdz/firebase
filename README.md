# Importar

<pre><code>
 <script src="https://code.jquery.com/jquery-3.3.1.min.js"></script> 
 <script src="https://www.gstatic.com/firebasejs/5.8.1/firebase.js"></script>
</code></pre>



# Registrar
<pre><code>
firebase.database().ref('personas').push().set({
  nombre:'Roberto',
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


