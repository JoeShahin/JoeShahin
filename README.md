// ignore_for_file: prefer_const_literals_to_create_immutables, override_on_non_overriding_member

//import 'dart:ui';

import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Ecommerce(),
    );
  }
}

class Ecommerce extends StatefulWidget {
  const Ecommerce({Key? key}) : super(key: key);

  @override
  State<Ecommerce> createState() => _EcommerceState();
}

late int selectedindex = 0;

class _EcommerceState extends State<Ecommerce> with SingleTickerProviderStateMixin {
  late TabController myController;
  @override
  // ignore: must_call_super
  void initState() {
    myController = TabController(length: 2, vsync: this, initialIndex: 1);
  }

  GlobalKey<ScaffoldState> scaffoldKey = GlobalKey<ScaffoldState>();
  @override
  Widget build(BuildContext context) {
    return Scaffold(
        key: scaffoldKey,
        bottomNavigationBar: BottomNavigationBar(
            currentIndex: selectedindex,
            onTap: (index) {
              setState(() {
                selectedindex = index;
              });
            },
            items: const [
              BottomNavigationBarItem(
                label: "",
                icon: Icon(Icons.settings),
                backgroundColor: Color.fromARGB(255, 49, 121, 93),
              ),
              BottomNavigationBarItem(
                label: "",
                icon: Icon(Icons.info),
                backgroundColor: Color.fromARGB(255, 49, 121, 93),
              ),
              BottomNavigationBarItem(
                label: "",
                icon: Icon(Icons.person_outlined),
                backgroundColor: Color.fromARGB(255, 49, 121, 93),
              ),
              BottomNavigationBarItem(label: "", icon: Icon(Icons.home))
            ]),
        appBar: AppBar(
            elevation: 1,
            bottom: TabBar(
                controller: myController,
                isScrollable: true,
                labelColor: const Color.fromARGB(153, 61, 172, 94),
                tabs: const [
                  Tab(
                    child: Text(
                      "سـابقـة",
                      style: TextStyle(
                          color: Colors.green,
                          fontSize: 15,
                          fontWeight: FontWeight.bold),
                    ),
                  ),
                  Tab(
                    child: Text(
                      "جـديـدة",
                      style: TextStyle(
                          color: Colors.green,
                          fontSize: 15,
                          fontWeight: FontWeight.bold),
                    ),
                    //icon: Icon(Icons.person),
                  ),
                ]),
            backgroundColor: const Color.fromARGB(253, 255, 255, 255),
            actions: [
              Container(
                padding: const EdgeInsets.only(right: 10),
                child: const Icon(
                  Icons.arrow_forward_ios,
                  color: Colors.green,
                ),
              ),
            ]),
        //drawer: const Drawer(),
        body: Container(
          padding: const EdgeInsets.only(top: 10),
          child: Column(
            children: [
              Container(
                  padding: const EdgeInsets.only(top: 10),
                  child: Column(
                    children: [
                      ListTile(
                        title: const Text("رقم الطلب. 398227",
                            style: TextStyle(
                                fontSize: 20,
                                fontWeight: FontWeight.bold,
                                color: Colors.blueAccent)),
                        subtitle: const Text("كمية الطلب"),
                        isThreeLine: false,
                        leading: const Icon(Icons.arrow_back_ios, size: 20),
                        trailing: Image.asset('images/3.webp'),
                      ),
                      const Text(
                        "اسـتلام مـن الفـرع",
                        style: TextStyle(fontWeight: FontWeight.bold),
                        textAlign: TextAlign.start,
                      ),
                      Container(
                        padding: const EdgeInsets.only(top: 20),
                        child: Row(
                          mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                          textDirection: TextDirection.rtl,
                          children: const [
                            Icon(
                              Icons.timer_outlined,
                              color: Colors.blueAccent,
                            ),
                            Text(
                              "12 May. 12:50 AM",
                              style: TextStyle(
                                  color: Color.fromARGB(255, 74, 74, 75)),
                            ),
                            Icon(
                              Icons.description_outlined,
                              color: Colors.blueAccent,
                            ),
                            Text(
                              "قيد الانتظار",
                              style: TextStyle(
                                  color: Color.fromARGB(255, 81, 81, 82)),
                            ),
                          ],
                        ),
                      )
                    ],
                  )),
              Container(
                  padding: const EdgeInsets.only(top: 10),
                  child: Column(
                    children: [
                      ListTile(
                        title: const Text("رقم الطلب. 398227",
                            style: TextStyle(
                                fontSize: 20,
                                fontWeight: FontWeight.bold,
                                color: Colors.blueAccent)),
                        subtitle: const Text("كمية الطلب"),
                        isThreeLine: false,
                        leading: const Icon(Icons.arrow_back_ios, size: 20),
                        trailing: Image.asset('images/3.webp'),
                      ),
                      const Text(
                        "اسـتلام مـن الفـرع",
                        style: TextStyle(fontWeight: FontWeight.bold),
                        textAlign: TextAlign.start,
                      ),
                      Container(
                        padding: const EdgeInsets.only(top: 20),
                        child: Row(
                          mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                          textDirection: TextDirection.rtl,
                          children: const [
                            Icon(
                              Icons.timer_outlined,
                              color: Colors.blueAccent,
                            ),
                            Text(
                              "12 May. 12:50 AM",
                              style: TextStyle(
                                  color: Color.fromARGB(255, 74, 74, 75)),
                            ),
                            Icon(
                              Icons.description_outlined,
                              color: Colors.blueAccent,
                            ),
                            Text(
                              "قيد الانتظار",
                              style: TextStyle(
                                  color: Color.fromARGB(255, 81, 81, 82)),
                            ),
                          ],
                        ),
                      )
                    ],
                  )),
              Container(
                  padding: const EdgeInsets.only(top: 10),
                  child: Column(
                    children: [
                      ListTile(
                        title: const Text("رقم الطلب. 398227",
                            style: TextStyle(
                                fontSize: 20,
                                fontWeight: FontWeight.bold,
                                color: Colors.blueAccent)),
                        subtitle: const Text("كمية الطلب"),
                        isThreeLine: false,
                        leading: const Icon(Icons.arrow_back_ios, size: 20),
                        trailing: Image.asset('images/3.webp'),
                      ),
                      const Text(
                        "اسـتلام مـن الفـرع",
                        style: TextStyle(fontWeight: FontWeight.bold),
                        textAlign: TextAlign.start,
                      ),
                      Container(
                        padding: const EdgeInsets.only(top: 20),
                        child: Row(
                          mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                          textDirection: TextDirection.rtl,
                          children: const [
                            Icon(
                              Icons.timer_outlined,
                              color: Colors.blueAccent,
                            ),
                            Text(
                              "12 May. 12:50 AM",
                              style: TextStyle(
                                  color: Color.fromARGB(255, 74, 74, 75)),
                            ),
                            Icon(
                              Icons.description_outlined,
                              color: Colors.blueAccent,
                            ),
                            Text(
                              "قيد الانتظار",
                              style: TextStyle(
                                  color: Color.fromARGB(255, 81, 81, 82)),
                            ),
                          ],
                        ),
                      )
                    ],
                  )),
            ],
          ),
        ));
  }
}
