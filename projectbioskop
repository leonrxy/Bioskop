import java.util.ArrayList;
import java.util.Scanner;
import java.io.IOException;
import java.util.Date;
import java.text.SimpleDateFormat;
import java.lang.String;
import java.util.Calendar;

public class projectbioskop {

    static Scanner data = new Scanner(System.in);
    static ArrayList<String> daftarFilm = new ArrayList<String>();
    static ArrayList<String> deskripsiFilm = new ArrayList<String>();
    static ArrayList<String> tiketBioskop = new ArrayList<String>();
    static String [] jamTayang = {"14.00","16.15","18.45","20.30"};
    static String [] jenisTiket = {"Reguler","Premium","Gold","Ultra"};
    static String [] hargaTiket = {"30.000","40.000","50.000","60.000"};
    static String [] metodePembayaran = {"Transfer Bank","Virtual Account","DANA","GoPay","LinkAja"};

    public static void main(String[] args)throws IOException, InterruptedException{
        boolean ulangmenu=true;
        while(ulangmenu){
            header();
            System.out.println(YELLOW + "DAFTAR MENU:");
            System.out.println("[1] Tambah Film Bioskop");
            System.out.println("[2] Hapus Film Bioskop");
            System.out.println("[3] Lihat Film Bioskop");
            System.out.println("[4] Lihat Detail Film");
            System.out.println("[5] Beli Tiket Bioskop");
            System.out.println("[6] Konfirmasi Pembayaran Tiket");
            System.out.println("[7] Lihat Daftar Tiket");
            System.out.println("[8] Lihat Detail Tiket");
            System.out.println("[9] Exit" + RESET);
            System.out.print("PILIH MENU> " );
            String pilihMenu = data.nextLine();
            switch(pilihMenu){
                case "1":
                    tambahFilmBioskop();
                    break;
                case "2":
                    hapusFilmBioskop();
                    break;
                case "3":
                    lihatFilmBioskop();
                    break;
                case "4":
                    lihatDetailFilm();
                    break;
                case "5":
                    dataTiket();
                    break;
                case "6":
                    konfirmasiBayar();
                    break;
                case "7":
                    lihatDaftarTiket();
                    break;
                case "8":
                    lihatDetailTiket();
                    break;
                case "9":
                    System.out.print(GREEN + "Terimakasih telah menggunakan program ini" + RESET);
                    System.exit(0);
                default:
                    System.out.println(RED + "Masukkan input dengan benar!" + RESET);
                    enter();
            }
        }
    }

    public static void header()throws IOException, InterruptedException{
        new ProcessBuilder("cmd", "/c", "cls").inheritIO().start().waitFor();
        System.out.println(GREEN + "=============================================================================");
        System.out.println("d8888b. d888888b  .d88b.  .d8888. db   dD  .d88b.  d8888b.   .d888b.    dD   ");
        System.out.println("88  `8D   `88'   .8P  Y8. 88'  YP 88 ,8P' .8P  Y8. 88  `8D   88   8D   d8'   ");
        System.out.println("88oooY'    88    88    88 `8bo.   88,8P   88    88 88oodD'   `VoooY'  d8'    ");
        System.out.println("88~~~b.    88    88    88   `Y8b. 88`8b   88    88 88~~~     .d~~~b. d8888b. ");
        System.out.println("88   8D   .88.   `8b  d8' db   8D 88 `88. `8b  d8' 88        88   8D 88' `8D ");
        System.out.println("Y8888P' Y888888P  `Y88P'  `8888Y' YP   YD  `Y88P'  88        `Y888P' `8888P  ");
        System.out.println("================================ leonrxy ====================================" + RESET);                                                                   
    }

    public static void enter(){
        System.out.print("Tekan enter untuk kembali ke menu");
        data.nextLine();
    }

    public static void filmKosong(){
        System.out.println(RED + "Daftar Film Kosong! Silakan menambah pada menu 'Tambah Film Bioskop'!" + RESET);
    }

    public static void tiketKosong(){
        System.out.println(RED + "Tiket masih kosong! silakan buat tiket terlebih dahulu." + RESET);
    }

