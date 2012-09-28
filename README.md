### Test Rails 4.0.0.beta asset pipeline changes

```
$ bundle install

$ time rake assets:precompile

...

** Execute assets:precompile:primary
D, [2012-09-28T12:49:06.206060 #27591] DEBUG -- : Compiled jquery.js  (2ms)  (pid 27591)
D, [2012-09-28T12:49:06.209140 #27591] DEBUG -- : Compiled jquery_ujs.js  (0ms)  (pid 27591)
D, [2012-09-28T12:49:06.300457 #27591] DEBUG -- : Compiled test.js  (89ms)  (pid 27591)
D, [2012-09-28T12:49:06.308536 #27591] DEBUG -- : Compiled application.js  (106ms)  (pid 27591)
D, [2012-09-28T12:49:08.429498 #27591] DEBUG -- : Compiled test.css  (3ms)  (pid 27591)
D, [2012-09-28T12:49:08.433272 #27591] DEBUG -- : Compiled test_erb.css  (1ms)  (pid 27591)
D, [2012-09-28T12:49:08.435215 #27591] DEBUG -- : Compiled application.css  (10ms)  (pid 27591)
D, [2012-09-28T12:49:08.444315 #27591] DEBUG -- : Processed digest assets in 2327ms
** Invoke assets:precompile:nondigest (first_time)
** Invoke assets:cache:clean
** Execute assets:precompile:nondigest
D, [2012-09-28T12:49:08.477553 #27591] DEBUG -- : Copied rails-35ec2bb29b15e93360da072060d3ab17.png to rails.png
D, [2012-09-28T12:49:08.478820 #27591] DEBUG -- : Stripped digests and copied application-786703dc9c99d2ed2229dc653d451cc1.js to application.js
D, [2012-09-28T12:49:08.479540 #27591] DEBUG -- : Stripped digests and copied application-b332dfbf73a8ec409467e94d6dd78183.css to application.css
D, [2012-09-28T12:49:08.481713 #27591] DEBUG -- : Processed non-digest assets in 33ms

real  0m10.435s
user  0m9.809s
sys 0m0.524s

$ time rake assets:precompile

...

** Execute assets:precompile:primary
D, [2012-09-28T12:49:40.528302 #27704] DEBUG -- : Not compiling rails.png, sources digest has not changed (35ec2bb)
D, [2012-09-28T12:49:40.598432 #27704] DEBUG -- : Not compiling application.js, sources digest has not changed (0692d5c)
D, [2012-09-28T12:49:40.610088 #27704] DEBUG -- : Not compiling application.css, sources digest has not changed (b6e7001)
D, [2012-09-28T12:49:40.612907 #27704] DEBUG -- : Processed digest assets in 87ms
** Invoke assets:precompile:nondigest (first_time)
** Invoke assets:cache:clean
** Execute assets:precompile:nondigest
D, [2012-09-28T12:49:40.615554 #27704] DEBUG -- : Copied rails-35ec2bb29b15e93360da072060d3ab17.png to rails.png
D, [2012-09-28T12:49:40.616753 #27704] DEBUG -- : Stripped digests and copied application-786703dc9c99d2ed2229dc653d451cc1.js to application.js
D, [2012-09-28T12:49:40.617471 #27704] DEBUG -- : Stripped digests and copied application-b332dfbf73a8ec409467e94d6dd78183.css to application.css
D, [2012-09-28T12:49:40.619520 #27704] DEBUG -- : Processed non-digest assets in 4ms

real  0m8.120s
user  0m7.568s
sys 0m0.452s
```