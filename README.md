# specs2yuml

 specs2yuml script [NodeJS](http://nodejs.org)
 Convert specs into a yuml

## Example

    $ ./specs2yuml [DIR]

## How To (SPECS)

### transforms.json

JSON file witch contains the relationships between entities

### Example

	{
		"profiles":
		{
			"associations":
			{
				"users":
				{
					"type":"has-many"
				,	"target":"users"
				,	"target_key":"id_profile"
				}
			}
		}
	,	"users":
		{
			"associations":
			{
				"profile":
				{
					"type":"belongs-to"
				,	"target":"profiles"
				,	"key":"id_profile"
				}
			}
		}	
	}

### mappings.json

JSON file witch contains the entities fields

### Example

	{
		"profiles":
		{
			"fields":
			{
				"id":"ID"
			,	"profile":"PROFILE"
			}
		}
	,	"users":
		{
			"fields":
			{
				"id":"ID"
			,	"first_name":"FIRST_NAME"
			,	"last_name":"LAST_NAME"
			,	"username":"USERNAME"
			,	"password":"PASSWORD"
			,	"id_profile":"ID_PROFILE"
			}
		}		
	}