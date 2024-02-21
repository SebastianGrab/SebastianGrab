let

func = () =>
	let
		Source = ""
	in
	  Source, 

documentation = [
	Documentation.Name = "Function Name #(cr,lf)", 
	Documentation.Description = "Function Description. #(cr,lf)", 
	Documentation.LongDescription = "Function long Description. #(cr,lf)", 
	Documentation.Category = "Function Category. #(cr,lf)", 
	Documentation.Source = "Quelle. #(cr,lf)", 
	Documentation.Author = "Sebastian Grab: www.smiit.com/kontakt. #(cr,lf)", 
	Documentation.Examples = 
		{
			[
				Description = "#(cr,lf)", 
				Code        = "Verwendung eingeben. #(cr,lf) ", 
				Result      = "Verwendung eingeben. #(cr,lf)"
			]
		}
]

in
  Value.ReplaceType(func, Value.ReplaceMetadata(Value.Type(func), documentation))