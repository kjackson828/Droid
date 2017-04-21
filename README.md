# Droid
codecademy project

/* Droid can be activated, charged, and hover above ground. */
public class Droid{
  private int batteryLevel;
	public Droid() {
    batteryLevel = 100;
  }
  public void activate() {
    System.out.println("Activated. How can I help you?");
    batteryLevel -= 5;
    System.out.println("Battery level is: " + batteryLevel + "percent.");
  }
  public void chargeBattery(int hours) {
    System.out.println("Droid charging...");
    batteryLevel += hours;
    if(batteryLevel > 100) {
      System.out.println("Battery level is: " + batteryLevel + "percent.");
    }
    else {
      System.out.println("Battery level is: " + batteryLevel + "percent.");
    }
  }
  public int checkBatteryLevel(){
   System.out.println(batteryLevel + "%");
   return batteryLevel;
  }
  public void hover(int feet) {
   if(feet > 2) {
     System.out.println("Error! I cannot hover above 2 feet.");
   }
   else {
     System.out.println("Hovering...");
     System.out.println(batteryLevel + "%");
     batteryLevel -= 20;
     System.out.println(batteryLevel + "%");
   }
 }
  public static void main(String[] args) {
  	Droid droid = new Droid();
  	droid.activate();
  	droid.chargeBattery(5);
  	droid.hover(2);
 }
}
