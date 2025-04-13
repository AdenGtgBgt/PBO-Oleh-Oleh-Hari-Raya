using System;

namespace SistemManajemenKaryawan
{
    public class Karyawan
    {
        private string _namaKaryawan;
        private double _gajiPokok;
        private string _idKaryawan;
        private string _jenisKaryawan;

        public string GetJenisKaryawan()
        {
            return _jenisKaryawan;
        }

        public void SetJenisKaryawan(string jenis)
        {
            _jenisKaryawan = jenis;
        }

        public string NamaKaryawan
        {
            get { return _namaKaryawan; }
            set { _namaKaryawan = value; }
        }
        public double GajiPokok
        {
            get { return _gajiPokok; }
            set { _gajiPokok = value; }
        }
        public string IDKaryawan
        {
            get { return _idKaryawan; }
            set { _idKaryawan = value; }
        }
        public virtual void HitungGaji()
        {
            //disini saya kosongin krn menurut saya kurang efektif krn bakalan d override di smw class turunannya
            //eh ya gsi kak? tpi sy coba ga eror hehe
        }
    }


    public class Tetap : Karyawan
    {
        private double BonusTetap = 500000;

        public override void HitungGaji()
        {
            double GajiAkhir = GajiPokok + BonusTetap;
            Console.WriteLine($"Gaji Akhir  : Rp {GajiAkhir}");
        }
    }


    public class Kontrak : Karyawan
    {
        private double PotonganKontrak = 200000;

        public override void HitungGaji()
        {
            double GajiAkhir = GajiPokok - PotonganKontrak;
            Console.WriteLine($"Gaji Akhir  : Rp {GajiAkhir}");
        }
    }


    public class Magang : Karyawan
    {
        public override void HitungGaji()
        {
            double GajiAkhir = GajiPokok;
            Console.WriteLine($"Gaji Akhir  : Rp {GajiAkhir}");
        }
    }


    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Sistem Manajemen Perusahaan SEKAREP");

            Console.WriteLine("Jenis Karyawan :");
            Console.WriteLine("[1]. Karyawan Tetap");
            Console.WriteLine("[2]. Karyawan Kontrak");
            Console.WriteLine("[3]. Karyawan Magang");
            Console.Write("\nPilih [1/2/3] : ");
            int jenisKaryawan = int.Parse(Console.ReadLine());

            Console.Write("Nama Karyawan : ");
            string nama = Console.ReadLine();

            Console.Write("ID Karyawan   : ");
            string id = Console.ReadLine();

            Console.Write("Gaji Pokok    : ");
            double gajiPokok = double.Parse(Console.ReadLine());


            Karyawan karyawan;
            

            if (jenisKaryawan == 1)
            {
                karyawan = new Tetap();
                karyawan.SetJenisKaryawan("Karyawan tetap");
            }
            else if (jenisKaryawan == 2)
            {
                karyawan = new Kontrak();
                karyawan.SetJenisKaryawan("Karyawan Kontrak");
            }
            else if (jenisKaryawan == 3)
            {
                karyawan = new Magang();
                karyawan.SetJenisKaryawan("Karyawan Magang");
            }
            else
            {
                Console.WriteLine("Pilihan jenis karyawan tidak ditemukan.");
                return;
            }


            karyawan.NamaKaryawan = nama;
            karyawan.IDKaryawan = id;
            karyawan.GajiPokok = gajiPokok;

            Console.WriteLine("\n Detail Karyawan Perusahaan SEKAREP");
            Console.WriteLine($"Nama Karyawan   : {karyawan.NamaKaryawan}");
            Console.WriteLine($"Jenis Karyawan  : {karyawan.GetJenisKaryawan()}");
            Console.WriteLine($"ID Karyawan     : {karyawan.IDKaryawan}");
            Console.WriteLine($"Gaji Pokok      : Rp {karyawan.GajiPokok}");
            karyawan.HitungGaji();
        }
    }
}
