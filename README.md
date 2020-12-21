# ỨNG DỤNG XEM THỜI TIẾT(WEATHER APP)
### Ứng dụng xem thời tiết này giúp chúng ta có thể xem được nhiệt độ, trạng thái thời tiết của các thành phố trên thế giới

## Mở đầu ứng dụng ta sẽ thấy giao diện màn hình hiển thị như sau:

![1](https://user-images.githubusercontent.com/70943426/102795408-59e6d480-43df-11eb-8366-e8323cc414ad.png)


### Chúng ta sẽ có 3 nút để click vào:

#### Nút thời tiết Hà Nội sẽ xem được nhiệt độ hiện tại của Hà Nội, trạng thái thời tiết, độ ẩm và tốc độ gió. Cụ thể khi ta click vào sẽ hiển thị như sau:

![2](https://user-images.githubusercontent.com/70943426/102795458-6b2fe100-43df-11eb-8260-031c1634ab79.png)

#### Nút thứ hai là nút thời tiết Hà Nam. Khi click vào thì cũng sẽ hiển thị cho chúng ta các thông tin như nút thời tiết Hà Nội. Cụ thể khi click vào sẽ cho chúng ta thông tin như sau:

![3](https://user-images.githubusercontent.com/70943426/102795483-74b94900-43df-11eb-9d71-6f09b857daca.png)

#### Nút cuối cùng là nút tìm kiếm thông tin thời tiết của các thành phố trên toàn thế giới khi vào ta sẽ được màn hình mặc định như sau:

![4](https://user-images.githubusercontent.com/70943426/102795515-800c7480-43df-11eb-962e-8d677ef3618c.png)

> Ta sẽ nhận được thông tin nhiệt độ vào trạng thái thời tiết của thành phố đó.

### Giờ ta thử tìm kiếm trạng thái thời tiết của thành phố London nước Anh

![5](https://user-images.githubusercontent.com/70943426/102795520-826ece80-43df-11eb-8de3-7c5905fb843e.png)

> Nhiệt độ và trạng thái thời tiết của London.

### Giờ ta sẽ thử tìm thông tin về thành phố khác như thành phố Seoul của Hàn Quốc

![6](https://user-images.githubusercontent.com/70943426/102795741-d1b4ff00-43df-11eb-9897-f6c6414f0492.png)

> Ta nhận thấy với một trạng thái thời tiết thì ảnh backgroud sẽ hiển thị đúng với trạng thái đó.

### Ở đây ứng dụng của chúng ta có 10 hình ảnh tương ứng với 10 trạng thái thời tiết khác nhau

![7](https://user-images.githubusercontent.com/70943426/102795817-eabdb000-43df-11eb-82a4-2ae96a7aceee.png)

## Ứng dụng này chúng ta sử dụng 2 API thời tiết khác nhau để tìm kiếm thông tin. API của OpenWeatherMap([https://openweathermap.org/api](https://openweathermap.org/api)) và API của MetaWeather([https://www.metaweather.com/](https://www.metaweather.com/))

### Hai nút đầu tiên tìm kiếm thời tiết của Hà Nội và Hà Nam sử dụng API của OpenWeatherMap

![8](https://user-images.githubusercontent.com/70943426/102796048-3e2ffe00-43e0-11eb-9b30-9e3979421a1f.png)

### Sử dụng API Curent Weather Data để hiển thị thông tin thời tiết hiện tại của thành phố cụ thể

### Các giá trị chúng ta lấy về để hiển thị lên màn hình là: temp( nhiệt độ), description( mô tả trạng thái thời tiết), currently(chi tiết trạng thái thời tiết), humidity(độ ẩm) và windSpeed(tốc độ gió).

![9](https://user-images.githubusercontent.com/70943426/102796131-615aad80-43e0-11eb-9a97-ef417c781f53.png)

### Nút cuối cùng là nút tìm kiếm thời tiết theo khu vực sử dụng API của MetaWeather

![10](https://user-images.githubusercontent.com/70943426/102796188-7c2d2200-43e0-11eb-96a5-5ced717b6286.png)

### API này giúp chúng ta tìm kiếm thông tin thời tiết của các thành phố trên toàn thế giới.

![11](https://user-images.githubusercontent.com/70943426/102796241-8fd88880-43e0-11eb-89a9-9137888a5d29.png)

### Các giá trị chúng ta lấy về để hiển thị lên màn hình là: temperature(nhiệt độ) và location(địa điểm). Trạng thái thời tiết lấy về chính là hình ảnh dạng .png hiển thị trên màn hình.

### Ứng dụng này chúng ta sử dụng thêm nhiều thư viện như

![12](https://user-images.githubusercontent.com/70943426/102796352-b4346500-43e0-11eb-883b-6014350b8788.png)

#### Thư viện **font\_awesome** để thêm các icon phong phú của thông tin thời tiết

#### Thư viện **http** giúp chúng ta có thể điều hướng đến 1 trang web để lấy thông tin cần thiết về thời tiết.

#### Thư viện **dart:convert** có tính năng mã hóa, giải mã dữ liệu, kể cả JSON, UTF-8,…

#### Thư viện **dart:io** thư viện IO cung cấp các chức năng về File, Socket, HTTP,…

### Ứng dụng gồm có 4 màn hình để tương tác

### Từ màn hình chính điều hướng sang 3 màn hình còn lại

![13](https://user-images.githubusercontent.com/70943426/102796470-eba31180-43e0-11eb-91b8-95f6346165e7.png)

### Khi gọi API ứng dụng luôn sử dụng hàm bất đồng bộ để ứng dụng chạy được mượt mà mà không bị xung đột với nhau.

![14](https://user-images.githubusercontent.com/70943426/102796544-05445900-43e1-11eb-999c-2dca2491690c.png)

### Sau đây là toàn bộ source code của ứng dụng
      
      import &#39;dart:io&#39;;

      import &#39;package:flutter/material.dart&#39;;

      import &#39;package:font\_awesome\_flutter/font\_awesome\_flutter.dart&#39;;

      import &#39;package:http/http.dart&#39; as http;

      import &#39;dart:convert&#39;;

      void main() =\&gt; runApp(MaterialApp(

            title: &quot;Weather App&quot;,

            initialRoute: &#39;/&#39;,

            routes: {

              &#39;/&#39;: (context) =\&gt; FirstScreen(),

              &#39;/second&#39;: (context) =\&gt; Home(),

              &#39;/third&#39;: (context) =\&gt; Home2(),

              &#39;/four&#39;: (context) =\&gt; WeatherApp(),

            },

            // home: Home(),

            debugShowCheckedModeBanner: false,

          ));

      class FirstScreen extends StatelessWidget {

        const FirstScreen({Key key}) : super(key: key);

        @override

        Widget build(BuildContext context) {

          return new Container(

            decoration: BoxDecoration(

                image: DecorationImage(

                    image: AssetImage(&quot;images/background.jpg&quot;), fit: BoxFit.cover)),

            child: new Column(

              mainAxisAlignment: MainAxisAlignment.center,

              crossAxisAlignment: CrossAxisAlignment.center,

              children: \&lt;Widget\&gt;[

                new RaisedButton(

                  //child: new Text(&quot;Thời tiết Hà Nội&quot;),

                  color: Colors.blueAccent[600],

                  onPressed: () {

                    Navigator.pushNamed(context, &#39;/second&#39;);

                  },

                  textColor: Colors.white,

                  padding: const EdgeInsets.all(0.0),

                  shape: RoundedRectangleBorder(

                      borderRadius: BorderRadius.circular(80.0)),

                  child: Container(

                    decoration: const BoxDecoration(

                        gradient: LinearGradient(

                          colors: \&lt;Color\&gt;[

                            Color(0xFF0D47A1),

                            Color(0xFF1976D2),

                            Color(0xFF42A5F5),

                          ],

                        ),

                        borderRadius: BorderRadius.all(Radius.circular(80.0))),

                    padding: const EdgeInsets.fromLTRB(20, 10, 20, 10),

                    child: const Text(&#39;Thời tiết Hà Nội&#39;,

                        style: TextStyle(fontSize: 20)),

                  ),

                ),

                new RaisedButton(

                  //child: new Text(&quot;Thời tiết Đà Nẵng&quot;),

                  //color: Colors.blueAccent[600],

                  onPressed: () {

                    Navigator.pushNamed(context, &#39;/third&#39;);

                  },

                  textColor: Colors.white,

                  padding: const EdgeInsets.all(0.0),

                  shape: RoundedRectangleBorder(

                      borderRadius: BorderRadius.circular(80.0)),

                  child: Container(

                    decoration: const BoxDecoration(

                        gradient: LinearGradient(

                          colors: \&lt;Color\&gt;[

                            Color(0xFF0D47A1),

                            Color(0xFF1976D2),

                            Color(0xFF42A5F5),

                          ],

                        ),

                        borderRadius: BorderRadius.all(Radius.circular(80.0))),

                    padding: const EdgeInsets.fromLTRB(20, 10, 20, 10),

                    child: const Text(&#39;Thời tiết Hà Nam&#39;,

                        style: TextStyle(fontSize: 20)),

                  ),

                ),

                new RaisedButton(

                  //child: new Text(&quot;Tìm kiếm thời tiết theo khu vực&quot;),

                  //color: Colors.blueAccent[600],

                  onPressed: () {

                    Navigator.pushNamed(context, &#39;/four&#39;);

                  },

                  textColor: Colors.white,

                  padding: const EdgeInsets.all(0.0),

                  shape: RoundedRectangleBorder(

                      borderRadius: BorderRadius.circular(80.0)),

                  child: Container(

                    decoration: const BoxDecoration(

                        gradient: LinearGradient(

                          colors: \&lt;Color\&gt;[

                            Color(0xFF0D47A1),

                            Color(0xFF1976D2),

                            Color(0xFF42A5F5),

                          ],

                        ),

                        borderRadius: BorderRadius.all(Radius.circular(80.0))),

                    padding: const EdgeInsets.fromLTRB(20, 10, 20, 10),

                    child: const Text(&#39;Tìm kiếm thời tiết theo khu vực&#39;,

                        style: TextStyle(fontSize: 20)),

                  ),

                ),

              ],

            ),

          );

        }

      }

      class Home extends StatefulWidget {

        Home({Key key}) : super(key: key);

        @override

        \_HomeState createState() =\&gt; \_HomeState();

      }

      class \_HomeState extends State\&lt;Home\&gt; {

        var temp;

        var description;

        var currently;

        var humidity;

        var windSpeed;

        Future getWheather() async {

          http.Response response = await http.get(

              &quot;http://api.openweathermap.org/data/2.5/weather?q=Hanoi&amp;units=metric&amp;appid=0b02ee1c6dd9dafd7a2a8a0780323cc2&quot;);

          var results = jsonDecode(response.body);

          setState(() {

            this.temp = results[&#39;main&#39;][&#39;temp&#39;];

            this.description = results[&#39;weather&#39;][0][&#39;description&#39;];

            this.currently = results[&#39;weather&#39;][0][&#39;main&#39;];

            this.humidity = results[&#39;main&#39;][&#39;humidity&#39;];

            this.windSpeed = results[&#39;wind&#39;][&#39;speed&#39;];

          });

        }

        @override

        void initState() {

          super.initState();

          this.getWheather();

        }

        @override

        Widget build(BuildContext context) {

          return Scaffold(

            body: Column(

              children: \&lt;Widget\&gt;[

                Container(

                  height: MediaQuery.of(context).size.height / 3,

                  width: MediaQuery.of(context).size.width,

                  color: Colors.blue[300],

                  child: Column(

                    mainAxisAlignment: MainAxisAlignment.center,

                    crossAxisAlignment: CrossAxisAlignment.center,

                    children: \&lt;Widget\&gt;[

                      Padding(

                        padding: EdgeInsets.only(bottom: 10),

                        child: Text(&quot;Hà Nội hiện tại&quot;,

                            style: TextStyle(

                                color: Colors.white,

                                fontSize: 25.0,

                                fontWeight: FontWeight.w600)),

                      ),

                      Text(

                        temp != null ? temp.toString() + &quot;\u00B0&quot; + &quot;C&quot; : &quot;Loading&quot;,

                        style: TextStyle(

                            color: Colors.white,

                            fontSize: 40.0,

                            fontWeight: FontWeight.w600),

                      ),

                      Padding(

                        padding: EdgeInsets.only(top: 10.0),

                        child: Text(currently.toString(),

                            style: TextStyle(

                                color: Colors.white,

                                fontSize: 14.0,

                                fontWeight: FontWeight.w600)),

                      )

                    ],

                  ),

                ),

                Expanded(

                    child: Padding(

                  padding: EdgeInsets.all(20.0),

                  child: ListView(

                    children: \&lt;Widget\&gt;[

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.thermometerHalf),

                        title: Text(&quot;Nhiệt độ&quot;),

                        trailing: Text(temp.toString() + &quot;\u00B0&quot; + &quot;C&quot;),

                      ),

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.cloud),

                        title: Text(&quot;Thời tiết&quot;),

                        trailing: Text(description.toString()),

                      ),

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.water),

                        title: Text(&quot;Độ ẩm&quot;),

                        trailing: Text(humidity.toString() + &quot;%&quot;),

                      ),

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.wind),

                        title: Text(&quot;Tốc độ gió&quot;),

                        trailing: Text(windSpeed.toString() + &quot;m/s&quot;),

                      ),

                    ],

                  ),

                ))

              ],

            ),

          );

        }

      }

      class Home2 extends StatefulWidget {

        Home2({Key key}) : super(key: key);

        @override

        \_Home2State createState() =\&gt; \_Home2State();

      }

      class \_Home2State extends State\&lt;Home2\&gt; {

        var temp;

        var description;

        var currently;

        var humidity;

        var windSpeed;

        Future getWheather() async {

          http.Response response = await http.get(

              &quot;http://api.openweathermap.org/data/2.5/weather?q=Turan&amp;units=metric&amp;appid=0b02ee1c6dd9dafd7a2a8a0780323cc2&quot;);

          var results = jsonDecode(response.body);

          setState(() {

            this.temp = results[&#39;main&#39;][&#39;temp&#39;];

            this.description = results[&#39;weather&#39;][0][&#39;description&#39;];

            this.currently = results[&#39;weather&#39;][0][&#39;main&#39;];

            this.humidity = results[&#39;main&#39;][&#39;humidity&#39;];

            this.windSpeed = results[&#39;wind&#39;][&#39;speed&#39;];

          });

        }

        @override

        void initState() {

          super.initState();

          this.getWheather();

        }

        @override

        Widget build(BuildContext context) {

          return Scaffold(

            body: Column(

              children: \&lt;Widget\&gt;[

                Container(

                  height: MediaQuery.of(context).size.height / 3,

                  width: MediaQuery.of(context).size.width,

                  color: Colors.blue[300],

                  child: Column(

                    mainAxisAlignment: MainAxisAlignment.center,

                    crossAxisAlignment: CrossAxisAlignment.center,

                    children: \&lt;Widget\&gt;[

                      Padding(

                        padding: EdgeInsets.only(bottom: 10),

                        child: Text(&quot;Hà Nam hiện tại&quot;,

                            style: TextStyle(

                                color: Colors.white,

                                fontSize: 25.0,

                                fontWeight: FontWeight.w600)),

                      ),

                      Text(

                        temp != null ? temp.toString() + &quot;\u00B0&quot; + &quot;C&quot; : &quot;Loading&quot;,

                        style: TextStyle(

                            color: Colors.white,

                            fontSize: 40.0,

                            fontWeight: FontWeight.w600),

                      ),

                      Padding(

                        padding: EdgeInsets.only(top: 10.0),

                        child: Text(currently.toString(),

                            style: TextStyle(

                                color: Colors.white,

                                fontSize: 14.0,

                                fontWeight: FontWeight.w600)),

                      )

                    ],

                  ),

                ),

                Expanded(

                    child: Padding(

                  padding: EdgeInsets.all(20.0),

                  child: ListView(

                    children: \&lt;Widget\&gt;[

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.thermometerHalf),

                        title: Text(&quot;Nhiệt độ&quot;),

                        trailing: Text(temp.toString() + &quot;\u00B0&quot; + &quot;C&quot;),

                      ),

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.cloud),

                        title: Text(&quot;Thời tiết&quot;),

                        trailing: Text(description.toString()),

                      ),

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.water),

                        title: Text(&quot;Độ ẩm&quot;),

                        trailing: Text(humidity.toString() + &quot;%&quot;),

                      ),

                      ListTile(

                        leading: FaIcon(FontAwesomeIcons.wind),

                        title: Text(&quot;Tốc độ gió&quot;),

                        trailing: Text(windSpeed.toString() + &quot;m/s&quot;),

                      ),

                    ],

                  ),

                ))

              ],

            ),

          );

        }

      }

      class WeatherApp extends StatefulWidget {

        @override

        \_WeatherAppState createState() =\&gt; \_WeatherAppState();

      }

      class \_WeatherAppState extends State\&lt;WeatherApp\&gt; {

        int temperature;

        String location = &#39;Hà Nội&#39;;

        int woeid = 2487956;

        String weather = &#39;clear&#39;;

        String abbrevation = &#39;&#39;;

        String errorMessage = &#39;&#39;;

        String searchApiUrl =

            &#39;https://www.metaweather.com/api/location/search/?query=&#39;;

        String locationApiUrl = &#39;https://www.metaweather.com/api/location/&#39;;

        initState() {

          super.initState();

          fetchLocation();

        }

        void fetchSearch(String input) async {

          try {

            var searchResult = await http.get(searchApiUrl + input);

            var result = json.decode(searchResult.body)[0];

            setState(() {

              location = result[&quot;title&quot;];

              woeid = result[&quot;woeid&quot;];

              errorMessage = &#39;&#39;;

            });

          } catch (error) {

            setState(() {

              errorMessage =

                  &quot;Xin lỗi chúng tôi không tìm thấy dữ liệu về thành phố này!&quot;;

            });

          }

        }

        void fetchLocation() async {

          var locationResult = await http.get(locationApiUrl + woeid.toString());

          var result = json.decode(locationResult.body);

          var consolidated\_weather = result[&quot;consolidated\_weather&quot;];

          var data = consolidated\_weather[0];

          setState(() {

            temperature = data[&quot;the\_temp&quot;].round();

            weather = data[&quot;weather\_state\_name&quot;].replaceAll(&#39; &#39;, &#39;&#39;).toLowerCase();

            abbrevation = data[&quot;weather\_state\_abbr&quot;];

          });

        }

        void onTextFieldSubmitted(String input) async {

          await fetchSearch(input);

          await fetchLocation();

        }

        @override

        Widget build(BuildContext context) {

          return MaterialApp(

            debugShowCheckedModeBanner: false,

            home: Container(

                decoration: BoxDecoration(

                  image: DecorationImage(

                    image: AssetImage(&#39;images/$weather.png&#39;),

                    fit: BoxFit.cover,

                  ),

                ),

                child: temperature == null

                    ? Center(child: CircularProgressIndicator())

                    : Scaffold(

                        backgroundColor: Colors.transparent,

                        body: Column(

                          mainAxisAlignment: MainAxisAlignment.spaceEvenly,

                          crossAxisAlignment: CrossAxisAlignment.center,

                          children: \&lt;Widget\&gt;[

                            Column(

                              children: \&lt;Widget\&gt;[

                                Center(

                                  child: Image.network(

                                    &#39;https://www.metaweather.com/static/img/weather/png/&#39; +

                                        abbrevation +

                                        &#39;.png&#39;,

                                    width: 100,

                                  ),

                                ),

                                Center(

                                  child: Text(

                                    temperature.toString() + &#39; °C&#39;,

                                    style: TextStyle(

                                        color: Colors.white, fontSize: 60.0),

                                  ),

                                ),

                                Center(

                                  child: Text(

                                    location,

                                    style: TextStyle(

                                        color: Colors.white, fontSize: 40.0),

                                  ),

                                ),

                              ],

                            ),

                            Column(

                              children: \&lt;Widget\&gt;[

                                Container(

                                  width: 300,

                                  child: TextField(

                                    onSubmitted: (String input) {

                                      onTextFieldSubmitted(input);

                                    },

                                    style:

                                        TextStyle(color: Colors.white, fontSize: 25),

                                    decoration: InputDecoration(

                                      hintText: &#39;Tìm kiếm khu vực...&#39;,

                                      hintStyle: TextStyle(

                                          color: Colors.white, fontSize: 18.0),

                                      prefixIcon:

                                          Icon(Icons.search, color: Colors.white),

                                    ),

                                  ),

                                ),

                                Padding(

                                  padding:

                                      const EdgeInsets.only(right: 32.0, left: 32.0),

                                  child: Text(errorMessage,

                                      textAlign: TextAlign.center,

                                      style: TextStyle(

                                          color: Colors.redAccent,

                                          fontSize:

                                              Platform.isAndroid ? 15.0 : 20.0)),

                                )

                              ],

                            ),

                          ],

                        ),

                      )),

          );

        }

      }
