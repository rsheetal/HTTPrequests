# HTTPrequests
Write a Python 3 program that uses the Requests module to make the following HTTP requests:  A: A Google search for the term "Tim Berners-Lee".  B: A POST request to a website that does not accept POST requests.  C: A request to a URL that does not exist.  For each request, your program must print:  The content ("body") of the response The status code of the response The response headers

"""
Created on Sat Sep  7 17:24:58 2019

@author: ranitassheetal
"""
import requests


a = requests.get('https://www.google.com/search?sxsrf=ACYBGNQF04lJZp5w2wOPbvVtqVgn2IZCAA%3A1567892286531&ei=PiN0XZbBH4nn_Qbh1KDYAg&q=tim+berners+lee&oq=tim+berners+lee&gs_l=psy-ab.3...2546.2951..3353...0.0..0.0.0.......0....1..gws-wiz.xY6eVlrnIfY&ved=0ahUKEwiW2KL21b_kAhWJc98KHWEqCCsQ4dUDCAs&uact=5')
print(a.text)
print(a.status_code)
print(a.headers)

b = requests.post('https://facebook.com')
print(b.text)
print(b.status_code)
print(b.headers)

c = requests.get('http://www.ranita.com')
print(c.text)
print(c.status_code)
print(c.headers)
