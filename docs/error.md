# error


```shell

====================[ Build | testodbaccess | Debug ]===========================
/root/clion-2018.2.6/bin/cmake/linux/bin/cmake --build /root/CLionProjects/testodbaccess/cmake-build-debug --target testodbaccess -- -j 1
-- Configuring done
-- Generating done
-- Build files have been written to: /root/CLionProjects/testodbaccess/cmake-build-debug
Scanning dependencies of target testodbaccess
[ 50%] Building CXX object CMakeFiles/testodbaccess.dir/driver.cxx.o
In file included from /root/CLionProjects/testodbaccess/driver.cxx:10:0:
/root/CLionProjects/testodbaccess/database.hxx:35:13: warning: ‘template<class> class std::auto_ptr’ is deprecated [-Wdeprecated-declarations]
 inline std::auto_ptr<odb::database>
             ^
In file included from /opt/rh/devtoolset-4/root/usr/include/c++/5.2.1/memory:81:0,
                 from /root/CLionProjects/testodbaccess/driver.cxx:4:
/opt/rh/devtoolset-4/root/usr/include/c++/5.2.1/bits/unique_ptr.h:49:28: note: declared here
   template<typename> class auto_ptr;
                            ^
In file included from /root/CLionProjects/testodbaccess/driver.cxx:10:0:
/root/CLionProjects/testodbaccess/database.hxx: In function ‘std::auto_ptr<odb::database> create_database(int&, char**)’:
/root/CLionProjects/testodbaccess/database.hxx:62:3: warning: ‘template<class> class std::auto_ptr’ is deprecated [-Wdeprecated-declarations]
   auto_ptr<database> db (new odb::mysql::database (argc, argv));
   ^
In file included from /opt/rh/devtoolset-4/root/usr/include/c++/5.2.1/memory:81:0,
                 from /root/CLionProjects/testodbaccess/driver.cxx:4:
/opt/rh/devtoolset-4/root/usr/include/c++/5.2.1/bits/unique_ptr.h:49:28: note: declared here
   template<typename> class auto_ptr;
                            ^
/root/CLionProjects/testodbaccess/driver.cxx: In function ‘int main(int, char**)’:
/root/CLionProjects/testodbaccess/driver.cxx:23:5: warning: ‘template<class> class std::auto_ptr’ is deprecated [-Wdeprecated-declarations]
     auto_ptr<database> db (create_database (argc, argv));
     ^
In file included from /opt/rh/devtoolset-4/root/usr/include/c++/5.2.1/memory:81:0,
                 from /root/CLionProjects/testodbaccess/driver.cxx:4:
/opt/rh/devtoolset-4/root/usr/include/c++/5.2.1/bits/unique_ptr.h:49:28: note: declared here
   template<typename> class auto_ptr;
                            ^
[100%] Linking CXX executable testodbaccess
CMakeFiles/testodbaccess.dir/driver.cxx.o：在函数‘odb::object_traits<person>::id_type odb::database::persist_<person, (odb::database_id)5>(person&)’中：
/usr/local/include/odb/database.txx:38：对‘odb::access::object_traits_impl<person, (odb::database_id)0>::persist(odb::database&, person const&)’未定义的引用
CMakeFiles/testodbaccess.dir/driver.cxx.o：在函数‘odb::result<person> odb::database::query_<person, (odb::database_id)5, (odb::class_kind)0>::call<odb::query<person, odb::mysql::query_base> >(odb::database&, odb::query<person, odb::mysql::query_base> const&)’中：
/usr/local/include/odb/database.txx:478：对‘odb::access::object_traits_impl<person, (odb::database_id)0>::query(odb::database&, odb::mysql::query_base const&)’未定义的引用
collect2: error: ld returned 1 exit status
gmake[3]: *** [testodbaccess] 错误 1
gmake[2]: *** [CMakeFiles/testodbaccess.dir/all] 错误 2
gmake[1]: *** [CMakeFiles/testodbaccess.dir/rule] 错误 2
gmake: *** [testodbaccess] 错误 2


```