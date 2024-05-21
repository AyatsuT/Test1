#!/usr/bin/env python
# coding: utf-8

# ## Classes

# In[6]:


class Dog:
    def __init__(self, name):
        self.name = name
        self.legs = 4
    
    def speak(self):
        print(self.name + ' says: Bark!')
        


# In[7]:


my_dog = Dog('Rover')
another_dog = Dog('Fluffy')


# In[8]:


my_dog.speak()


# In[9]:


another_dog.speak()


# In[ ]:


#NOTHING ---------------------------------------------------------------------------------


# In[78]:


import os 
import random
from IPython.display import clear_output

class Pokemon:
    def __init__(self,name,hp,atk,dfd,skill1,skl1_dmg,skill2,skl2_dmg,skill3,skl3_dmg,skill4,skl4_dmg):
        self.name = name
        self.hp = hp
        self.atk = atk
        self.dfd = dfd
        self.skill1 = skill1
        self.skl1_dmg = skl1_dmg
        self.skill2 = skill2
        self.skl2_dmg = skl2_dmg
        self.skill3 = skill3
        self.skl3_dmg = skl3_dmg
        self.skill4 = skill4
        self.skl4_dmg = skl4_dmg
    
    def status(self):
        print(self.name + "'s remaining hp is", self.hp)


# In[91]:


pokemon1 = Pokemon('ヒノアラシ',146,18,10,'すてみタックル',120,'ひのこ',40,'ころがる',30,'まるくなる',0)
pokemon1.max_hp = 146
#marukunaru:defend up+korogaru dmgx2
#sutemitackle:120dmg+jibun 33%
#ころがる:5 always use the same skill for 5 turns, dmg starts from 30,60,90,120... accuracy 90%

pokemon2 = Pokemon('ルカリオ',600,30,10,'ボーンラッシュ',25,'まもる',0,'つるぎのまい',0,'はっけい',60)
pokemon2.max_hp = 177
#bonerush:(2-6)x25
#mamoru:0 dmg


# 

# In[94]:


#add any additional skill info here
#pokemon1.skill1
pokemon1.skl1_side_effect = 40
#pokemon1.skill3
#while a<=5:
a = 1
b = 30
    #pokemon1.skl3_dmg = pokemon1.skl3_dmg*a
    #a = a+1

x = 1

