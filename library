a = [['book1',10],['book2',10],['book3',10]]

default=[['book1',10],['book2',10],['book3',10]]
student = {
    1 : {},
    2 : {},
    3 : {}
}

cn=True

while cn == True:
    print('\n============= Welcome To Library ==============\n')
    print('1. List of books\n2. Borrow a book\n3. Return a book\n4. exit\n5. student data')
    b=int(input('enter your choice: '))
    if b==1:
        for i,j in a:
            print(i,j)
            
    elif b==2:
        e = input('enter the name of book: ')
        e= e.lower()
        id = int(input('enter your id: '))
        if e in student[id].keys():
            print('you already have this book')
            break
        if id in student.keys():
            for i,j in enumerate(a):
                if e in j:
                    if(a[i][1]==0):
                        print('book unavailable')
                        break
                    else: 
                        a[i][1]-=1
                        student[id][e]= [1,2]

                        print(f'{e} has been issued to you')

                        break
            else:
                print('book unavailable')
                cn = False
                break
        else:
            student[id] = {}

    elif b==3:
        id = int(input('enter your id: '))
        if id in student.keys():
            f = input('enter the name of book you want to return: ')
            f = f.lower()
            if f in student[id].keys():
                for i,j in enumerate(a):
                    if f in j:
                        if a[i][1] < default[i][1]:
                            a[i][1]+=1
                            del student[id][f]
                            print(f'{f} has been returned')
                            break
                        else:
                            print('this book was not taken from here')
                            break
                else:
                    print('this book doesnt belong to this library')
                    cn = False
                    break
            else:
                print('you havent taken this book')
                break
        else:
            print('you have not taken any book')
    elif b ==4:
        exit()
    elif b==5:
        print(student)
