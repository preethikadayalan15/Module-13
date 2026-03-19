Reg - 212222090019 D.Prethika

OPERATORS=set(['*','+']) 


def evaluate_postfix(expression):
    stack=[] 
    for i in expression:
        if i not in OPERATORS:
            stack.append(i)  
        
        else:
            a=stack.pop()  
            b=stack.pop()
        
            if i=='+':
                res=int(b)+int(a)  
            elif i=='*':
                res=int(b)*int(a)
            
            stack.append(res) 
    return stack[0]

expression = input()
print('postfix expression: ',expression)
print('Evaluation result: ',evaluate_postfix(expression))
