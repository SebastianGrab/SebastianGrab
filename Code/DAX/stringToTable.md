stringToTable =
VAR __mystring =
    SUBSTITUTE ( <mystring>, ",", "|" )
VAR __len =
    LEN ( __mystring )
VAR __table =
    ADDCOLUMNS (
        GENERATESERIES ( 1, __len ),
        "mylist", VALUE ( PATHITEM ( __mystring, [Value] ) )
    )
VAR __list =
    SELECTCOLUMNS ( __table, "list", [mylist] )
RETURN
    CALCULATE ( COUNTROWS ( Table ), Table[ID] IN __list )