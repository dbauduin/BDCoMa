# Traditional book example

Example of a traditional book made up of 3 pages with an animated transition between the second page and the third one:  
  
![Traditional sample](LeTueur.gif "Traditional sample")


## Source images

- [Cover.jpg](cover.jpg)
- [Page 1](0.jpg)
- [Page 2](1.jpg)
   - [Transition image 1](1-01.jpg)
   - [Transition image 2](1-02.jpg)
   - [Transition image 3](1-03.jpg)
   - [Transition image 4](1-04.jpg)
   - [Transition image 5](1-05.jpg)
   - [Transition image 6](1-06.jpg)
   - [Transition image 7](1-07.jpg)
   - [Transition image 8](1-08.jpg)
   - [Transition image 9](1-09.jpg)
   - [Transition image 10](1-10.jpg)
- [Page 3](2.jpg)


## Manifest

{  
    "@context": "https://readium.org/webpub-manifest/context.jsonld",  
  
    "metadata": {  
        "@type": "http://schema.org/Book",  
        "title": "Long feu (Extrait)",  
        "identifier": "urn:isbn:9782203057265",  
        "language": "fr",  
        "modificationDate": "2013-02-09T00:00:00Z",  
        "publicationDate": "2013-02-09T00:00:00Z",  
        "series": {  
            "name": "Le Tueur"  
        },  
        "contributors": {  
            "author": [  
                {  
                    "name": "Matz"  
                }  
            ],  
            "illustrator": [  
                {  
                    "name": "Luc Jacamon"  
                }  
            ]  
        },  
        "publisher": {  
            "name": "Casterman"  
        },  
        "readingProgression": "ltr",  
        "numberOfPages": 3,  
        "position": 0,  
        "description": "Long feu est l'autobiographie d'un tueur professionnel. Un homme solitaire et froid, méthodique et consciencieux, qui ne s'embarrasse pas de scrupules ni de regrets. Alors qu'il guette sa prochaine victime, nous partageons ses pensées, nous apprenons à le connaître, nous découvrons sa vie à travers de nombreux flash-back. Plus l'attente dure et plus il s'énerve, il nous entraîne dans des abîmes de violence, jusqu'à l'explosion finale. Mais les cartes seraient-elles truquées ? Gare aux éclaboussures...",  
        "cover": {  
            "href": "[cover.jpg](cover.jpg)",  
            "type": "image/jpeg",  
            "width": 1536,  
            "height": 2048  
        }  
    },  
  
    "spine": [  
        {  
            "href": "[0.jpg](0.jpg)",  
            "type": "image/jpeg",  
            "width": 1536,  
            "height": 2048,  
            "properties": {  
                "fragments": [  
                    {"width": 864, "height": 635, "x": 40, "y": 64},  
                    {"width": 291, "height": 632, "x": 916, "y": 67},  
                    {"width": 280, "height": 632, "x": 1220, "y": 68},  
                    {"width": 959, "height": 434, "x": 38, "y": 709},  
                    {"width": 493, "height": 435, "x": 1008, "y": 710},  
                    {"width": 355, "height": 547, "x": 38, "y": 1153},  
                    {"width": 1466, "height": 846, "x": 36, "y": 1152}  
                ]  
            }  
        },  
        {  
            "href": "[1.jpg](1.jpg)",  
            "type": "image/jpeg",  
            "width": 1536,  
            "height": 2048,  
            "properties": {  
                "transition-forward": {  
                    "effect": "images",  
                    "duration": 1500,  
                    "controllable": true,  
                    "resources": [  
                         {"href": "[1-01.jpg](1-01.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-02.jpg](1-02.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-03.jpg](1-03.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-04.jpg](1-04.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-05.jpg](1-05.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-06.jpg](1-06.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-07.jpg](1-07.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-08.jpg](1-08.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-09.jpg](1-09.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838},  
                         {"href": "[1-10.jpg](1-10.jpg)", "type": "image/jpeg", "width": 1475, "height": 1167, "x": 35, "y": 838}  
                    ]  
                },  
                "fragments": [  
                    {"width": 313, "height": 763, "x": 34, "y": 70},  
                    {"width": 151, "height": 761, "x": 353, "y": 70},  
                    {"width": 663, "height": 762, "x": 515, "y": 68},  
                    {"width": 313, "height": 761, "x": 1188, "y": 68},  
                    {"width": 1467, "height": 1163, "x": 38, "y": 839}  
                ]  
            }  
        },  
        {  
            "href": "[2.jpg](2.jpg)",  
            "type": "image/jpeg",  
            "width": 1536,  
            "height": 2048,  
            "properties": {  
                "fragments": [  
                    {"width": 1009, "height": 921, "x": 35, "y": 71},  
                    {"width": 446, "height": 926, "x": 1054, "y": 68},  
                    {"width": 1461, "height": 324, "x": 40, "y": 1003},  
                    {"width": 262, "height": 672, "x": 40, "y": 1338},  
                    {"width": 1190, "height": 669, "x": 310, "y": 1338}  
                ]  
            }  
        }  
    ],  
  
    "sections": [],  
  
    "renditions": [],  
  
    "resources": [],  
  
    "links": []  
}  