
import win32con, win32api
import time
import random
import pyautogui
import os
import os.path
import keyboard
import sys
import gc


sys.setrecursionlimit(20000)
Buxdesired = 10
Gasdesired = 40000
Mindesired = 40000






#me2=0

x=0
image = ['0.png','1.png','2.png','3.png','4.png','5.png','6.png','7.png','8.png','9.png','dot.png','m.png','k.png'] 
Firstlist = []
Firstlist1 = []
dispatch1 = []
dispatch = []
img=0
escapevalue = False


def click(x,y):
    win32api.SetCursorPos ((x,y)) #cursor location to click
    win32api.mouse_event(win32con.MOUSEEVENTF_LEFTDOWN, 0,0)
    time.sleep(0.01)
    win32api.mouse_event(win32con.MOUSEEVENTF_LEFTUP,0,0)


def detectingheroic():
    timeout =time.time() + 1.5
    #while keyboard.is_pressed('`') == True:
    while True:
        #if keyboard.is_pressed('`'):

            q=[526,369,339,330,325,316,311,304,290,281,269];z=[1032,1034,1035,1037,1038,1041,1043,1045,1046,1049,1056];j=[209,27,132,66];i=random.randint(0,10);k=random.randint(0,3) #click coordinate
            #if pyautogui.pixel(q,z)  == (151,115,123): (For all 3 pixel type)
            if pyautogui.pixel(q[i],z[i]) [2] == j[k]: #pasting array into coordinate (can mix with detecting type and change this later)
                #click(1687,1021) #clicking location (delaying the click till identifying what would happen                     )
                #time.sleep(0) # delay the click so that it wont click multiple time
                return 1
            if time.time()>=timeout:
                return 0


def multiplycation(a,z):#having problem here
    if z == 1:   
        a = a*10**3
    elif z == 2:
        a = a*10**6#if removed the int(float) value, it will print 1Mil times the value for some reason    
    return a
    



def ignoreten(h):
    #ignore all 10 after the first was found
    indices = [i for (i,v) in enumerate(h) if v == 10]
    for i in reversed(indices[1:]):
        del h[i]
                
    
def listrule(h):
    try:
        #deny in case first value of dispatch is "."
        if h[0] == 10:
            del h[0]
        #if h[-2] == 10:
        #    del h[-1]
        if h[-1] == 10:
            del h[-1]
    except IndexError:
        pass

def gettingimage():
    global image
    if pyautogui.locateOnScreen("BuxImage2.png", confidence = 0.90,region=( 1571 , 990 , 230 , 68 ))!= None or pyautogui.locateOnScreen("GasImage.png", confidence = 0.80,region=( 1571 , 990 , 230 , 68 ))!= None or pyautogui.locateOnScreen("MinImage.png", confidence = 0.80,region=( 1571 , 990 , 230 , 68 ))!= None:
        img = pyautogui.screenshot(region=( 1571 , 990 , 230 , 68 ))
        img.save("valuereader.png")

def throwingimage2():
    old_name = r"C:/Users/duong/OneDrive/Desktop/Automations/valuereader.png"
    new_name = r"C:/Users/duong/OneDrive/Desktop/Automations/valuereader2.png"

# Renaming the file
    if os.path.exists(r"C:/Users/duong/OneDrive/Desktop/Automations/valuereader2.png"):
        os.remove("valuereader2.png")
    os.rename(old_name, new_name)


