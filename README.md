# ESP8266-Wifi-module-1
 void setup() {
  Serial.begin(115200);
  delay(1000);
  Serial.println("AT+CWJAP=\"Simulator Wifi\",\"\"\r\n");//if you wanna you thingsspeak through tinker cad use simulator wifi as your ssid
  delay(3000);
}
 void loop() {
{
  Serial.println("AT+CIPSTART=\"TCP\",\"api.thingspeak.com\",80\r\n");
  delay(5000);
  int len = 57;//length of line 15
  Serial.print("AT+CIPSEND=");
  Serial.println(len);
  delay(10);
  Serial.print("GET /update?api_key=5GU4JMNLQDFZXUUJ&field1=500 HTTP/1.1\r\n");
  delay(100);
  Serial.println("AT+CIPCLOSE=0\r\n");
  delay(6000);
}
} 
