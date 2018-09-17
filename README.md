# BDCoMa

There are mainly 3 types of books:

Traditional (with eventually transition between pages)  |  Scrollable (with eventually parallax effects)  |  Turbomedia (animated slideshow)
:------------------------------------------------------:|:-----------------------------------------------:|:-------------------------------:
![Traditional sample](LeTueur.gif "Traditional sample") | ![Scrollable sample](BrothersBond2.gif "Scrollable sample") | ![Turbomedia sample](Overwatch.gif "Turbomedia sample")


Here is a suggestion of [**manifest specifications**](manifest.md), in relation with the [EDRLab Working group](https://github.com/edrlab/bd-comics-manga), and an illustration of the implementation for each of this book type.

## [Manifest](manifest.md)

{  
     "@context": "https://readium.org/webpub-manifest/context.jsonld",  

     "metadata": {  
          "@type": "*`http://schema.org/Book` for publication or `https://bib.schema.org/Chapter` for section.*",  
          "title": "*`Publication/Chapter title`*",  
          "identifier": "*`Unique identifier as a URI`*",  
          "language": "[@languageCode](manifest.md#languagecode)",  
          "modificationDate": "[@date](manifest.md#date)",  
          "publicationDate": "[@date](manifest.md#date)",  
          "series": {  
               "identifier": "*`Unique identifier as a URI`*"  
               "name": "*`Name of the serie`*"  
          },  
          "contributors": {  
               [@contributorType](manifest.md#contributortype): [  
                    {  
                         "identifier": "*`Unique identifier`*",  
                         "name": "*`Name of the entity (contributor or publisher), in the language of the publication`*",  
                         "translations": {  
                              "[@languageCode](manifest.md#languagecode)": "*`Name of the entity (contributor or publisher) in the language defined by the key`*"  
                         }  
                    }  
               ]  
          },  
          "publisher": {  
               "identifier": "*`Unique identifier`*",  
               "name": "*`Name of the entity (contributor or publisher), in the language of the publication`*",  
               "translations": {  
                    "[@languageCode](manifest.md#languagecode)": "*`Name of the entity (contributor or publisher) in the language defined by the key`*"  
               }  
          },  
          "readingProgression": [@readingProgression](manifest.md#readingprogression),  
          "numberOfPages": [@uint](manifest.md#uint),  
          "position": [@uint](manifest.md#uint),  
          "description": "*`Description of the publication/chapter`*",  
          "cover": {  
               "href": "*`Path to resource`*",  
               "type": "[@resourceType](manifest.md#resourcetype)",  
               "width": [@uint](manifest.md#uint),  
               "height": [@uint](manifest.md#uint)  
          }  
     },  

     "spine": [  
          {  
               "href": "*`Path to resource`*",  
               "type": [@resourceType](manifest.md#resourcetype),  
               "width": [@uint](manifest.md#uint),  
               "height": [@uint](manifest.md#uint),  
               "properties": {  
                    "fit": [@fitType](manifest.md#fittype),  
                    "position": [@positionMask](manifest.md#positionmask),  
                    "scrollable": [@boolean](manifest.md#boolean),  
                    [@transitionType](manifest.md#transitiontype): {  
                         "effect": "[@transitionEffect](manifest.md#transitioneffect)",  
                         "duration": [@duration](manifest.md#duration),  
                         "timing-function": [@timingFunction](manifest.md#timingfunction),  
                         "controllable": [@boolean](manifest.md#boolean),  
                         "unique": [@boolean](manifest.md#boolean),  
                         "resources": [  
                              {  
                                   "href": "*`Path to resource`*",  
                                   "type": [@resourceType](manifest.md#resourcetype),  
                                   "width": [@uint](manifest.md#uint),  
                                   "height": [@uint](manifest.md#uint),  
                                   "x": [@uint](manifest.md#uint),  
                                   "y": [@uint](manifest.md#uint),   
                                   "duration": [@duration](manifest.md#duration)  
                              }  
                         ]  
                    },  
                    "fragments": [  
                         {  
                              "width": [@uint](manifest.md#uint),  
                              "height": [@uint](manifest.md#uint),  
                              "x": [@uint](manifest.md#uint),  
                              "y": [@uint](manifest.md#uint),  
                              *`"type": ("panel", "text"...)`?*  
                         }  
                    ],  
                    "background": {  
                         "color": [@color](manifest.md#color),  
                         "gradient": {  
                              "type": [@gradientType](manifest.md#gradienttype),  
                              "start": {  
                                   "x": [@percentage](manifest.md#percentage),  
                                   "y": [@percentage](manifest.md#percentage)  
                              },  
                              "end": {  
                                   "x": [@percentage](manifest.md#percentage),  
                                   "y": [@percentage](manifest.md#percentage)  
                              },  
                              "colors": [  
                                   {  
                                        "color": [@color](manifest.md#color),  
                                        "location": [@percentage](manifest.md#percentage)  
                                   }  
                              ],  
                         }  
                    }  
               },  
               "layers": [  
                    {  
                         "width": [@uint](manifest.md#uint),  
                         "height": [@uint](manifest.md#uint),  
                         "speed": [@float](manifest.md#float),  
                         "opacity": [@percentage](manifest.md#percentage),  
                         "rotation": {  
                              "x": [@float](manifest.md#float),  
                              "y": [@float](manifest.md#float),  
                              "z": [@float](manifest.md#float)  
                         },  
                         "scale": {  
                              "x": [@ufloat](manifest.md#ufloat),  
                              "y": [@ufloat](manifest.md#ufloat)  
                         },  
                         "path": "[@path](manifest.md#path)",  
                         "resources": [  
                              {  
                                   "type": [@resourceType](manifest.md#resourcetype),  
                                   "href": "*`Path to resource`*",  
                                   "duration": [@duration](manifest.md#duration)  
                              }  
                         ],  
                         "background": {  
                              "color": [@color](manifest.md#color),  
                              "gradient": {  
                                   "type": [@gradientType](manifest.md#gradienttype),  
                                   "start": {  
                                        "x": [@percentage](manifest.md#percentage),  
                                        "y": [@percentage](manifest.md#percentage)  
                                   },  
                                   "end": {  
                                        "x": [@percentage](manifest.md#percentage),  
                                        "y": [@percentage](manifest.md#percentage)  
                                   },  
                                   "colors": [  
                                        {  
                                             "color": [@color](manifest.md#color),  
                                             "location": [@percentage](manifest.md#percentage)  
                                        }  
                                   ],  
                              }  
                         },  
                         "animations": [  
                              {  
                                   "start": [@uint](manifest.md#uint),  
                                   "duration": [@uint](manifest.md#uint),  
                                   "timing-function": [@timingFunction](manifest.md#timingfunction),  
                                   "sequence": [  
                                        {  
                                             "from": {  
                                                  [@animationProperty](manifest.md#animationproperty): *[`Defined by the corresponding property`](manifest.md#animationproperty)*  
                                             },  
                                             "to": {  
                                                  [@animationProperty](manifest.md#animationproperty): *[`Defined by the corresponding property`](manifest.md#animationproperty)*  
                                             },  
                                             "duration": [@duration](manifest.md#duration),  
                                             "timing-function": [@timingFunction](manifest.md#timingfunction)  
                                        }  
                                   ],  
                                   "loops": [@uint](manifest.md#uint)  
                              }  
                         ]  
                    }  
               ],  
               "cover": {  
                    "href": "*`Path to resource`*",  
                    "type": "[@resourceType](manifest.md#resourcetype)",  
                    "width": [@uint](manifest.md#uint),  
                    "height": [@uint](manifest.md#uint)  
               }  
          }  
     ],  

     "sections": [  
          [**@Section**](manifest.md#section)  
     ],  

     "renditions": [  
          [**@Rendition**](manifest.md#rendition)  
     ],  

     "resources": [],  

     "links": []  
}
