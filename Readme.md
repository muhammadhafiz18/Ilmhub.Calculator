# New Calculator
### Ushbu loyiha kalkulyator kabi __amallarni bajarish__ uchuun mo'ljallangan va C# dasturlash tili yordamida yozilgan.

## Loyiha tarkibi:
### 1. Servislar (Services)
### 2. Interfeyslar (Interfaces)
### 3. Models
### 4. Program.cs
### va boshqa biz kod yozmaydigan fayllar

## __Services:__
#### 1. __DisplayService__ - bu service kodogi matnlarning chiqishi va kirishi uchun javob beradi va tarixini chiqarish, biror bir matn chiqarib o'zgaruvchini qabul qilish va shunchaki matn chiqarish vazifalarini methodlar asosida bajaradi.
#### 2. __CalculateService__ - bu service esa kiritilgan amallarni bajarish vazifasini bajaradi va shu bilan u siz ifoda yoki boshqa narsa kiritganingizni aniqlaydi va ifoda kiritgininguzcha uni so'raydi.
#### 3. __HistoryService__ - bu service o'z nomi bilan tarixga javob beradi va tarixni chiqarib berish, uni saqlash, o'chirish va dasturga qayta kirganda ham saqlanib qolishi uchun metodlarni o'z ichiga oladi.

## __Interfaces:__
#### 1. __IDisplayService__ - bu interface DisplayService ning tarkibi uchun javob beradi va void Print(string message), string ReadInput(string message),string ReadInput(), void PrintHistory(List<HistoryItem> history) larni o'z ichiga olishini belgilaydi.
#### 2. __ICalculateService__ - bu interface CalculateService ning tarkibi uchun javob beradi va huddi IDisplayService kabi ichidagi bor methodlari va method signature kabilarni belgilaydi.Ya'ni void Calculate(List<HistoryItem> history) ning bo'lishini.
#### 3. __IHistoryService__ - bu interface HistoryService ning tarkibi uchun javob beradi va huddi IDisplayService kabi ichidagi bor methodlari va method signature kabilarni belgilaydi. Ya'ni void ShowHistory(List<HistoryItem> history), void ClearHistory(List<HistoryItem> history), void LoadHistory(string path, List<HistoryItem> history), void SaveHistory(List<HistoryItem> history, string path) larning mavjudligini va boshqa narsalarning bo'lmasligini belgilaydi.

## __Models:__
#### 1. HistoryItem - bu model tarkibida HistoryItem deb nomlangan class bo'lib u history (tarix)ni saqlashda yordam beradigan, loyihada string kabi type deb olingan. Bu yerda esa uning ichida nimalar bo'lishi ya'ni hisoryda nimalar saqlanishi bor.

## __Program.cs:__
#### bu fayl loyihaning boshqaruv qismi deb olinishi mumkin chunki bu yerda boshqa asosiy kodlar yozilgan fayllar tarkibidan shablon sifatida foydalanilgan ya'ni ular asosida loyiha yaratilgan.Masalan, Loyihaning boshida chiquvchi gaplarni DisplayService dagi Print methodi orqali chiqarilishi va hokazolar.

## __Boshqa fayllar__
#### bunda sln, csproj kabi biz kod yozmaydigan fayllar azarda tutilgan.