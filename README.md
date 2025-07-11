This is a Java-based Hotel Management System that allows users to book rooms, order food, check room availability, and manage customer checkouts. The application supports both single and double rooms with luxury and deluxe options. Data persistence is handled using Java Serialization.

🔧 Features
📋 Room Types:

Luxury Double Room

Deluxe Double Room

Luxury Single Room

Deluxe Single Room

🛏️ Room Management:

Book rooms with customer details

Check availability of specific room types

View room features and pricing

🍽️ Food Ordering:

Menu: Sandwich, Pasta, Noodles, Coke

Itemized billing based on food orders

💵 Billing & Checkout:

Automatic generation of bills

Includes room rent and food charges

Room deallocation upon checkout

💾 Data Persistence:

Customer data and room occupancy are saved using object serialization (backup file)

Data is restored on program restart
HotelManagementSystem/
│
├── Main.java                # Main entry point of the application
├── Food.java                # Handles food items and pricing
├── Singleroom.java          # Defines Single room with basic customer info
├── Doubleroom.java          # Extends Singleroom for two-person occupancy
├── NotAvailable.java        # Custom exception for room unavailability
├── holder.java              # Stores arrays of room objects
├── Hotel.java               # Core class managing room booking, billing, etc.
├── write.java               # Handles writing backup data in a separate thread
├── backup                   # Serialized data file (created after first run)
└── hotel-management.jar     # Compiled JAR file to run the program
How to Run
Requirements
Java Development Kit (JDK 8 or later)

Command line or terminal

Steps
Compile and Create JAR (if not done already)
If you've already created a JAR file, skip to step 2.
Otherwise, compile and package your files:

bash
Copy
Edit
javac Main.java
jar cf hotel-management.jar *.class
Run the JAR File

bash
Copy
Edit
java -jar hotel-management.jar
Follow On-Screen Menu

You’ll be prompted with options to view rooms, book, order food, and checkout.

📋 Menu Options
markdown
Copy
Edit
1. Display room details
2. Display room availability
3. Book
4. Order food
5. Checkout
6. Exit
🧠 Technical Highlights
Uses object serialization (ObjectInputStream/ObjectOutputStream) to persist room booking data.

Implements multithreading to save backup data in the background.

Custom exception NotAvailable alerts the user if a room is already booked.

Flexible data structure using arrays of room objects.

❗ Important Notes
Ensure backup file is present for loading previous session data.

Room numbers:

1–10: Luxury Double

11–30: Deluxe Double

31–40: Luxury Single

41–60: Deluxe Single

Do not delete the backup file unless you want to reset all data.

📌 Author
Developed by: Swarna Sikha

Language: Java

Persistence: File-based Serialization
