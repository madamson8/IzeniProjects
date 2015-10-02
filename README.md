package snake;

import java.awt.*;

import javax.swing.*;

import java.util.*;

// Top Level Window
public class TopLevelWindow extends snake{
	
	static Scanner userInput = new Scanner(System.in);
	static int x = 10;
	static int y = 10;
	
	private static void createWindow() {
		// Make the window
		JFrame window = new JFrame("Izeni Snake");
		window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		JLabel startText = new JLabel("Please enter some dimensions somewhere between 300 - 400.",SwingConstants.CENTER);  // String Object?
		startText.setPreferredSize(new Dimension(300, 100));  // Setting size of Text?
		window.getContentPane().add(startText, BorderLayout.CENTER); // Adding to window
		
		// This displays the window
		window.setLocationRelativeTo(null);
		window.setSize(300, 300); // .pack() auto sets it .setSize allows entry
		// IMPORTANT:: if you make setSize() userInput it will not work.
		window.setResizable(true);
		window.setVisible(true);
		
	}
	
	public void printAndReplaceArray() {
		for(int x = 0; x < 20; x++) {
			for(y = 0; y < 20; y++) {
				if(gameboard[x][y] == 1) {
					PrintArray(gameboard);
					
				}
			}
		}
	}
	
	public static void main(String[] args){ 
		createWindow();  // Will create a new window on entry
	}
	
}
