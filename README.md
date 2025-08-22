
```csharp
using ReadMe;
internal class Program
{
    static void Main(string[] args)
    {
        AboutMe aboutMe = new AboutMe(
            Name: "Fayad Alhanash",
            Title: "Software Developer",
            LinkedIn: "https://www.linkedin.com/in/fayadalhanash",
            Address: new Address(City: "Västerås"),
            Skills: new List<string>
            {
                "C#",
                "C",
                "F#",
                "Python",
                "TypeScript",
            });

        Console.WriteLine(aboutMe.ToString());
    }
}
```
<!--
```csharp
namespace ReadMe
{
    record AboutMe(string Name, string Title, string LinkedIn, Address Address, IEnumerable<string> Skills)
    {
        public override string ToString() =>
            $"""
            {Name}
            Title:    {Title}
            LinkedIn: {LinkedIn}
            Address:  {Address.City}
            Skills:   {string.Join(", ", Skills)}
            """;
    }
    record Address(string Street ="", string City = "", string ZipCode = "", string Country = "");
```
-->
