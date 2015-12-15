<?php
	
/**
 *  Üye Ol
 */
class users  {
	public $user_id = 0;
	public $user_group_id = 0;
	public $ref_id = 0;
	public $county_id = 0;
	public $city_id = 0;
	public $town_id = 0;
	public $district_id = 0;
	public $user_name = 0;
	public $user_email = 0; 
	public $user_password = null;
	public $user_password2 = null;
	public $user_sex = null;
	public $user_birth_date = null;
	public $user_phone1 = null;
	public $user_phone1_internal = null;
	public $user_phone2 = null;
	public $user_address = null;
	public $user_first_name = null;
	public $user_last_name = null;
	public $user_reg_date = null;
	public $user_last_login_time = null;
	public $user_last_login_ip = null;
	public $user_activation = 1; // Burada direk olarak user aktif duruma alınıyor. Dikkat !
	public $user_registeration_ref = null;
		
	function add () {
		
	 $action = mysql_query("INSERT INTO users VALUES('',
	 												 '{$this->user_group_id}',
	 												 '{$this->ref_id}',
	 												 '{$this->county_id}',
	 												 '{$this->city_id}',
	 												 '{$this->town_id}',
	 												 '{$this->district_id}',
	 												 '{$this->user_name}',
	 												 '{$this->user_email}',
	 												 '{$this->user_password}',
	 												 '{$this->user_password2}',
	 												 '{$this->user_sex}',
	 												 '{$this->user_birth_date}',
	 												 '{$this->user_phone1}',
	 												 '{$this->user_phone1_internal}',
	 												 '{$this->user_phone2}',
	 												 '{$this->user_address}',
	 												 '{$this->user_first_name}',
	 												 '{$this->user_last_name}',
	 												 '{$this->user_reg_date}',
	 												 '{$this->user_last_login_time}',
	 												 '{$this->user_last_login_ip}',
	 												 '{$this->user_activation}',
	 												 '{$this->user_registeration_ref}'
	 			
	 			)");
	 
	 	echo mysql_error();
		 if($action){
		 		$this->user_id = mysql_insert_id();
		 }else{
		 	// Hata için birşeyler..
		 }
		 			
	} // Add Finish
	
	function login() {
		$count = mysql_num_rows(mysql_query("SELECT * FROM users WHERE user_email='".$this->user_email."' AND user_password='".$this->user_password."'" ));
		
		if($count > 0){
			$user = mysql_fetch_array( mysql_query("SELECT * FROM users WHERE user_email='".$this->user_email."' AND user_password='".$this->user_password."'"));
			$this->user_id = $user[user_id];		
		}else{
			$this->user_id ='';
		}
		
	} // Login Finish
	
	function edit() {
		$action = mysql_query("UPDATE users SET user_first_name = '".$this->user_first_name."',
												user_last_name = '".$this->user_last_name."',
												user_birth_date ='".$this->user_birth_date."',
												user_sex = '".$this->user_sex."',
												user_phone1 = '".$this->user_phone1."',
												user_phone2 = '".$this->user_phone2."',
												user_password = '".$this->user_password."',
												user_password2 = '".$this->user_password2."'
												
												
							   WHERE user_id =".$_SESSION[user_id]);   
	}

	// Class Finish
}
?>