    public static void tambahFilmBioskop(){
        String ulang;
        int size = daftarFilm.size();
        do{
        System.out.print("Masukkan Nama Film : ");
        String tambahFilm = data.nextLine();
        daftarFilm.add(tambahFilm);
        System.out.print("Masukkan Deskripsi Film : ");
        String tambahDeskripsi = data.nextLine();
        deskripsiFilm.add(tambahDeskripsi);
        if(daftarFilm.size()!=size){
            System.out.println(GREEN + "Menambah Daftar Film Berhasil!" + RESET);
        }
            else{
            System.out.println(RED +"Menambah Daftar Film Gagal!" + RESET);
            }
        System.out.print("Apakah ingin menambah film lagi? (y/n) ");
        ulang = data.nextLine();
        }
        while(ulang.contains("y") || ulang.contains("Y"));
        enter();
    }

    public static void hapusFilmBioskop(){
        if(daftarFilm.size()!=0){
        int size = daftarFilm.size();
        System.out.println(ORANGE +"======= HAPUS FILM BIOSKOP =======" + RESET);
        for(int i=0; i<daftarFilm.size();i++){
            System.out.println("["+(i+1)+"] "+daftarFilm.get(i));
        }
        System.out.print("Masukkan nomor yang ingin dihapus : ");
        int nomor = Integer.parseInt(data.nextLine());
        daftarFilm.remove((nomor-1));
        deskripsiFilm.remove((nomor-1));
        if(daftarFilm.size()!=size){
            System.out.println(GREEN + "Daftar Film Berhasil Dihapus!" + RESET);
        }
            else{
            System.out.println(RED +"Daftar Film Tidak Berhasil Dihapus!" + RESET);
            }
        }
            else{
                filmKosong();
            }
        enter();
    }

    public static void lihatFilmBioskop(){
        if(daftarFilm.size()!=0){
            System.out.println(ORANGE + "============= SEDANG TAYANG =============");
            for(int i=0; i<daftarFilm.size();i++){
            System.out.println("["+(i+1)+"] "+daftarFilm.get(i));
            }
            System.out.println("=========================================" + RESET);
        }
        else {
            filmKosong();
        }
        enter();
    }

    public static void lihatDetailFilm(){
        if(daftarFilm.size()!=0){
            System.out.println(ORANGE +"=============== DAFTAR FILM ===============");
            for(int i=0; i<daftarFilm.size();i++){
            System.out.println("["+(i+1)+"] "+daftarFilm.get(i));
            }
            System.out.println("===========================================" + RESET);
            System.out.print("PILIH FILM> ");
            int pilihFilm = Integer.parseInt(data.nextLine());
            System.out.println(CYAN + "============= DAFTAR FILM ["+ pilihFilm + "] =============");
            System.out.println("Judul Film     : " + daftarFilm.get((pilihFilm-1)));
            System.out.println("Deskripsi Film : " + deskripsiFilm.get((pilihFilm-1)));
            System.out.println("===========================================" + RESET);
        }
        else {
            filmKosong();
        }
        enter();
    }

    public static void dataTiket(){
        System.out.println(ORANGE + "======= BELI TIKET BIOSKOP =======" + RESET);
        System.out.print("Masukkan Nama Anda : ");
        String nama = data.nextLine();
        System.out.println(ORANGE + "----------------------------------");
        System.out.println(">> Pilih Jadwal Tayang");
        System.out.println("[1] "+ getTanggal(0));
        System.out.println("[2] "+ getTanggal(1));
        System.out.println("[3] "+ getTanggal(2));
        System.out.println("[4] "+ getTanggal(3));
        System.out.print(RESET + "PILIH Jadwal Tayang> ");
        int pilihTanggal = Integer.parseInt(data.nextLine());
        System.out.println(ORANGE + "----------------------------------");
        System.out.println(">> Pilih Film");
        for(int i=0; i<daftarFilm.size();i++){
            System.out.println("["+(i+1)+"] "+ daftarFilm.get(i));
        }
        System.out.print(RESET + "PILIH FILM> ");
        int pilihFilm = Integer.parseInt(data.nextLine());
        System.out.println(ORANGE + "----------------------------------");
        System.out.println(">> Pilih Jam Tayang");
        System.out.println("[1] 14.00");
        System.out.println("[2] 16.15");
        System.out.println("[3] 18.45");
        System.out.println("[4] 20.30");
        System.out.print(RESET + "PILIH JAM TAYANG> ");
        int pilihJamTayang = Integer.parseInt(data.nextLine());
        System.out.println(ORANGE + "----------------------------------");
        System.out.println(">> Pilih Jenis Tiket");
        System.out.println("[1] Reguler");
        System.out.println("[2] Premium");
        System.out.println("[3] Gold");
        System.out.println("[4] Ultra");
        System.out.print(RESET + "PILIH JENIS TIKET> ");
        int pilihJenisTiket = Integer.parseInt(data.nextLine());
        System.out.println(ORANGE + "----------------------------------");
        System.out.println(">> Pilih Metode Pembayaran");
        System.out.println("[1] Transfer Bank");
        System.out.println("[2] Virtual Account");
        System.out.println("[3] Dana");
        System.out.println("[4] GoPay");
        System.out.println("[5] LinkAja");
        System.out.print(RESET + "PILIH JENIS TIKET> ");
        int pilihPembayaran = Integer.parseInt(data.nextLine());
        beliTiketBioskop(nama, pilihTanggal, pilihFilm, pilihJamTayang, pilihJenisTiket, pilihPembayaran);
    }

