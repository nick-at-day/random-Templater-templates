<%*
let gate1
while (gate1==null)
{
	gate1 = await tp.system.suggester(
		[
			"Yes",
			"No"
		],
		[
			true,
			false
		],
		true,
		"Am I surprised by the note title?"
	)
		if (gate1==true)
			{
				alert("Set Review to Hard")
				break
			}
	gate1 = await tp.system.suggester(
		[
			"Yes",
			"No"
		],
		[
			true,
			false
		],
		true,
		"Am I surprised by the note content?"
	)
		if (gate1==true)
			{
				alert("Set Review to Hard")
				break
			}
	gate1 = await tp.system.suggester(
		[
			"Yes",
			"No"
		],
		[
			false,
			true
		],
		true,
	"Can I easily link to other notes?"
	)
	if (gate1==true)
		{
			alert("Set Review to Hard")
			break
		}
	gate1 = await tp.system.suggester(
		[
			"Yes",
			"No",
			"No, and it's boring"
		],
		[
			true,
			false,
			"bad"
		],
		true,
		"Does the note need work?"
	)
	if (gate1=="bad")
		{
			alert("Set Review to Easy")
			break
		} else if (gate1==false){
			alert("Set Review to Good")
			break
		}
	gate1 = await tp.system.suggester(
		[
			"Yes",
			"No"
		],
		[
			true,
			false
		],
		true,
		"Can I tag the work that needs to be done?"
	)
	if (gate1==true)
		{
			alert("Set Review to Good")
			break
		} else {
			alert("Set review to Hard")
			break
		}
}
-%>