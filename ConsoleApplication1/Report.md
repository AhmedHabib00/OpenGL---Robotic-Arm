Name: Ahmed Mohamed Yehia Habib
Code: 1170323

The most challenging part was the coordination in the rotation between the fingers as I had a problem with the offset in the y-axis or the x-axis 
so I had to put every finger with its rotation function in a stack for it so that they are all coordinated. 
""" 
  glPushMatrix();
    glTranslatef(1.0, 0.0, 0.0);
    glRotatef((GLfloat)fingerBase, 0.0, 0.0, 1.0);
    glTranslatef(0.15, 0.0, 0.0);
    glPushMatrix();
    glScalef(0.3, 0.1, 0.1);
    glutWireCube(1);
    glPopMatrix();

    //Draw finger flang 1 
    glPushMatrix();
    glTranslatef(0.15, 0.0, 0.0);
    glRotatef((GLfloat)fingerUp, 0.0, 0.0, 1.0);
    glTranslatef(0.15, 0.0, 0.0);
    glScalef(0.3, 0.1, 0.1);
    glutWireCube(1);
    glPopMatrix();

    glPopMatrix();
    
"""

The other challenge was to set a limit for the fingers to move to be as realistic as possible, so i put limits in if conditions when I click the 
button that's supposed to move the fingers/rotate them so that the fingertips don't go up and only be able to move down until they hit the palm and
the other fingers  can go up and down to a certain limit as well as the elbow itself that doesn't go down and only up


"""
 case 'F':
        if (fingerBase < 50)
        {
            fingerBase = (fingerBase + 5) % 360;
        }

        glutPostRedisplay();
        break;
    case 'g':
        if (fingerUp > -150)
        {
            fingerUp = (fingerUp - 5) % 360;
        }
"""

I had some help from Omar Abo el Fadl regarding the limits