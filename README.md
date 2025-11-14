```
Console.WriteLine("MIs on su lemmikvärvid? Sisesta palun ükshaaval\nKui rohkem värve ei ole, kirjuta \"rohkem pole\"");
List<string> kasutajaVärvid = new List<string>();

string sisestus = "";
do
{
    Console.WriteLine("Sisesta 1 värv korraga: ");
    sisestus = Console.ReadLine();

    if (sisestus != "rohkem pole")
    {
        kasutajaVärvid.Add(sisestus);
    }

} while (sisestus != "rohkem pole");

foreach (var värv in kasutajaVärvid)
{
    switch (värv)
    {
        // punane, oranz, kollane, roheline, helesinine, tumeroheline, lilla,
        // roosa, pruun, must, valge, hall, värvi-ei-tunta
        // roosa & oranz - neid värve ei ole, tagasta sõnum mis on värevispetsiifiline
        case "punane":
            Console.BackgroundColor = ConsoleColor.Red;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- p u n a n e -*-*-");
            break;
        /* LISAGE ISESEISVALT KÕIKIDE MUUDE VÄRVIDE CASED */
        case "oranz":
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("Oranz pole saadaval");
            break;
        case "kollane":
            Console.BackgroundColor = ConsoleColor.Yellow;
            Console.ForegroundColor = ConsoleColor.Black;
            Console.WriteLine("-*-*- k o l l a n e -*-*-");
            break;
        case "roheline":
            Console.BackgroundColor = ConsoleColor.Green;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- r o h e l i n e -*-*-");
            break;
        case "helesinine":
            Console.BackgroundColor = ConsoleColor.DarkBlue;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- h e l e s i n i n e -*-*-");
            break;
        case "tumeroheline":
            Console.BackgroundColor = ConsoleColor.DarkGreen;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- t u m e r o h e l i n e -*-*-");
            break;
        case "lilla":
            Console.BackgroundColor = ConsoleColor.Magenta;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- p u n a n e -*-*-");
            break;
        case "pruun":
            Console.BackgroundColor = ConsoleColor.DarkYellow;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- p r u u n ? -*-*-");
            break;
        case "must":
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- m u s t -*-*-");
            break;

        default:
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine($"Ei tunne sellist värvi{värv}");
            break;

    }
}
