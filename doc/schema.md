## Schema for user table

	{
		"type":"object",
		"properties":{
			"username":{"type":"string"},
			"password":{"type":"string"},
			"firstName":{"type":"string"},
			"lastName":{"type":"string"},
			"mail":{"type":"string"},
			"profileImg":{"type":"string"},
			"lastLogin":{"type":"number"},
			"presentations":{"type":"array"}
	   }
	}

### Exmaple use:

	{
		"username":"usr123",
		"password":"sfoidfu3453oeriuf234",
		"firstName":"Vegard",
		"lastName":"Schau",
		"mail":"vegaes15@uia.no",
		"profileImg":"path_on_serv/img.jpg",
		"lastLogin":"34598374958734",
		"presentations":[pres_object, pres_object]
	}

## Schema for presentations

	{
		"type":"object",
		"properties":{
			"author":{"type":"string"},
			"name":{"type":"string"},
			"pages":{
				"type":"array",
				"items":{
					"type":"object",
					"properties": {
						"body":"string"
					}
				}
			},
			"created":{"type":"number"}
		}
	}

### Example use:

	{
		"author":"vegard",
		"name":"Mysuper presentation",
		"pages":[{"body":"
			<div class=center>
				<p id=infoBox></p>
				<input placeholder=Whats your name?.. class='input' id='input'/>
				<button class='btn' id='btnSend'>Say hi</button>
				<br><br>
				<h2 id='txtOut'></h2>
			</div>
			"}, {"body":"
			<h1>Page 2</h1>
			"}],
		"created":"193485039480"
	}