    public static void beliTiketBioskop(String nama, int pilihTanggal, int pilihFilm, int pilihJamTayang, int pilihJenisTiket, int pilihPembayaran){
        String tanggal = getTanggal((pilihTanggal-1));
        String film=daftarFilm.get((pilihFilm-1));
        String jam=jamTayang[(pilihJamTayang-1)];
        String jenis=jenisTiket[(pilihJenisTiket-1)];
        String pembayaran = metodePembayaran[(pilihPembayaran-1)];
        int ctiket=tiketBioskop.size()+1;
        String tiket=String.valueOf(ctiket);
        String noTiket= membuatKodeTiket(tiket);
        String totalBayar = hargaTiket[(pilihJenisTiket-1)];
        String statusBayar = "Pending";
        String IDtiket = noTiket + " ; " + nama + " ; " + film + " ; " + tanggal + " ; " + jam + " ; " + jenis + " ; " + pembayaran + " ; " + totalBayar + " ; " + statusBayar;
        tiketBioskop.add(IDtiket);
        System.out.println(GREEN + "=========== DATA TIKET ===========");
        System.out.println("No Tiket          : " + noTiket);
        System.out.println("Nama              : " + nama);
        System.out.println("Film              : " + film);
        System.out.println("Hari, Tanggal     : " + tanggal );
        System.out.println("Jam Tayang        : " + jam + " WIB");
        System.out.println("Jenis Tiket       : " + jenis);
        System.out.println("Metode Pembayaran : " + pembayaran);
        System.out.println("==================================");
        System.out.println("Total Harga       : Rp." + totalBayar);
        System.out.println("Status            : " + RED + statusBayar);
        System.out.println(GREEN + "==================================");
        System.out.println("Tiket telah berhasil dibuat!");
        System.out.println("----------------------------------" + RESET);
        enter();
    }
    public static String getTanggal(int hari){
        Date tanggal = new Date();
        SimpleDateFormat fh = new SimpleDateFormat("EEEE", new java.util.Locale("id"));
        SimpleDateFormat ft = new SimpleDateFormat("dd", new java.util.Locale("id"));
        SimpleDateFormat fb = new SimpleDateFormat("MMMM", new java.util.Locale("id"));
        SimpleDateFormat fth = new SimpleDateFormat("yyyy");
        int h = Integer.parseInt(ft.format(tanggal))+hari;
        Calendar cal = Calendar.getInstance();
        cal.add(Calendar.DATE, hari);
        Date h1 = cal.getTime();
        String tgl= fh.format(h1) + ", " + h + " " + fb.format(tanggal) + " " + fth.format(tanggal);
        return tgl;
    }

