HFTP Draft

The Hypertext File Transfert Protocol (HFTP) is file transfert protocol built over HTTP.

The protocol use 4 HTTP Request: GET, PUT, DELETE, HEAD

1. GET
    retrive file, link or directory content

    TODO metadata: creation time, owners acl, type

    a. file
        the response header include stat of the file, data section include the raw file content.
        parameter offset in byte and/or length in byte can also be provided to get part of the file.
    b. directory
        the reponse is a always file with directory content encoded in ASCII with that may use HTTP escape. The response may include a encoding header thatprovide hint to the client to show the name to the user.
    c. link
    	link return the HTTP encoded link to the file.
2. HEAD
   get metata from the file, i.e. same as GET without file content, same as GET with length=0

3. PUT
    update the file content, similar to GET but to change state of the file.
    
