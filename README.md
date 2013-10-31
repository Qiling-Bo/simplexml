simplexml
=========

load xml to dict and dump dict to xml in python

usage
-----

original diction for example:

    dic = {'date': '2009-11-25',
           'errorcode': 7,
           'errormsg': u'Noise Too High',
           'item': 'SNR',
           'noise': {'data': [5, 6, 7]},
           'signal': {'data': [1, 2, 3]},
           'sn': 2103839}

dump dict to xml:

    import simplexml
    xml = simplexml.dumps(dic)
    print(xml)

result:

    <?xml version="1.0" ?>
    <xml>
        <noise>
            <data>5</data>
            <data>6</data>
            <data>7</data>
        </noise>
        <errormsg>Noise Too High</errormsg>
        <signal>
            <data>1</data>
            <data>2</data>
            <data>3</data>
        </signal>
        <errorcode>7</errorcode>
        <item>SNR</item>
        <sn>2103839</sn>
        <date>2009-11-25</date>
    </xml>

load xml to dict:

    import simplexml
    dic = simplexml.loads(xml)
    print(dic)

result:

    {u'date': u'2009-11-25',
    u'errorcode': u'7',
    u'errormsg': u'Noise Too High',
    u'item': u'SNR',
    u'noise': {u'data': [u'5', u'6', u'7']},
    u'signal': {u'data': [u'1', u'2', u'3']},
    u'sn': u'2103839'}
