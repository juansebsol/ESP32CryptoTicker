<!DOCTYPE html>
<html>
  <head>

  <body>
    <h1>ESP32StockTicker</h1>
    <h3><u>Summary</u></h3>
    <p>ESP32 based stock ticker that uses a MAX7219 LED Matrix (mine is 4
      segments but how many is up to you), that receives the ticker symbol from
      self served webpage.</p>
    <p>I am currently using Yahoo Finance for price info every 5 seconds but you
      can change that to the API of your choice along with the update frequency.</p>
    <p>This code utilizes both cores, without doing so causes a pause when
      prices get updated. Technically should work on ESP8266 with changes.</p>
    <p>I am not a developer or programmer, so my code is not pretty, but it
      works and I work on it all the time. </p>
    <p>This code is compatible with Arduino and PlatformIO.</p>
    <h3><u>Libraries Used:</u></h3>
    <p><a href="https://github.com/bartoszbielawski/LEDMatrixDriver" target="_blank">LEDMatrixDriver</a>
      by <a href="https://github.com/bartoszbielawski" target="_blank">Bartosz
        Bielawski</a><br>
      <a href="https://github.com/me-no-dev/ESPAsyncWebServer" target="_blank">ESPAsyncWebServer</a>
      by <a href="https://github.com/me-no-dev" target="_blank">Me No Dev</a></p>
    <h3><u>Setup</u></h3>
    <p>My personal ESP32 setup is as follows:</p>
    <table style="width: 289px; height: 160px;" border="1">
      <tbody>
        <tr>
          <td><u>ESP32 Pins</u></td>
          <td><u>LED Matrix</u></td>
        </tr>
        <tr>
          <td>3.3V</td>
          <td>VCC</td>
        </tr>
        <tr>
          <td>GND</td>
          <td>GND</td>
        </tr>
        <tr>
          <td>23</td>
          <td>DIN</td>
        </tr>
        <tr>
          <td>15</td>
          <td>CS</td>
        </tr>
        <tr>
          <td>18</td>
          <td>CLK</td>
        </tr>
      </tbody>
    </table>
    <p>You must insert your own SSID and password for your Wifi, so it can
      connect. </p>
    <p>Upon getting an IP address it will display it continually on the LED
      Matrix until it receives its first ticker symbol.</p>
    <p>From any browser input the IP address where you will be presented with a
      ticker input. </p>
    <p>Input the ticker symbol, the program automatically changes it to
      uppercase, so it's okay to be lazy here.</p>
    <p>The program will automatically check for a new price every 5 seconds.</p>
    <p>It also supports crypto, but you must use the Yahoo Finance format, for
      example BTC-USD for Bitcoin.</p>
    <p>Any symbol that works on Yahoo Finance should technically work.</p>
    <p><br>
    </p>
  </body>
</html>
