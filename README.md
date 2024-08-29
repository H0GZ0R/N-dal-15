// Create a new Cat object
Cat newCat = new Cat("Garfield", "ginger");
Console.WriteLine($"{newCat.Name} wants a rub on its belly.");

// While the cat's belly is not full
while (newCat.BellyFull > 0)
{
    newCat.Sleep();
}

// Cat meows and shows its data
newCat.Meow();
newCat.ShowCatData();

// Cat class definition
class Cat
{
    private string _name;
    private string _color;
    private int _bellyFull;

    // Constructor
    public Cat(string name, string color)
    {
        _name = name;
        _color = color;
        _bellyFull = 10;
        Console.WriteLine($"A {color} cat named {name} has been created.");
    }
    
    // Getter for Name property
    public string Name
    {
        get { return _name; }
    }
    
    // Getter for BellyFull property
    public int BellyFull
    {
        get { return _bellyFull; }
    }

    // Method to simulate the cat sleeping
    public void Sleep()
    {
        _bellyFull--;
        Console.WriteLine($"{_name} says: Z-z-Z-z-Z-z");
    }

    // Method to make the cat meow
    public void Meow()
    {
        Console.WriteLine($"{_name} says: Meow!");
    }

    // Method to display the cat's data
    public void ShowCatData()
    {
        Console.WriteLine($"Name: {_name}");
        Console.WriteLine($"Color: {_color}");
        Console.WriteLine($"Level of hungriness: {_bellyFull}");
    }
}
