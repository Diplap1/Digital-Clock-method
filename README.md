# Digital-Clock-method
Digital clock method in html by diplap


#code is here 
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>
		digital clock
	</title>
</head>
<body>
<div id="clock">8:17:25</div>
<script type="text/javascript">
	setInterval(showTime,1000);
	//showtime function define
	function showTime(){
//get current time and date
		let time=new Date();
		let hour = time.getHours();
		let min = time.getMinutes();
		let sec =time.getSeconds();
		am_pm= "AM";
		//settinf time for 12 hr format
		if(hour >=12){
			if (hour >12) hour -=12;
			am_pm="PM";

		}
		else if (hour ==0){
			hr =12;
			am_pm ="AM";

		}
		hour = 
		hour<10 ? "0" + hour :hour;
		min =min < 10 ? "0" + min :min;
		sec = sec <10 ? "0" + sec : sec;

		let CurrentTime =
		hour +
		":" +
		min + 
		":" +
		sec +
		am_pm;

		//displaying the time
		document.getElementById("clock").innerHTML =currentTime;

	}
	showTime();
</script>
</body>
</html>
