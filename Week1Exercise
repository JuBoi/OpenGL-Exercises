import pygame
import random
from pygame.locals import *

from OpenGL.GL import *
from OpenGL.GLU import *



def Square():
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT)
    #glColor3f(0.0, 0.0, 1.0)
    glBegin(GL_QUADS)
    glVertex2f(-1.0, -1.0)
    glVertex2f(-1.0, 1.0)
    glVertex2f(1.0, 1.0)
    glVertex2f(1.0, -1.0)
    glEnd()


def main():
    pygame.init()
    display = (800,600)
    pygame.display.set_mode(display, DOUBLEBUF|OPENGL)

    gluPerspective(45, (display[0]/display[1]), 0.1, 50.0)

    glTranslatef(0.0,0.0, -5)

    while True:
        glClear(GL_COLOR_BUFFER_BIT|GL_DEPTH_BUFFER_BIT)
        Square()
        pygame.display.flip()
        pygame.time.wait(10)
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
                quit()
            if event.type == pygame.KEYDOWN:
                if event.key == pygame.K_LEFT:
                    glTranslatef(-0.05, 0.0, 0.0)
                if event.key == pygame.K_RIGHT:
                    glTranslatef(0.05, 0.0, 0.0)
                if event.key == pygame.K_UP:
                    glTranslatef(0.0, 0.05, 0.0)
                if event.key == pygame.K_DOWN:
                    glTranslatef(0.0, -0.05, 0.0)
                if event.key == pygame.K_SPACE:
                    glColor3f(random.uniform(0.0, 1.0) , random.uniform(0.0, 1.0) , random.uniform(0.0, 1.0))
                    
        


main()
