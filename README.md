<pre lang=vb.net>
Module Module1

    Sub Main()
        'Variable Declaration
        ' Dim identifier As DataType (value)
        Dim num As Integer
        Dim myString As String = "This is a a string"

        ' Constant declaration
        ' const Identifier as DataType = Value
        Const planck As Double = 6.62607015E-34

        ' assignment
        ' variable = value
        num = 123
        myString = "This is assigning a value to the variable"

        'Assignment from user input
        'Console.ReadLine()
        'Reads as a string
        'VB is forgiving and will allow parsing (conversion) to data type of variable (in most cases)
        Console.Write("Enter some text: ")
        myString = Console.ReadLine
        Console.Write("Enter a number: ")
        num = Console.ReadLine ' Don't need to convert

        '''''''''''''''''''''''''''''''''''''''''''
        '''NOTE''''''''''''''''''''''''''''''''''''
        '''''''''''''''''''''''''''''''''''''''''''
        'You can convert on entry but it is not required in the coding requirements
        'If you mistakenly forget to declare the data type you would need to convert on first entry
        Console.Write("Enter a number: ")
        num = Convert.ToInt32(Console.ReadLine())
        Console.Write("Enter a real number: ")
        Dim dNum = Convert.ToDouble(Console.ReadLine)
        ''''''''''''''''''''''''''''''''''''''''''''''''''''''
        '''
        'Iteration
        ' For Loops
        For i = 0 To 10
            Console.WriteLine(i) ' output 0 to 10 inclusive
        Next

        'User input to guide number of times to loop
        Console.Write("Enter how many times to loop")
        num = Console.ReadLine
        For i = 1 To num
            Console.WriteLine(i)
        Next

        ' loops with different increments
        For i = 1 To 9 Step 3
            Console.WriteLine(i) ' 1 4 7 (step/increment of 3)
        Next
        For i = 10 To 1 Step -1
            Console.WriteLine(i) ' 10 to 1 counting down
        Next

        'Condition controlled loops
        num = 10
        While num > 0
            num -= 1 ' num = num - 1
        End While
        num = 10
        Do
            num -= 2 ' num = num - 2
        Loop While num > 0
        num = 10
        Do
            num -= 1
        Loop Until num = 0

        ' Nested iteration
        Dim found As Boolean = False
        Dim counter As Integer = 1
        While Not found

            For i = 1 To 10
                Console.WriteLine(i)
            Next
            counter += 1
            If counter = 10 Then
                found = True
            End If
        End While

        For i = 1 To 10
            For j = 1 To 10
                Console.WriteLine($"{i} {j}")
            Next
        Next

        For i = 1 To 10
            found = False
            While Not found
                Console.Write("Enter your guess: ")
                num = Console.ReadLine
                If num = i Then
                    found = True
                End If
            End While
        Next
    End Sub

End Module
