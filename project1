import java.util.*;
import java.time.*;
import java.time.format.DateTimeFormatter;
import java.time.ZonedDateTime;
import java.time.ZoneId;
public class project1{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        //LocalDateTime l is used to store the present time
        LocalDateTime l=LocalDateTime.now();
        //DateTimeFormatter dft to customise the time and date format
        DateTimeFormatter dft=DateTimeFormatter.ofPattern("dd/MMMM/yyyy hh 'hours' mm 'mins' ");
        System.out.println("The present Date and Time is: ");
        System.out.print(l.format(dft));
        System.out.println();
        System.out.println("To Show All Country Zone ids please enter YES else enter NO");
        String s=sc.nextLine();
        if(s.equals("YES"))
            Showids();
        ZoneId myid=ZoneId.systemDefault();
        String currId=myid.getId();
        ZonedDateTime myzdt=ZonedDateTime.of(l,ZoneId.of(currId));
        System.out.println("Enter the Country Zone id:");
        //id reads the Country zone 
        String id=sc.nextLine();
        //ZonedDateTime is used to convert the local time to entred country zone
        ZonedDateTime zdt=myzdt.withZoneSameInstant(ZoneId.of(id));
        System.out.println("The Converted local time zone to "+id+" :");
        System.out.println(zdt.format(dft));
    }
    static void Showids(){
        Set<String> zoneids=ZoneId.getAvailableZoneIds();
        for(String s:zoneids)
            System.out.print(s+" ");
        System.out.println();
    }
}
