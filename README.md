def start():
    try:
        atte = 0
        i = int(input("The least amount of files: "))
        max = int(input("The most amount of files: "))
        if i < max:
            while i < max:
                if atte == 0:
                    f = open("test.txt", "w")
                    print("THIS IS A FILE FROM THE PROGRAM! YOU CAN DELETE THIS FILE!", file=f)
                    f.close()
                    atte = atte + 1
                f = open("test" + str(atte) + ".txt", "w")
                print("THIS IS A FILE FROM THE PROGRAM! YOU CAN DELETE THIS FILE!", file=f)
                f.close()
                i = i + 1
                atte = atte + 1
            print("==============================")
            print("The command has been executed.")
            print("==============================")
        else:
            print("Least amount of files < max amount of files.")
            start()
    except:
        print("ERROR PLEASE TRY AGAIN.")
        start()
start()