#Write a function, only run the code when detect bux, gas or mineral image in the text box
def hindering():   
    global Firstlist1
    a=0
    z=0
    Firstlist1 =[]
    print('New List Value')
    for x in range (0,13):            
        if x == 1:      #condition to check and exit loop should be check here
            Firstlist =  list(pyautogui.locateAllOnScreen(image[x], confidence = 0.95,region=( 1569 , 987 , 209 , 87 ))) #with x equal zero as defined
        elif  x != 1 or x != 10 or x !=11 or x!=12:
            Firstlist =  list(pyautogui.locateAllOnScreen(image[x], confidence = 0.85,region=( 1569 , 987 , 209 , 87 ))) #with x equal zero as defined
        elif x == 10:
            Firstlist =  list(pyautogui.locateAllOnScreen(image[x],confidence = 0.85,region=( 1650 , 1020 , 150 , 50 )))
        #Firstlist1 = list(pyautogui.locateAllOnScreen(image1, confidence = 0.95,region=( 1570 , 990 , 230 , 70 ))) + Firstlist
        if len(Firstlist) >= 2: #NOTE: THIS SHOULD BE ENABLE IF FEEL LIKE THE VALUE IS TOO TRIPY
            elems = [f[0] for f in Firstlist]  # create a list of just first index
            i = 0
            while i < len(elems) - 1:  # iterate through the list with i
                j = i + 1
                while j < len(elems):  # iterate through the rest of the list with j
                    if abs(elems[i] - elems[j]) <= 6:  # if item at index i is within 5 pixels of item at index j
                        del elems[j]
                        del Firstlist[j]   # delete item j and continue
                    else:
                        j += 1    # otherwise move to next item
                i += 1  #  Move to next i item
            #print (elems)
        #if x == 1
        Firstlist = [F[0:1] for F in Firstlist]#get first value for first list
        for i in range (0,len(Firstlist)):
            if x in range(0,11):
                if len(Firstlist) !=0:#set order for list (223,1),(224,2)
                    Firstlist[i]+=(x,)   #NOTE : Only Tuple concatenate with each other and tuple cannot be edit, hence, Immutable
                    #print (Firstlist) #DEBUG LINE
                    
        if x in range (0,11):
           #print(len(Firstlist), '     and this is ', x)
            Firstlist1 =Firstlist1 +Firstlist
    #print(Firstlist1)

    #print(Firstlist1)
    dispatch1 = ([F[1] for F in Firstlist1])
    dispatch = ([F[0] for F in Firstlist1])
    if len(dispatch1) !=0:
        #DEBUGGGGG LINEEEEE      print (Firstlist1)
        counter = 0
        if len(dispatch) != 1:
            while counter <2: 
                for i in range (0, len(dispatch)-1): 
                    for j in range (i,len(dispatch)):
                        if dispatch[i]>dispatch[j]:
                            dispatch[i],dispatch[j]=dispatch[j],dispatch[i]
                            dispatch1[i],dispatch1[j]=dispatch1[j],dispatch1[i]
                            counter=0
                        j=j+1
                    i=i+1
                    if i== len(dispatch)-1:
                        counter=counter+1
        listrule(dispatch1)#modifying dispatch1 for value (deleting first value incase it indicate it is ".")
        ignoreten(dispatch1)#deleting all value after the firstone in case it found duplicate

        if pyautogui.locateOnScreen(image[11], confidence = 0.7,region=( 1569 , 987 , 209 , 87 )) != None:
            z =2 
        elif pyautogui.locateOnScreen(image[12], confidence = 0.7,region=( 1569 , 987 , 209 , 87 )) != None:
            z =1

        #elif x == 12:
        #    if list(pyautogui.locateAllOnScreen(image[x], confidence = 0.95,region=( 1569 , 987 , 209 , 87 ))) != None:
        #        print('saw M')
        #        z =2            
        for i in range(0, len(dispatch1)):
            if dispatch1[i] == 10:
                dispatch1[i] = '.'
        #print(dispatch)
        a = str(dispatch1[0])      
        for i in range(0, len(dispatch1)-1):
            a = a+str(dispatch1[i+1])
        a=int(float(a))                
        print (multiplycation(a,z))
        return multiplycation(a,z)




def condition(x,y):
    global escapevalue
    if x == 0:
        mainrunner()
    if pyautogui.locateOnScreen("BuxImage2.png", confidence = 0.90,region=( 1571 , 990 , 230 , 68 ))!= None:
        if (x <= Buxdesired and y == 1):
            click(1687,1021)
            escapevalue= True
            cancel()            
            click(1296,631)
    elif pyautogui.locateOnScreen("MinImage.png", confidence = 0.80,region=( 1571 , 990 , 230 , 68 )) != None:
        if (x <= Mindesired and y == 1) or (x <= 6000 and y==0):            
            click(1687,1021)
            escapevalue= True
            cancel()            
            click(1296,631)
    elif pyautogui.locateOnScreen("GasImage.png", confidence = 0.80,region=( 1571 , 990 , 230 , 68 ))!= None:
        if (x <= Gasdesired and y == 1) or (x <= 6000 and y==0):
            click(1687,1021)
            escapevalue= True
            cancel()           
            click(1100,618)
    
def checktrue():
    if (pyautogui.locateOnScreen("BuxImage2.png", confidence = 0.90,region=( 1571 , 990 , 230 , 68 ))!= None or pyautogui.locateOnScreen("GasImage.png", confidence = 0.80,region=( 1571 , 990 , 230 , 68 ))!= None or pyautogui.locateOnScreen("MinImage.png", confidence = 0.80,region=( 1571 , 990 , 230 , 68 ))!= None) and pyautogui.locateOnScreen("valuereader2.png",region=( 1571 , 990 , 230 , 68 )) == None:
        if pyautogui.locateOnScreen("valuereader.png", confidence = 0.90,region=( 1571 , 990 , 230 , 68 )) != None:
            return True#equal image value1 but different from oldimage, image value 2
    else:
        return False

def cancel():
    global escapevalue
    try:
        if checktrue() == False:
            #print("List updating!!!")
            if escapevalue == True:
                click(990,838)
            escapevalue = False 
            mainrunner()
    except IOError:
        print('raise exception')
        pass
set = 0
count = 0
def mainrunner():
    global count
    global set
    while count < 1000:
        if set == 0 and keyboard.is_pressed('`') or set ==1:
            if set == 0:
                print("Let's get started boys!!!")
            set=1
            count+=1
            while set == 1:
                gettingimage()
                gc.collect()#THISHSISHTIS
                #time.sleep(1)
                cancel()
                xxx = detectingheroic()
                xxy = hindering()
                cancel()       
                #throwingimage2()    
                condition(xxy,xxx)        
                # if this cancel found out a weird value, click a randomplace to close buying option       
                throwingimage2()
                #click confirmed
                    #gettingimage()
                #create uncheck image class to see if it's differentto value reading 2
#FUCTIONNNNNN
def main():
    global count    
    while True:
    #hindering()
        mainrunner()
        count = 0

if __name__ == "__main__":
    main()
