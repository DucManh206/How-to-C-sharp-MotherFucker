🔧 PHẦN 1: CÀI ĐẶT MÔI TRƯỜNG
B1. Cài Visual Studio Code

Tải tại: https://code.visualstudio.com/

Cài bản Windows x64

Sau khi cài → mở VS Code

B2. Cài .NET SDK (bắt buộc)

Tải tại: https://dotnet.microsoft.com/download

Chọn .NET SDK (LTS – khuyên dùng .NET 8 LTS)

👉 Kiểm tra đã cài thành công:

dotnet --version


Nếu hiện số version → ✅ OK

B3. Cài Extension C#

Mở VS Code

Extensions (Ctrl + Shift + X)

Tìm C# (by Microsoft) → Install

📌 Extension này cung cấp:

IntelliSense

Debug

Build & Run C#

▶️ PHẦN 2: TẠO & CHẠY PROJECT C#
Tạo project Console
dotnet new console -n HelloCSharp
cd HelloCSharp
dotnet run


📂 Cấu trúc thư mục:

HelloCSharp/
 ├─ Program.cs
 ├─ HelloCSharp.csproj
 ├─ bin/
 └─ obj/

File Program.cs cơ bản
Console.WriteLine("Hello C#");

🧠 PHẦN 3: CÚ PHÁP C# CƠ BẢN
1️⃣ Biến & kiểu dữ liệu
int a = 10;
double b = 3.14;
string name = "Dadas";
bool isOnline = true;

2️⃣ In / Nhập dữ liệu
Console.WriteLine("Nhập tên:");
string name = Console.ReadLine();
Console.WriteLine($"Xin chào {name}");

3️⃣ Điều kiện
if (a > 5)
{
    Console.WriteLine("Lớn hơn 5");
}
else
{
    Console.WriteLine("Nhỏ hơn hoặc bằng 5");
}

4️⃣ Vòng lặp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine(i);
}

while (a > 0)
{
    a--;
}

5️⃣ Hàm (Method)
static int Sum(int a, int b)
{
    return a + b;
}

6️⃣ Class & Object
class Player
{
    public string Name;
    public int Level;

    public void Info()
    {
        Console.WriteLine($"{Name} - Level {Level}");
    }
}

// Sử dụng
Player p = new Player();
p.Name = "Steve";
p.Level = 10;
p.Info();

7️⃣ List & Dictionary
List<int> numbers = new List<int> {1,2,3};

Dictionary<string, int> scores = new Dictionary<string, int>();
scores["A"] = 10;

⚙️ PHẦN 4: CÁC LỆNH dotnet QUAN TRỌNG
Lệnh	Chức năng
dotnet new console	Tạo app console
dotnet run	Chạy chương trình
dotnet build	Build
dotnet clean	Xóa file build
dotnet add package X	Cài thư viện
dotnet list package	Xem package
dotnet publish -c Release	Build bản release
🧩 PHẦN 5: CÀI THƯ VIỆN (NuGet)

Ví dụ cài Newtonsoft.Json:

dotnet add package Newtonsoft.Json


Sử dụng:

using Newtonsoft.Json;

🐞 PHẦN 6: DEBUG TRONG VS CODE

Đặt breakpoint (bấm vào lề trái)

Nhấn F5

VS Code tự tạo launch.json

🌐 PHẦN 7: CÁC LOẠI PROJECT C# PHỔ BIẾN
Mục đích	Lệnh
Console App	dotnet new console
Web API	dotnet new webapi
MVC Web	dotnet new mvc
Class Library	dotnet new classlib
Test	dotnet new xunit
📚 PHẦN 8: TÀI LIỆU (DOCS CHÍNH THỨC)

📘 C# Docs: https://learn.microsoft.com/dotnet/csharp/

📘 .NET CLI: https://learn.microsoft.com/dotnet/core/tools/

📘 NuGet: https://www.nuget.org/

📘 ASP.NET: https://learn.microsoft.com/aspnet/core/
