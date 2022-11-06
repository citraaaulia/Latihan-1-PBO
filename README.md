# Latihan-1-PBO
//Pegawai
public class Pegawai {
    private String name;
    private String address;
    private int number;
    public Pegawai (String name, String address, int number){
        System.out.println("Menyusun Pegawai");
        this.name = name;
        this.address = address;
        this.number = number;
    }
    public void mailCheck(){
        System.out.println("Memeriksa Surat Untuk" + this.name+ " " + this.address);
    }
    public String toString(){
        return name + " " + address + " " + number;
    }
    public String getName(){
        return name;
    }
    public String getAddress(){
        return address;
    }
    public void setAddress(String newAddress){
        address = newAddress;
    }
    public int getNumber(){
        return number;
    }
}

Nilai x = 5
ini class Child

//Salary
public class Gaji extends Pegawai
{
    private double salary;
    public Gaji(String name, String address, int number, double salary){
        super(name, address, number);
        setSalary(salary);
    }
    public void mailCheck(){
        System.out.println("Memeriksa kelas gaji dalam surat ");
        System.out.println("Surat tertuju untuk " +getName()+ " dengan gaji" + salary);
    }
    public double getSalary(){
        return salary;
    }
    public void setSalary(double newSalary){
        if(newSalary >=0.0){
            salary = newSalary;
        }
    }
    public double computerPay(){
        System.out.println("Menghitung pembayaran gaji untuk " + getName());
        return salary/52;
    }
}

//Virtual Demo
public class VirtualDemo {
    public static void main(String[]args){
        Gaji s= new Gaji("Wahyu", "KUBAR", 3, 5000.00);
        Pegawai e= new Gaji("Ini nama", "Samarinda", 2, 2500.00);
        System.out.println("Memanggil mailCheck Berdasarkan Referensi Gaji--");
        s.mailCheck();
        System.out.println("\nMemanggil mailCheck Berdasarkan Referensi Pegawai--");
        e.mailCheck();
    }
    
}
//Hasil Akhir
Menyusun Pegawai
Menyusun Pegawai
Memanggil mailCheck Berdasarkan Referensi Gaji--
Memeriksa kelas gaji dalam surat 
Surat tertuju untuk Wahyu dengan gaji5000.0

Memanggil mailCheck Berdasarkan Referensi Pegawai--
Memeriksa kelas gaji dalam surat
Surat tertuju untuk Ini nama dengan gaji2500.0
