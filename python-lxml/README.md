## Python lxml

### How to use it?

```
$ docker pull mfuentesg/python-lxml
$ docker run --rm python-lxml python -c "from lxml import html; tree = html.fromstring('<html><body><h1>Hello lxml</h1></body></html>'); print(tree.xpath('//h1')[0].text)"

# Hello lxml
```
