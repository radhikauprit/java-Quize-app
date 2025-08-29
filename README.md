# java-Quize-app
java quize app with using java swing for graphical user interface(GUI)
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;


public class login extends JFrame implements ActionListener{
  JButton rules,back;
  JTextField tname;
    login() {
        // Frame basics
        setTitle("Simple Minds Login");
        setSize(1200, 500);
        setLocation(100, 200);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // Use no layout for absolute positioning
        setLayout(null);

        // Set background white for the content pane
        getContentPane().setBackground(Color.white);

        // Insert image as background JLabel
        ImageIcon i = new ImageIcon("image/quize.jpg");
        JLabel imageLabel = new JLabel(i);
        imageLabel.setBounds(0, 0, 600, 500);
        add(imageLabel);

        // Add heading label
        JLabel heading = new JLabel("Simple Minds:");
        heading.setBounds(750, 60, 400, 45);
        heading.setFont(new Font("Viner Hand ITC", Font.BOLD, 40));
        heading.setForeground(new Color(14, 57, 55));
        add(heading);

        // Add name label
        JLabel name = new JLabel("Enter Your Name:");
        name.setBounds(750, 150, 400, 40);  // Adjust height to match font size visually
        name.setFont(new Font("Viner Hand ITC", Font.BOLD, 40));
        name.setForeground(new Color(14, 57, 55));
        add(name);

        // Add text field for name
         tname = new JTextField();
        tname.setBounds(750, 200, 300, 35);  // Aligned below the name label with proper height
        tname.setFont(new Font("Times New Roman", Font.BOLD, 20));
        tname.setForeground(new Color(18, 17, 18));
        add(tname);

         rules=new JButton("Rules");
        rules.setBounds(745,270,120,25);
        rules.setBackground(new Color(90,14,254));
        rules.setForeground(Color.WHITE) ;
        rules.addActionListener(this);

         back=new JButton("Back");
        back.setBounds(940,270,120,25);
        back.setBackground(new Color(90,14,254));
        back.setForeground(Color.WHITE) ;
        back.addActionListener(this);
        add(back);
          
        add(rules);

        // Make frame visible last
        setVisible(true);

 }
 

    public static void main(String[] args) {
       new login();       
    }


    @Override
    public void actionPerformed(ActionEvent e) {
      // TODO Auto-generated method stub
      if(e.getSource()==rules){
        setVisible(false);
        String name=tname.getText();
        new rules(name);

      }else if(e.getSource()==back){
      setVisible(false);
      }
    }
    
}
