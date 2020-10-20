# The Cashier

Aplikasi ini berisi tentang menghitung harga total dari barang yang ingin
dibeli.

# Scope & Functionalities
- User dapat memasukkan nama item
- User dapat memilih tipe nya
- User dapat memasukkan jumlah data
- User dapat memasukkan harga  

# How does it works?

Diawali dari method `MainWindow` pada class MainWindow.xaml.cs
```csharp
       public MainWindow()
        {
            InitializeComponent();
            calculator = new Calculator();
            listBox.ItemsSource = calculator.getListItem();
        }
```

logika perhitungan terdapat pada `Item.cs` sebagai berikut caranya
```csharp
       public double getSubTotal()
        {
            subtotal = price * quantity;
            return subtotal;
        }
``` 

Jadi, pertama kita menginput nama item, kemudian memilih barang atau jasa. Jika sudah menginput jumlah barang dan berapa harganya 
dengan logika perhitungan `subtotal = price * quantity;` dan hasilnya akan muncul di dalam listbox dan total harganya.