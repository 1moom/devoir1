# devoir1
"""
>>> (len ('charge_image'))
12
"""
import pygame

HEIGHT = 16
WIDTH = 24


pygame.init()
window = pygame.display.set_mode((36 * WIDTH, 36 * HEIGHT))
window.fill((255, 255, 255))
run = True

import os

 # Module os de python - Qui permet a Python de communiquer avec Windows
                    # Systeme de fichier de Windows est accessible a travers le module
print(os.getcwd())  # getcwd = get current working directory, autrement dit, la ou s'execute votre programme


carte = """.....#...........
#..##........#.#......######
#..............###....######
################........####
#..........#....###....#####
###.....#...#...##########..
#...##.....#..##############


# def charge_image():
image=pygame.image.load("ressources/tuiles.png").convert(0)
   width, height =image.get_size()
   tuiles = []
   for x in range(width//WIDTH):
      ligne = []
      for y in range(height//HEIGHT):
         rect = ( x * WIDTH, y * HEIGHT, WIDTH, HEIGHT)
         ligne.append(image.subsurface(rect))
         tuiles.append(ligne)
   return tuiles

    with open("Ressources/tuiles.png","r") as f :
    print("pavgame")
    while run:
      for event in pygame.event.get():
        if event.type == pygame.QUIT:
            run = False

      tuiles=charge_image()
      lignes=carte.split("/n")
      for i, ligne in enumerate(lignes):     #ordonnees(ligne)
        for j, tuile in enumerate(ligne):      #abscisses(ligne)
          if tuile =='#':
            window.blit(tuiles[0][0],(WIDTH*j,HEIGHT*i))
          if tuile =='#':
            window.blit(tuiles[0][2],(WIDTH*j,HEIGHT*i))

      pygame.display.flip()
      pygame.quit()
               # for x, ligne in enumerate(charge_image()):
              #for y, tuile in enumerate(ligne):
               #  tuile =Pygame.transform.scale(tuile, (WIDTH * 8, HEIGHT * 8))
                #window.blit(tuile, (x * (WIDTH * 9), y * (HEIGHT* 9)))



    
    #On va creer un encodage pour representer une vue de la carte que l'on souhaite afficher
    # Codec
    #.= terrain libre
    ## =mur
    # carte de taille 16*16 -chaque case fait 24 pixel par 16
    # 16*24 par 16*16=385*256
    # lignes= carte.split("/n")
    # for i,ligne in enumerate(lignes)
    # for j,point in enumerate(ligne)
    #  pygame.display.flip()
 """#pygame.quit()
