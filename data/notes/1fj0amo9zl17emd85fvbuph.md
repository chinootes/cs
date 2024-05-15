
|                             |                                                                               |
|-----------------------------|-------------------------------------------------------------------------------|
| 1. Import the package       | import java.sql.*                                                             |
| 2a. Load driver             | Steps to load and add connector jar                                           |
| 2b. Register driver         | Class.forName("com.mysql.jdbc.Driver");                                       |
| 3. Establish the connection | Connection con= DriverManager.getConnection("URL","Username","Password");     |
| 4. Create the statement     | Statement st = con.createStatement();                                         |
| 5. Execute the Query        | ResultSet rs = st.executeQuery(query); / int count = st.executeUpdate(query); |
| 6. Process Result           | rs.next(); String s = rs.getString(column number);                            |
| 7. Close                    | st.close();                                                                   |
|                             | con.close();                                                                  |


## Use PreparedStatement for user input

Use PreparedStatement instead of Statement to give user input in queries

query - (?,?) // question marks for parameters you want to take as user input in the query

```java
Prepared Statement st = con.prepareStatement(query); 
st.setInt(1, input1); 
st.setString(2, input2);
```
