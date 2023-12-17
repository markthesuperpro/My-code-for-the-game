import sys #1
#https://www.pygame.org/ftp/contrib/pygame_docs.pdf
import pygame #1
from pygame.locals import * #1
import random

pygame.init() #1
DISPLAYSURF = pygame.display.set_mode((700, 700)) #1
pygame.display.set_caption('Game') #1

enemy_p1 = (random.randint(0,700),random.randint(0,700))
enemy_p2 = (random.randint(0,700),random.randint(0,700))

while True: #1
    pygame.display.flip() #1
    for event in pygame.event.get(): #1
         if event.type == QUIT: #1
           pygame.quit() #1
           sys.exit() #1
         if event.type == MOUSEBUTTONUP: #1
           x,y = event.pos #1
           pos = (x,y) #1
    DISPLAYSURF.fill((0, 0, 0)) #1
    rect = pygame.Rect((30,30,30,30)) #1

    enemy_1 = pygame.Rect((30,30,30,30))
    enemy_2 = pygame.Rect((30,30,30,30))
    
    enemy_x1 = enemy_p1[0] + random.choice([ int((random.choice(["-",""])) + str(random.randint(0,20))) , 0])
    enemy_y1 = enemy_p1[1] + random.choice([ int((random.choice(["-",""])) + str(random.randint(0,20))) , 0])
    enemy_x2 = enemy_p2[0] + random.choice([ int((random.choice(["-",""])) + str(random.randint(0,20))) , 0])
    enemy_y2 = enemy_p2[1] + random.choice([ int((random.choice(["-",""])) + str(random.randint(0,20))) , 0])

    if enemy_x1 < 0:
      enemy_x1 = 0
    if enemy_y1 < 0:
      enemy_y1 = 0
    if enemy_x1 > 700:
      enemy_x1 = 670
    if enemy_y1 > 700:
      enemy_y1 = 670
    
    if enemy_x2 < 0:
      enemy_x2 = 0
    if enemy_y2 < 0:
      enemy_y2 = 0
    if enemy_x2 > 700:
      enemy_x2 = 670
    if enemy_y2 > 700:
      enemy_y2 = 670

    enemy_p1 = (enemy_x1,enemy_y1)
    enemy_p2 = (enemy_x2,enemy_y2)
    enemy_1.center = enemy_p1
    enemy_2.center = enemy_p2
    pygame.draw.rect(DISPLAYSURF, "red",enemy_1, width=0)
    pygame.draw.rect(DISPLAYSURF, "red",enemy_2, width=0)
    
    try: #1
      rect.center=pos #1
    except NameError: #1
      rect.center=0,0 #1
    pygame.draw.rect(DISPLAYSURF, "blue",rect, width=0) #1
    pygame.display.update() #1
