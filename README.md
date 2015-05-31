<html>
<meta charset="UTF-8">
<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">


<head>
<title>Mapa do Desemprego 2015 - Força Sindical</title>
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
<script>
$(document).ready(function () {
    $('select#location').change(function(){
        var iframeSrc = $(this.selectedOptions[0]).attr('data-value');
        $('#container').fadeOut(500,function(){
            $('#container iframe').attr('src',iframeSrc);
            $('#container iframe').load(function() {
            	$('#container').fadeIn(500);
            });
            
        });
        return false;
    });
});

</script>
<style>


.cartoclone {
	margin-left: 0px;
	margin-top: 0px;
	z-index: 4;
	max-width: 500px;
	display: block;
	background-color: rgba(255, 102, 0, 0.701961);
	border-radius:3px;
	font-size:20px;
	color:#FFF;
	position: absolute;

}</style>
</head>
<body>
<select class="cartoclone" style="left:520px;top:56px;height:45px;" id="location">

  <option data-value="https://diogoriemerblanco.cartodb.com/viz/9e4e9900-073b-11e5-a401-0e6e1df11cbf/embed_map">Todos os setores por estado</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/a7cedce0-0738-11e5-8375-0e43f3deba5a/embed_map">Administração Pública</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/9c61069a-073c-11e5-aff4-0e6e1df11cbf/embed_map">Agropecuária, extrativa vegetal, caça e pesca</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/deeaa97e-0734-11e5-b7bd-0e8dde98a187/embed_map">Comércio</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/fc7ca084-0732-11e5-9c81-0e49835281d6/embed_map">Construção Civil</option>

  <option data-value="https://diogoriemerblanco.cartodb.com/viz/b2d6bdc2-0721-11e5-904b-0e6e1df11cbf/embed_map">Extrativa Mineral</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/af921f4c-072d-11e5-8143-0e43f3deba5a/embed_map">Industria de transformação</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/51dcc27c-0736-11e5-bf47-0e8dde98a187/embed_map">Serviços</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/e1b731bc-0730-11e5-8f3b-0e5e07bb5d8a/embed_map">Serviços industriais de Utilidade Pública</option>
  <option data-value="https://diogoriemerblanco.cartodb.com/viz/16ef08e6-07cc-11e5-9a78-0e5e07bb5d8a/embed_map">Total Brasil</option>
  </select>
  <div id="container">
  <iframe id='map' width='100%' height='100%' frameborder='0' src='https://diogoriemerblanco.cartodb.com/viz/9e4e9900-073b-11e5-a401-0e6e1df11cbf/embed_map' allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
</div>
</body>
</html>
