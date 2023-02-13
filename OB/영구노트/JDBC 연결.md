
### #오라클 #jdbc #mysql 
---



>오라클

driver = oracle.jdbc.OracleDriver
url = jdbc:oracle:thin:@localhost:1521:xe
user = SCOTT
pw = tiger


> mysql

	String driver = "com.mysql.cj.jdbc.Driver";
	String url = "jdbc:mysql://localhost:3306/testdb";
	String id = "root";
	String pw = "mysql";



==드라이버 로드==
	public UsersDAO() throws SQLException {

		
		try {
			Class.forName(driver);
		
			
		} catch (ClassNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		
		
	}

==셀렉문==

	public ArrayList<UsersDTO> select(){
		
		ArrayList<UsersDTO> list = new ArrayList<UsersDTO>();
		
		Connection conn = null;
		Statement stmt = null;
		ResultSet rs = null;
		
		try {
			conn = DriverManager.getConnection(url, id, pw);
			stmt = conn.createStatement();
			String sql = "SELECT * FROM student";
			rs = stmt.executeQuery(sql);
			
			while(rs.next()) {
				int id = rs.getInt("id");
				String userName = rs.getString("userName");
				String userAge = rs.getString("userAge");
				
				list.add(new UsersDTO(id, userName, userAge));
			}
			
		
			
		} catch (SQLException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} finally {
			try {
				if(rs != null) rs.close();
				if(stmt != null) stmt.close();
				if(conn != null) conn.close();
			} catch (Exception e2) {
				// TODO: handle exception
			}
		}

		

		
		return null;
		

		
		
	}



### 영상기억 :  ==드라이버오라클돌고래 

셀렉트 인설트 업데이트 문 만들어보기!  #공부할것




### 연결문서 : 

[[SQL CRUD]]





















