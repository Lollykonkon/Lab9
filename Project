import java.util.Scanner;
import java.util.ArrayList;
class rabotnik{
    String name;
    String otdel;
    rabotnik(String name, String otdel){
        this.name= name;
        this.otdel =otdel;
    } @Override
    public String toString() {
        return "rabotnik{" +
                "ФИО='" + name + '\'' +
                ", Отдел='" + otdel + '\'' +
                '}';
    }
}
class hourWorker extends rabotnik{
    hourWorker(String name, String otdel) {
        super(name, otdel);
    } @Override
    public String toString() {
        return "Почасовой работник{" +
                "ФИО='" + name + '\'' +
                ", Отдел='" + otdel + '\'' +
                '}';
    }
}
class salaryWorker extends rabotnik{
    salaryWorker(String name, String otdel) {
        super(name, otdel);
    } @Override
    public String toString() {
        return "На окладе {" +
                "ФИО='" + name + '\'' +
                ", Отдел='" + otdel + '\'' +
                '}';
    }
}
class Package{
    private ArrayList<rabotnik> masRab =new ArrayList<rabotnik>();
    public void addFile(rabotnik m){
        masRab.add(m);
    }
    public void printWorkers() {
        System.out.println("В предприятии: ");
        for (rabotnik a : masRab) {
            System.out.println("\t" + a.toString());
        }
    }
    public void numberOfHourWorkers(){
        int colHour=0;
        for (rabotnik a : masRab) {
            if (a instanceof hourWorker) {
                colHour+=1;
            }
        }
        System.out.println("Количество почасовых работников "+ colHour);
    }
    public void numberOfSalaryWorkers(){
        int colSalary=0;
        for (rabotnik a : masRab) {
            if (a instanceof salaryWorker) {
                colSalary+=1;
            }
        }
        System.out.println("Количество работников на окладе "+ colSalary);
    }
}
public class Worker {
    //Вариант 2
    public static void main(String[] args) {
        Package HR = new Package();
        Scanner sc = new Scanner(System.in);
        System.out.println("\t" +"Введите количество почасовых работников");
        int colhour= sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < colhour; i++) {
            System.out.println("Введите ФИО почасового работника ");
            String name = sc.nextLine();
            System.out.println("Введите его отдел работы");
            String otdel = sc.nextLine();
            hourWorker hour1 = new hourWorker(name,otdel);
            HR.addFile(hour1);
        }
        System.out.println("Введите количество работников на окладе");
        int colsalary= sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < colsalary; i++) {
            System.out.println("Введите ФИО работника на окладе");
            String name = sc.nextLine();
            System.out.println("Введите его отдел работы");
            String otdel = sc.nextLine();
            salaryWorker salary1 = new salaryWorker(name,otdel);
            HR.addFile(salary1);
        }
        HR.printWorkers();
        HR.numberOfHourWorkers();
        HR.numberOfSalaryWorkers();
    }
}
