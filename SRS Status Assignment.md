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
			"#Ever/Seed/Unplanted"
		],
		true,
		"Does the note have topics or backlinks?"
	)
	if (gate1!==true)
		{
		break
		}
	gate1 = await tp.system.suggester(
		[
			"Yes",
			"No"
		],
		[
			true,
			"#Ever/Seed/water"
		],
		true,
		"Does the note have a body?"
	)
	if (gate1!==true)
		{
		break
		}
	gate1 = await tp.system.suggester(
		[
			"Yes",
			"No"
		],
		[
			true,
			"#to/tend/prune"
		],
		true,
		"Do I agree with what the note is saying??"
	)
	if (gate1!==true)
		{
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
		"Is the note a complete concept?"
	)
	if (gate1==true)
		{
			gate1= await tp.system.suggester(
		[
			"Yes",
			"No"
		],
		[
			"#ever/green",
			"#ever/sprout/cultivate"
		],
		true,
		"Is the note used a lot? In practice or in other notes?"
	)
	break
		}
	gate1 = await tp.system.suggester(
		[
			"too small",
			"too large"
		],
		[
			true,
			"#to/tend/graft"
		],
		true,
		"Is it too large or too small?"
	)
	if (gate1!==true)
		{
		break
		}
	gate1 = await tp.system.suggester(
		[
			"yes",
			"no"
		],
		[
			"#ever/sprout/water",
			"#ever/green"
		],
		true,
		"Do I have more to say?"
	)
	if (gate1!==true)
		{
		break
		}
}
tR += gate1
-%>