while True:
    #pokemon1_turn
    print()
    print('----------------------------------TURN', x,'----------------------------------')

    print(pokemon1.name, "'s HP:",pokemon1.hp,'/',pokemon1.max_hp) 
    print(pokemon1.hp * '|')
    print(pokemon2.name, "'s HP:",pokemon2.hp,'/',pokemon2.max_hp)
    print(pokemon2.hp * '|')
    print()

    #skill3 loop
    if 1<a<=5 :
        print('----------------------------------',pokemon1.name + "の番です.----------------------------------")
        print(pokemon1.name, 'used', pokemon1.skill3)
        pokemon1.skl3_dmg = b*a
        pokemon2.hp -= pokemon1.skl3_dmg - pokemon2.dfd
        print(pokemon1.name, 'dealt', (pokemon1.skl3_dmg-pokemon2.dfd), 'damage to', pokemon2.name)
        print("remaining ", pokemon2.name, "'s hp is", pokemon2.hp, '!')
        a = a+1
        print()
        print()
        
        if pokemon2.hp <= 0 :
            print(pokemon1.name, 'win!')
            break    
    
    if a>6 or a==1 :    
        print('----------------------------------',pokemon1.name + "の番です.----------------------------------")
        print('Select your move:')
        print('1. Normal Attack')
        print('2. Skill')
        print('3. Item')
        print('4. Run')
        choice = input('enter your choice:  ')
    
    
    
        if choice == '1' :
            pokemon2.hp -= pokemon1.atk-pokemon2.dfd
            print(pokemon1.name, 'dealt', (pokemon1.atk-pokemon2.dfd), 'damage to', pokemon2.name)
            print("remaining ", pokemon2.name, "'s hp is", pokemon2.hp, '!')
            print()
            
            if pokemon2.hp <= 0 :
                print(pokemon1.name, 'win!')
                break    
                
        #skill_description.....................................................................................
        if choice == '2':
            #pokemon1.skl_dmg = random.randint(10,30)
            #skl1_dmg = pokemon1.skl1_dmg
            print('Choose skill:')
            print('A.',pokemon1.skill1)
            print('B.',pokemon1.skill2)
            print('C.',pokemon1.skill3)
            print('D.',pokemon1.skill4)
            choice = input('enter your choice:  ')
            if choice == 'A':
                pokemon2.hp -= pokemon1.skl1_dmg - pokemon2.dfd
                print(pokemon1.name, 'used', pokemon1.skill1)
                print(pokemon1.name, 'dealt', (pokemon1.skl1_dmg-pokemon2.dfd), 'damage to', pokemon2.name)
                print("remaining ", pokemon2.name, "'s hp is", pokemon2.hp, '!')
                print('...but!')
                #need to work here
        
                #side_effect.........................................................
                pokemon1.hp -= pokemon1.skl1_side_effect
                print(pokemon1.name,'got hurt by using',pokemon1.skill1)
                print("remaining ", pokemon1.name, "'s hp is", pokemon1.hp, '!')
                print()
                

            if choice == 'B':
                pokemon2.hp -= pokemon1.skl2_dmg - pokemon2.dfd
                print(pokemon1.name, 'used', pokemon1.skill2)
                print(pokemon1.name, 'dealt', (pokemon1.skl2_dmg-pokemon2.dfd), 'damage to', pokemon2.name)
                print("remaining ", pokemon2.name, "'s hp is", pokemon2.hp, '!')
    
            if choice == 'C':
                a=1
                print(pokemon1.name, 'used', pokemon1.skill3)
                pokemon1.skl3_dmg = b*a
                pokemon2.hp -= pokemon1.skl3_dmg-pokemon2.dfd
                print(pokemon1.name, 'dealt', (pokemon1.skl3_dmg-pokemon2.dfd), 'damage to', pokemon2.name)
                print("remaining ", pokemon2.name, "'s hp is", pokemon2.hp, '!')
                a = a+1
                print()

            if choice == 'D':
                print(pokemon1.name, 'used',pokemon1.skill4)
                pokemon1.dfd = pokemon1.dfd*2
                print(pokemon1.name,'Def has raised.')
                b = b*2
                print(pokemon1.name,'has charged up!')
    
                
            
            #pokemon2.hp -= pokemon1.skl1_dmg
            #print(pokemon1.name, 'Used', pokemon1.skill1)
            #print(pokemon1.name, 'dealt', pokemon1.skl1_dmg, 'damage to', pokemon2.name)
            #print("remaining ", pokemon2.name, "'s hp is", pokemon2.hp, '!')
            
            
            if pokemon2.hp <= 0 :
                print(pokemon1.name, 'win!')
                break
        
        if choice == '3':
            heal_amount = 20
            pokemon1.hp = min(pokemon1.hp + heal_amount, pokemon1.max_hp)
            print(pokemon1.name, 'Used Small Potion')
            print("remaining ", pokemon1.name, "'s hp is", pokemon1.hp, '!')
            print()
            
        elif choice == '4' :
            print(pokemon1.name, 'Run away.')
            print()
            break
    print('..................................End Turn....................................')
    
    #pokemon2 turn
    if pokemon1.hp <= 0 :
                    print(pokemon2.name, 'win!')
                    break
        
    print(pokemon1.name, "'s HP:",pokemon1.hp,'/',pokemon1.max_hp) 
    print(pokemon1.hp * '|')
    print(pokemon2.name, "'s HP:",pokemon2.hp,'/',pokemon2.max_hp)
    print(pokemon2.hp * '|')
    print()

    print('----------------------------------',pokemon2.name + "の番です.----------------------------------")
    print('Select your move:')
    print('1. Normal Attack')
    print('2. Skill')
    print('3. Item')
    print('4. Run')
    choice = input('enter your choice:  ')

    if choice == '1' :
        pokemon1.hp -= pokemon2.atk-pokemon1.dfd
        print(pokemon2.name, 'dealt', (pokemon2.atk-pokemon1.dfd), 'damage to', pokemon1.name)
        print("remaining ", pokemon1.name, "'s hp is", pokemon1.hp, '!')
        print('..................................End Turn....................................')
        print()
        x = x+1

        if pokemon1.hp <= 0 :
            print(pokemon2.name, 'win!')
            break

    if choice == '2':
            #pokemon1.skl_dmg = random.randint(10,30)
            #skl1_dmg = pokemon1.skl1_dmg
            print('Choose skill:')
            print('A.',pokemon2.skill1)
            print('B.',pokemon2.skill2)
            print('C.',pokemon2.skill3)
            print('D.',pokemon2.skill4)
            choice = input('enter your choice:  ')
            if choice == 'A':
                no_hits = (random.randint(2,6))
                pokemon1.hp -= (pokemon2.skl1_dmg*no_hits) - pokemon1.dfd
                print(pokemon2.name, 'used', pokemon2.skill1)
                print(pokemon2.name, 'hits', no_hits,'times')
                print(pokemon2.name,'dealt',(pokemon2.skl1_dmg*no_hits-pokemon2.dfd),'damage to',pokemon1.name)
                print("remaining ", pokemon1.name, "'s hp is", pokemon1.hp, '!')
            

    elif choice == '4' :
        print(pokemon2.name, 'Run away.')
        break
            
    elif choice == 'End' :
        print('good game!')
        break


# In[5]:


skl_dmg = random.randint(10,50)
print(skl_dmg)


# In[ ]:




