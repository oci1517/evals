###########
Module 2 : récursion, listes, slicing, boucles, conditions, événements, programmation fonctionnelle, callbacks
###########

Question 1
==========

Question 2
==========

..  admonition:: Corrigé
    :class: warning
    
    ..  comment-code-block:: python
    
        chaine = 'Python'

        expressions = [
            "chaine[2:6]",
            "chaine[1:4]",
            "chaine[3:]",
            "chaine[:4]",
            "chaine[-4:-1]",
            "chaine[-1:-4]",
            "chaine[::-2]",
            "chaine[:3] + chaine[3:]"
        ]
        
        for e in expressions:
            print(e, "==>", "'"+eval(e)+"'")
            
    Sortie :
    
    ::
    
        chaine[2:6] ==> 'thon'
        chaine[1:4] ==> 'yth'
        chaine[3:] ==> 'hon'
        chaine[:4] ==> 'Pyth'
        chaine[-4:-1] ==> 'tho'
        chaine[-1:-4] ==> ''
        chaine[::-2] ==> 'nhy'
        chaine[:3] + chaine[3:] ==> 'Python'

Question 3
==========

salut les amis

Question 7
==========

..  admonition:: Corrigé
    :class: warning
    
    ..  code-block:: python

        def rotate1(liste, n):
            return liste[-n:] + liste[:-n]
        
        
        def rotate2(liste, n):
            rotation = [0] * len(liste)
            size = len(liste)
        
            for i in range(size):
                rotation[(i+n) % size] = liste[i]
        
            return rotation
        
        rotate = rotate1
        
        print(rotate([1,2,3,4,5], 1))
        print(rotate([1,2,3,4,5], -1))
        print(rotate([1,2,3,4,5], 2))
        
        
    Sortie :
    
    ::
    
        [5, 1, 2, 3, 4]
        [2, 3, 4, 5, 1]
        [4, 5, 1, 2, 3]