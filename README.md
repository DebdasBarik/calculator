# calculator
import java.awt.*;
import javax.swing.*;
import java.awt.event.*;

class cal extends JFrame implements ActionListener
{ JTextField b1,b2,b3;
JLabel lb1,lb2;
JButton btn,btn1,btn2,btn3;
Container c;

	cal()
	{ 
	c=this.getContentPane();
	b1=new JTextField();
	b1.setBounds(120,20,100,50);
	b2=new JTextField();
	b2.setBounds(120,70,100,50);
	b3=new JTextField();
	b3.setBounds(10,100,250,250);
	btn=new JButton("+");
	btn1=new JButton("-");
	btn2=new JButton("*");
	btn3=new JButton("/");
lb1=new JLabel("INPUT NUMBER1");
lb2=new JLabel("INPUT NUMBER2");
lb1.setBounds(10,20,100,50);
lb2.setBounds(10,70,100,50);

Font fn=new Font("Aerial",Font.BOLD,15);
btn.setBounds(10,150,70,40);
btn1.setBounds(100,150,70,40);
btn2.setBounds(200,150,70,40);
btn3.setBounds(300,150,70,40);
btn.setFont(fn);
btn1.setFont(fn);
btn2.setFont(fn);
btn3.setFont(fn);

c.add(b1);
c.add(b2);
c.add(lb1);
c.add(lb2);
c.add(btn);
c.add(btn1);
c.add(btn2);
c.add(btn3);
c.add(b3);
c.setBackground(Color.green);
	btn.addActionListener(this);
	btn1.addActionListener(this);
	btn2.addActionListener(this);
	btn3.addActionListener(this);
	
}
public void actionPerformed(ActionEvent e)
{String s1=b1.getText();
String s2=b2.getText();
float i=Float.parseFloat(s1);
float j=Float.parseFloat(s2);
	if(e.getSource()==btn)
	{
       float k=i+j;
        String s3=Float.toString(k);
	     b3.setText(s3);	
	}
	else if (e.getSource()==btn1)
	{
		float l=i-j;
		String s4=Float.toString(l);
		b3.setText(s4);
	}	
else if (e.getSource()==btn2)
	{
		float m=i*j;
		String s5=Float.toString(m);
		b3.setText(s5);
	}
else if (e.getSource()==btn3)
	{
		float n=i/j;
		String s5=Float.toString(n);
		b3.setText(s5);
	}		
}

}

public class calculator
{
 public static void main(String arg[])
 {
  cal s=new cal();
  s.setTitle("CALCULATOR");
  s.setVisible(true);
  s.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
  s.setBounds(100,100,700,600);
 }
}
