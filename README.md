# 19AI308-Object-Oriented-Programming-using-CSharp-Exp-10-File-Manipulation
Develop a C# program to get the values from the user using structure and store it in a file in a specific path using file stream concept
# AIM:
To develop a C# program using file streams.

# PROGRAM:
```
using System;
using System.IO;

struct UserData
{
    public string Name;
    public int Age;
    public string Email;
}

class Program
{
    static void Main(string[] args)

    {
        string filePath = @"C:\Users\SEC\OneDrive\Desktop\exp 10.txt";
        UserData[] ud=new UserData[3];
        for(int i=0; i<3;i++)
        {
            Console.WriteLine("Enter your name:");
            ud[i].Name = Console.ReadLine();

            Console.WriteLine("Enter your age:");
            ud[i].Age = int.Parse(Console.ReadLine());

            Console.WriteLine("Enter your email:");
            ud[i].Email = Console.ReadLine();

            WriteUserDataToFile(filePath, ud[i]);
        }  
        Console.WriteLine("User data has been saved to the file.");
    }

    static void WriteUserDataToFile(string filePath, UserData userData)
    {
        using (StreamWriter writer = File.AppendText(filePath))
        { 
            writer.WriteLine($"Name: {userData.Name}");
            writer.WriteLine($"Age: {userData.Age}");
            writer.WriteLine($"Email: {userData.Email}");  
        }
    }
}
```
# OUTPUT:
![Screenshot 2024-05-12 205638](https://github.com/Migaleyy/19AI308-Object-Oriented-Programming-using-CSharp-Exp-10-File-Manipulation/assets/118262199/2a14b16b-f48e-40d8-8ca7-9ff9ddc2d71f)
![Screenshot 2024-05-12 205647](https://github.com/Migaleyy/19AI308-Object-Oriented-Programming-using-CSharp-Exp-10-File-Manipulation/assets/118262199/ed0c9481-2646-418e-831f-0eec2397dc94)

# RESULT:
Thus the C# program to get the values from the user using structure and store it in a file in a specific path using file stream concept executed successfully.
