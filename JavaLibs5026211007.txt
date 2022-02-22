import javax.swing.JOptionPane;
class JavaLibs5026211007 {
  public static void main(String[] args) {
    int intmoney;
    double double1;
    String money = "";
    String[] options = { "Yes", "No" };
    int introInt = JOptionPane.showOptionDialog(null, "Welcome to my quest game!, do you want to play the game?", "Hello, User!", 0, 1, null, (Object[])options, options[0]);
    if (introInt != 0) {
      JOptionPane.showMessageDialog(null, "Well, see you later!", "Too bad!", 1);
      System.exit(0);
    } 
    String name = (String)JOptionPane.showInputDialog(null, "What is your adventurer name?", "First question", 3, null, null, "String");
    String weapon = (String)JOptionPane.showInputDialog(null, "Your weapon is_________.", "Second question", 3, null, null, "String");
    String companion = (String)JOptionPane.showInputDialog(null, "Your companion in this quest is______.", "Third question", 3, null, null, "String");
    String pet = (String)JOptionPane.showInputDialog(null, "Name your pet animal to join your adventure!.", "Fourth question", 3, null, null, "String");
    String compad = (String)JOptionPane.showInputDialog(null, "What is  the best word to describe " + companion + "\'s appearance?", "Fifth question", 3, null, null, "String");
    String spell = (String)JOptionPane.showInputDialog(null, "Name a magic spell.", "Sixth question", 3, null, null, "String");
    while (true) {
      try {
        money = (String)JOptionPane.showInputDialog(null, "How much would you spend on your gears?", "Seventh question", 3, null, null, "int");
        intmoney = Integer.parseInt(money);
        break;
      } catch (Exception e) {
        if (money != null) 
        JOptionPane.showMessageDialog(null, "That is not an integer.", "Error", 1);
      } 
    } 
    while (true) {
      try {
        String decimalroll = (String)JOptionPane.showInputDialog(null, "roll between 0 to 1, in decimals!", "Eighth question", 3, null, null, "double");
        double1 = Double.parseDouble(decimalroll);
        break;
      } catch (Exception e) {
        JOptionPane.showMessageDialog(null, "A double is a number with decimal precision such as 1.0, 0.4323, or -3.14.", "What is a double?", 1);
      } 
    } 
    String degree = (String)JOptionPane.showInputDialog(null, "What is your degree in your institution of adventurers?", "Nineth question", 3, null, null, "String");
    String enemy = (String)JOptionPane.showInputDialog(null, "What do you think you will face in your adventure?", "Final question", 3, null, null, "String");
    JOptionPane.showMessageDialog(null, "Alright, " + name + ".  Lets go to your adventure!", "Start point", 1);
    JOptionPane.showMessageDialog(null, "And so, here are the stories of how " + name + " went to the dungeon!", "Results!", 2);
    String story = "When " + name + " entered the dungeon, " + name + " faced an enemy called " + enemy + ", but then "+ name + " defeated the monster\n with his mighty " + weapon + ". " + name + " looked at his companion, " + companion + ", and asked if " + companion + " was okay. " + "they continued their journey\n until " + pet + ", founded a big treasure, in which contain " + (double1 * (intmoney) / 4 ) + " gold!  " + name + " said that the gold was only " + ((double1 * (intmoney) / 4 )  / (intmoney) * 100.0D) + "% from " + name + "\'s " + intmoney + " gold.\n" + "\n" + "They exited the dungeon, and " + name + " said that " + companion + " was " + compad + ", and that\n" + name + " was really admired about it. " + companion + " was surprised by that, and cast a spell of " + spell + " which makes " + name + " ran away... \n";
    JOptionPane.showMessageDialog(null, story, "The Story", 1);
    JOptionPane.showMessageDialog(null, "And thats the story, " + name + ". Oh yeah by the way, how is your study in " + degree + " is going?, well, good luck then!", "The Story", 1);
  }
}
	