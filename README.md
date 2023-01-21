# alerta_cuando_se_lee_atributo_clase
Codigo en python que alerta cuando se entra a un atributo de una clase usando __getattribute__


class D(object):
    def __init__(self):
        self.test = 20
        self.test2 = 40
    def __getattribute__(self, name):
        if name == 'test':
            return 0
        else:
            return object.__getattribute__(self, name)

obj1 = D()
print(obj1.test)
print(obj1.test2)
