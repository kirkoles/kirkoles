n = 0

def app(env, start_response):
    global n
    n += 1
    response = "%.6d" % n

    start_response('200 OK', [('Content-Type', 'text/plain')])
    return [bytes(response, 'utf-8')]
