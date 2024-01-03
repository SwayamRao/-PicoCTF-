This actually is a very good lvl because we need to use the http headers in this.
We need burpsuite in repeater mode cause we need to make changes continuously.
First we need to change the 'User-Agent' value to picobrowser cause it is asking us to use pico browser.
Then we need to use the header called 'Referer' and give our current url.
Then we need to add header called 'Date' to add and manipulate the date and time.
Then we need to use 'DNT' which is 'do not track' and the value should be kept to 1.
Then we need to use 'X-Forwarded-For' and the ip address of sweden to access as sweden client.
Then we change the value of 'Accept-Launguage' to sv.
The whole challenge was to get to know about the http headers and how to manipuate those headers.
--------------------------------
Flag : picoCTF{http_h34d3rs_v3ry_c0Ol_much_w0w_79e451a7}
--------------------------------


Reading material : https://datatracker.ietf.org/doc/html/rfc2616#section-13
Reading material : https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