    public static void konfirmasiBayar(){
        if(tiketBioskop.size()!=0){
            System.out.println(ORANGE + "======== DAFTAR TIKET ========");
            for(int i=0; i<tiketBioskop.size();i++){
                System.out.println("["+(i+1)+"] "+tiketBioskop.get(i));
                }
            }
            else{
                tiketKosong();
                }
        System.out.print(RESET + "PILIH NO TIKET> ");
        int noTiket = Integer.parseInt(data.nextLine());
        tampilTiket(noTiket);
        String tiket = (String)tiketBioskop.get((noTiket-1));
        String [] detailTiket = tiket.split(" ; ");
        System.out.print("Apakah Kamu Ingin Mengkonfirmasi Pembayaran Tiket Tersebut? (y/n) ");
        String konfirmasi = data.nextLine();
        if (konfirmasi.contains("y") || konfirmasi.contains("Y")){
            String statusBayar = "Sudah Bayar";
            tiketBioskop.set((noTiket-1), detailTiket[0] + " ; " + detailTiket[1] + " ; " + detailTiket[2] + " ; " + detailTiket[3] + " ; " + detailTiket[4] + " ; " + detailTiket[5] + " ; " + detailTiket[6]  + " ; " + detailTiket[7]  + " ; " + statusBayar );
            System.out.println(GREEN + "Pembayaran Tiket No." + detailTiket[0] + " Berhasil Dikonfirmasi" + RESET);
        }
            else{
                System.out.println(RED + "Pembayaran Tiket No." + detailTiket[0] + " Gagal Dikonfirmasi" + RESET);
            }
        enter();
    }

    public static void lihatDaftarTiket(){
        if(tiketBioskop.size()!=0){
        System.out.println(ORANGE + "============ DAFTAR TIKET ============");
        for(int i=0; i<tiketBioskop.size();i++){
            System.out.println("["+(i+1)+"] "+tiketBioskop.get(i));
        }
        System.out.println("=====================================" + RESET);
        }
            else{
                tiketKosong();
            }
        enter();
    }

    public static void lihatDetailTiket(){
        if(tiketBioskop.size()!=0){
        System.out.println(ORANGE + "======== LIHAT DETAIL TIKET ========");
        for(int i=0; i<tiketBioskop.size();i++){
        System.out.println("["+(i+1)+"] "+tiketBioskop.get(i));
        }
        System.out.print(RESET + "PILIH NO TIKET> ");
        int pilihTiket = Integer.parseInt(data.nextLine());
        tampilTiket(pilihTiket);
        enter();
        }
            else {
                tiketKosong();
                enter();
            }
    }

    public static void tampilTiket(int pilihTiket){
        String tiket = (String)tiketBioskop.get((pilihTiket-1));
        String [] detailTiket = tiket.split(" ; ");
        System.out.println(LBLUE + "--------- DETAIL TIKET [" + (pilihTiket) + "] ---------");
        System.out.println("No Tiket            : " + detailTiket[0]);
        System.out.println("Nama                : " + detailTiket[1]);
        System.out.println("Film                : " + detailTiket[2]);
        System.out.println("Hari, Tanggal       : " + detailTiket[3]);
        System.out.println("Jam Tayang          : " + detailTiket[4]);
        System.out.println("Jenis Tiket         : " + detailTiket[5]);
        System.out.println("Metode Pembayaran   : " + detailTiket[6]);
        System.out.println("Harga               : " + detailTiket[7]);
        System.out.print("Status Bayar        : ");
        if (detailTiket[8].contains("Sudah Bayar")){
            System.out.println(GREEN + detailTiket[8]);
        }
            else {
                System.out.println(RED + detailTiket[8]);
            }
        System.out.println(LBLUE + "------------------------------------" + RESET);
    }

    public static String membuatKodeTiket(String noTiket){
        if(noTiket.length()==1){
            noTiket="00000" + noTiket;
        }
            else if(noTiket.length()==2){
                noTiket="0000" + noTiket;
            }
                else if(noTiket.length()==3){
                    noTiket="000" + noTiket;
                }
                    else if(noTiket.length()==4){
                        noTiket="00" + noTiket;
                    }
                        else if(noTiket.length()==5){
                        noTiket="0" + noTiket;
                        }
        return noTiket;
    }

    //Warna Teks
    static String RESET = "\033[0;97m";
    static String GREEN = "\033[1;92m";
    static String YELLOW = "\033[1;33m";
    static String RED = "\033[1;91m";
    static String ORANGE = "\033[38;2;225;153;0m";
    static String CYAN = "\033[1;96m";
    static String LBLUE = "\033[38;2;120;172;255m";
}
