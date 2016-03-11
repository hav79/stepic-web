def app(environ, start_response):
    
    params_str = environ["QUERY_STRING"]
    data = [s + '\n' for s in params_str.split("&")]
    status = '200 OK'
    response_headers = [
        ('Content-type','text/plain'),
        ('Content-Length', str(len(data)))
    ]
    start_response(status, response_headers)
    return iter([data])
