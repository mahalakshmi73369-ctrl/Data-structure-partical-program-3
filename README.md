# Data-structure-partical-program-3
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

top = None

def push(data):
    global top
    new = Node(data)
    new.next = top
    top = new

def pop():
    global top
    if top is None:
        print "Stack Empty"
        return
    print "Undo:", top.data
    top = top.next

push("Type A")
push("Type B")
pop()
