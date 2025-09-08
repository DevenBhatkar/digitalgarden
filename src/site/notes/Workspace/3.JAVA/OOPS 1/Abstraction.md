---
{"dg-publish":true,"permalink":"/workspace/3-java/oops-1/abstraction/","noteIcon":""}
---

- The process of displaying the things which are required and hiding the things which are not required is known as *abstraction*


### Concrete method

- A method which has body logic or implementation is known concrete method

### Concrete class 

- A class which has all the concrete method is known has *concrete class*


### Example:

```java
public class Driver {  
    public static void main(String[] args) {  
  
        System.out.println("main start");  
        Dhirubhai ref=new Dhirubhai();  
        ref.add(10,20);  
        System.out.println("Main End");  
    }  
}  
  
class Dhirubhai// concrete class  
{  
    //concrete method  
    public void add(int a ,int b)  
    {  
        int ans=a+b;  
        System.out.println(ans);  
    }  
}
```


### Abstract Method 

- A method which does not have body logic or implementation is known as *abstract method*

### How to create  a abstract Method

- Method must *Prefixed*  with Abstract keyword
- Method does not have body logic or implementation

### Abstract Class 

- A class which has abstract method is known as abstract class 
- If any class inherites abstracts method Then that inherited class also be an abstract class
- If we dont want to make the inherited class as abstract class then we need to override abstract method 

>Can we create Abstract class without abstract method ?
>	yes 
>Can we create Static method as Abstract method ?
>	No , because we cannot override static  method

### What are the members we can create in concrete class ?

<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="abstractionTableexcalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.12.2","elements":[{"id":"FP0g7AZF9b2giJx08mDoF","type":"arrow","x":-144.75,"y":-248.2421875,"width":85,"height":5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a0","roundness":{"type":2},"seed":1828319622,"version":152,"versionNonce":2138794118,"isDeleted":false,"boundElements":null,"updated":1756793583833,"link":null,"locked":false,"points":[[0,0],[85,-5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"wuXLagyNzNRl_avjneeNc","type":"line","x":-141.75,"y":-248.2421875,"width":2,"height":81,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a1","roundness":{"type":2},"seed":1907588870,"version":41,"versionNonce":1560243034,"isDeleted":false,"boundElements":null,"updated":1756793642766,"link":null,"locked":false,"points":[[0,0],[2,81]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"H8ndz7mqxe9FwYY8jIVvv","type":"arrow","x":-138.75,"y":-166.2421875,"width":85,"height":3,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a2","roundness":{"type":2},"seed":1399648282,"version":40,"versionNonce":1717083930,"isDeleted":false,"boundElements":null,"updated":1756793646671,"link":null,"locked":false,"points":[[0,0],[85,-3]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"g5TeBftfVTVwYRn3mO8Ta","type":"line","x":-217.75,"y":-205.2421875,"width":78,"height":2,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a3","roundness":{"type":2},"seed":993730714,"version":30,"versionNonce":287946714,"isDeleted":false,"boundElements":null,"updated":1756793653468,"link":null,"locked":false,"points":[[0,0],[78,-2]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"wl9__iNlqCPzy7Jy5Z-v6","type":"arrow","x":-143.33204090469982,"y":-83.20771611332896,"width":85,"height":5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a4","roundness":{"type":2},"seed":803997402,"version":180,"versionNonce":1813937754,"isDeleted":false,"boundElements":[],"updated":1756793670693,"link":null,"locked":false,"points":[[0,0],[85,-5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"q39vGSEoqUSLbhTrZ1gdg","type":"line","x":-140.33204090469982,"y":-83.20771611332896,"width":2,"height":81,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a5","roundness":{"type":2},"seed":1698306970,"version":69,"versionNonce":1932632858,"isDeleted":false,"boundElements":[],"updated":1756793670693,"link":null,"locked":false,"points":[[0,0],[2,81]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"MNrhjoDO0GqByQX5n1hCF","type":"arrow","x":-137.33204090469982,"y":-1.2077161133289565,"width":85,"height":3,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a6","roundness":{"type":2},"seed":426219610,"version":68,"versionNonce":503459802,"isDeleted":false,"boundElements":[],"updated":1756793670693,"link":null,"locked":false,"points":[[0,0],[85,-3]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"pRq-MPcFbh3PvN425_Se1","type":"line","x":-216.33204090469982,"y":-40.20771611332896,"width":78,"height":2,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a7","roundness":{"type":2},"seed":206011674,"version":58,"versionNonce":1621304474,"isDeleted":false,"boundElements":[],"updated":1756793670693,"link":null,"locked":false,"points":[[0,0],[78,-2]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"ytw7zF51u0bZadJ1my_k2","type":"arrow","x":-141.33204090469982,"y":62.79228388667104,"width":85,"height":5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a8","roundness":{"type":2},"seed":1964073370,"version":181,"versionNonce":375687258,"isDeleted":false,"boundElements":[],"updated":1756793678573,"link":null,"locked":false,"points":[[0,0],[85,-5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"vZKDaypo2v1MRsNKp56YN","type":"line","x":-138.33204090469982,"y":62.79228388667104,"width":2,"height":81,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a9","roundness":{"type":2},"seed":2053512794,"version":70,"versionNonce":1009151258,"isDeleted":false,"boundElements":[],"updated":1756793678573,"link":null,"locked":false,"points":[[0,0],[2,81]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"AXF5DEPP3lf4Ubr3Vjtqs","type":"arrow","x":-135.33204090469982,"y":144.79228388667104,"width":85,"height":3,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aA","roundness":{"type":2},"seed":394609434,"version":69,"versionNonce":1104001498,"isDeleted":false,"boundElements":[],"updated":1756793678573,"link":null,"locked":false,"points":[[0,0],[85,-3]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"vVhHclB2cDm9FJ2bgdaqP","type":"line","x":-214.33204090469982,"y":105.79228388667104,"width":78,"height":2,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aB","roundness":{"type":2},"seed":920768474,"version":111,"versionNonce":1450012314,"isDeleted":false,"boundElements":[],"updated":1756793678573,"link":null,"locked":false,"points":[[0,0],[78,-2]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"LhUi4nYQXOkW00idzM749","type":"arrow","x":-135.33204090469982,"y":220.79228388667104,"width":85,"height":5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aC","roundness":{"type":2},"seed":805217370,"version":176,"versionNonce":1828697370,"isDeleted":false,"boundElements":[],"updated":1756793683387,"link":null,"locked":false,"points":[[0,0],[85,-5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"Ns1yYYQJANRnvYEPgswdY","type":"line","x":-132.33204090469982,"y":220.79228388667104,"width":2,"height":81,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aD","roundness":{"type":2},"seed":1411189018,"version":65,"versionNonce":406716890,"isDeleted":false,"boundElements":[],"updated":1756793683387,"link":null,"locked":false,"points":[[0,0],[2,81]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"8fKEF_ZDRN-2IJLRCouuA","type":"arrow","x":-129.33204090469982,"y":302.79228388667104,"width":85,"height":3,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aE","roundness":{"type":2},"seed":1485886938,"version":64,"versionNonce":127186586,"isDeleted":false,"boundElements":[],"updated":1756793683387,"link":null,"locked":false,"points":[[0,0],[85,-3]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"tMb2raVf4j4aKszsQhvbR","type":"line","x":-208.33204090469982,"y":263.79228388667104,"width":78,"height":2,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aF","roundness":{"type":2},"seed":1584204442,"version":54,"versionNonce":1807143770,"isDeleted":false,"boundElements":[],"updated":1756793683387,"link":null,"locked":false,"points":[[0,0],[78,-2]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"kxNe3s2Q","type":"text","x":-366.75,"y":-224.2421875,"width":111.67188720703125,"height":33.00000000000001,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aH","roundness":null,"seed":742365594,"version":45,"versionNonce":30336666,"isDeleted":false,"boundElements":null,"updated":1756793715323,"link":null,"locked":false,"text":"Variables","rawText":"Variables","fontSize":26.400000000000002,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Variables","autoResize":true,"lineHeight":1.25},{"id":"LvPBBmnN","type":"text","x":-343.75,"y":-58.2421875,"width":98.68155517578124,"height":34,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aI","roundness":null,"seed":1634825434,"version":33,"versionNonce":1191462982,"isDeleted":false,"boundElements":null,"updated":1756793758588,"link":null,"locked":false,"text":"Method","rawText":"Method","fontSize":27.199999999999992,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Method","autoResize":true,"lineHeight":1.25},{"id":"2SpQ6XlI","type":"text","x":-316.75,"y":93.7578125,"width":65.45996093749997,"height":31.19520095310783,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aJ","roundness":null,"seed":1668431322,"version":40,"versionNonce":1210636038,"isDeleted":false,"boundElements":null,"updated":1756793752690,"link":null,"locked":false,"text":"Block","rawText":"Block","fontSize":24.956160762486267,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Block","autoResize":true,"lineHeight":1.25},{"id":"DoCeecAJ","type":"text","x":-385.75,"y":248.7578125,"width":156.75990295410156,"height":31.4123166262346,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aK","roundness":null,"seed":1521596570,"version":91,"versionNonce":715532698,"isDeleted":false,"boundElements":null,"updated":1756793746227,"link":null,"locked":false,"text":"Construction","rawText":"Construction","fontSize":25.12985330098768,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Construction","autoResize":true,"lineHeight":1.25},{"id":"yLEaXAZT","type":"text","x":-11.75,"y":-265.2421875,"width":129.7598876953125,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aL","roundness":null,"seed":1925817862,"version":17,"versionNonce":1656347142,"isDeleted":false,"boundElements":null,"updated":1756793770235,"link":null,"locked":false,"text":"Local variable","rawText":"Local variable","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Local variable","autoResize":true,"lineHeight":1.25},{"id":"yo0gswN1","type":"text","x":-19.75,"y":-171.2421875,"width":140.0198974609375,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aM","roundness":null,"seed":841191558,"version":18,"versionNonce":1404060614,"isDeleted":false,"boundElements":null,"updated":1756793780028,"link":null,"locked":false,"text":"Global variable","rawText":"Global variable","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Global variable","autoResize":true,"lineHeight":1.25},{"id":"jUq82In1","type":"text","x":-17.75,"y":-91.2421875,"width":167.19989013671875,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aN","roundness":null,"seed":1482328646,"version":30,"versionNonce":437070982,"isDeleted":false,"boundElements":null,"updated":1756793791909,"link":null,"locked":false,"text":"Abstract Method","rawText":"Abstract Method","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Abstract Method","autoResize":true,"lineHeight":1.25},{"id":"92OXxtqr","type":"text","x":-0.75,"y":-6.2421875,"width":166.11990356445312,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aO","roundness":null,"seed":497304326,"version":20,"versionNonce":196431046,"isDeleted":false,"boundElements":null,"updated":1756793799812,"link":null,"locked":false,"text":"Concrete Method","rawText":"Concrete Method","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Concrete Method","autoResize":true,"lineHeight":1.25},{"id":"ww0DNPRF","type":"text","x":-13.75,"y":56.7578125,"width":38.559967041015625,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aP","roundness":null,"seed":2003915590,"version":6,"versionNonce":1972799366,"isDeleted":false,"boundElements":null,"updated":1756793802809,"link":null,"locked":false,"text":"SIB","rawText":"SIB","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"SIB","autoResize":true,"lineHeight":1.25},{"id":"zUsWaAsF","type":"text","x":-7.75,"y":130.7578125,"width":37.01997375488281,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aQ","roundness":null,"seed":1154670086,"version":6,"versionNonce":921262662,"isDeleted":false,"boundElements":null,"updated":1756793806193,"link":null,"locked":false,"text":"IIB","rawText":"IIB","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"IIB","autoResize":true,"lineHeight":1.25},{"id":"PxxGnlQDHn4vGKxxPFVHw","type":"arrow","x":215.66795909530018,"y":-201.20771611332896,"width":85,"height":5,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aR","roundness":{"type":2},"seed":1111161094,"version":179,"versionNonce":939345606,"isDeleted":false,"boundElements":[],"updated":1756793817446,"link":null,"locked":false,"points":[[0,0],[85,-5]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"ft6FQBBRE3Xr7waCN5L0w","type":"line","x":218.66795909530018,"y":-201.20771611332896,"width":2,"height":81,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aS","roundness":{"type":2},"seed":1405216838,"version":68,"versionNonce":2138340870,"isDeleted":false,"boundElements":[],"updated":1756793817446,"link":null,"locked":false,"points":[[0,0],[2,81]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"7J4rkNdDNe-LxM9lDDoLM","type":"arrow","x":221.66795909530018,"y":-119.20771611332896,"width":85,"height":3,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aT","roundness":{"type":2},"seed":1294528390,"version":67,"versionNonce":428002630,"isDeleted":false,"boundElements":[],"updated":1756793817446,"link":null,"locked":false,"points":[[0,0],[85,-3]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"JmS_g7CKCCjfs6vYQdZ_F","type":"line","x":142.66795909530018,"y":-158.20771611332896,"width":78,"height":2,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aU","roundness":{"type":2},"seed":1789726406,"version":57,"versionNonce":1401238662,"isDeleted":false,"boundElements":[],"updated":1756793817446,"link":null,"locked":false,"points":[[0,0],[78,-2]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"PgRC7uAX","type":"text","x":344.25,"y":-209.2421875,"width":142.77987670898438,"height":25,"angle":0,"strokeColor":"#1971c2","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aV","roundness":null,"seed":2022111814,"version":19,"versionNonce":741290586,"isDeleted":false,"boundElements":null,"updated":1756793899676,"link":null,"locked":false,"text":"Static Variable","rawText":"Static Variable","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Static Variable","autoResize":true,"lineHeight":1.25},{"id":"l5tH4RoQ","type":"text","x":341.25,"y":-124.2421875,"width":184.99986267089844,"height":25,"angle":0,"strokeColor":"#1971c2","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aW","roundness":null,"seed":2107203418,"version":37,"versionNonce":1368670086,"isDeleted":false,"boundElements":null,"updated":1756793902361,"link":null,"locked":false,"text":"Non Static variable","rawText":"Non Static variable","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Non Static variable","autoResize":true,"lineHeight":1.25},{"id":"r8_jWf6lKIvBzTv8vD-rL","type":"arrow","x":180.25,"y":-71.2421875,"width":88,"height":0,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aX","roundness":{"type":2},"seed":792197722,"version":33,"versionNonce":319988806,"isDeleted":false,"boundElements":null,"updated":1756793849415,"link":null,"locked":false,"points":[[0,0],[88,0]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"A5XULWLJ","type":"text","x":299.25,"y":-78.2421875,"width":181.11990356445312,"height":25,"angle":0,"strokeColor":"#1971c2","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aZ","roundness":null,"seed":675057562,"version":21,"versionNonce":310401178,"isDeleted":false,"boundElements":null,"updated":1756793904607,"link":null,"locked":false,"text":"Non static method","rawText":"Non static method","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Non static method","autoResize":true,"lineHeight":1.25},{"id":"XqYYm0ua0HYZ5BrfwuxMP","type":"arrow","x":249.45930620493925,"y":-27.87146342112321,"width":77.78873038843254,"height":4.3731013678354245,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aa","roundness":{"type":2},"seed":1403890714,"version":229,"versionNonce":1115013082,"isDeleted":false,"boundElements":[],"updated":1756793872887,"link":null,"locked":false,"points":[[0,0],[77.78873038843254,-4.3731013678354245]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"dgWsRmTdEM9jQwSsJ8Arb","type":"line","x":252.20479080688392,"y":-27.87146342112321,"width":1.8303230679631186,"height":70.84424215893387,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"ab","roundness":{"type":2},"seed":68491482,"version":118,"versionNonce":1344582810,"isDeleted":false,"boundElements":[],"updated":1756793872887,"link":null,"locked":false,"points":[[0,0],[1.8303230679631186,70.84424215893387]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"g5KsPq8CJOb99kjZNF-b2","type":"arrow","x":254.9502754088286,"y":43.847399011377746,"width":77.78873038843254,"height":2.6238608207012546,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"ac","roundness":{"type":2},"seed":913370522,"version":117,"versionNonce":1570181466,"isDeleted":false,"boundElements":[],"updated":1756793872887,"link":null,"locked":false,"points":[[0,0],[77.78873038843254,-2.6238608207012546]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"S2OYUvqB6stouehqw9y2q","type":"line","x":182.65251422428545,"y":9.737208342261432,"width":71.38259965056163,"height":1.7492405471341697,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"ad","roundness":{"type":2},"seed":2146708058,"version":107,"versionNonce":1847580186,"isDeleted":false,"boundElements":[],"updated":1756793872887,"link":null,"locked":false,"points":[[0,0],[71.38259965056163,-1.7492405471341697]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null,"polygon":false},{"id":"rTdlxm7g","type":"text","x":366.25,"y":-37.2421875,"width":139.5399169921875,"height":25,"angle":0,"strokeColor":"#1971c2","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"ae","roundness":null,"seed":1474204762,"version":19,"versionNonce":1330505030,"isDeleted":false,"boundElements":null,"updated":1756793907629,"link":null,"locked":false,"text":"Static method","rawText":"Static method","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Static method","autoResize":true,"lineHeight":1.25},{"id":"Wd24TxUa","type":"text","x":363.25,"y":36.7578125,"width":180.57989501953125,"height":25,"angle":0,"strokeColor":"#1971c2","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"af","roundness":null,"seed":192775834,"version":21,"versionNonce":226502362,"isDeleted":false,"boundElements":null,"updated":1756793910471,"link":null,"locked":false,"text":"non Static method","rawText":"non Static method","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"non Static method","autoResize":true,"lineHeight":1.25},{"id":"9HQAMcke","type":"text","x":-280.75,"y":-113.2421875,"width":8,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aG","roundness":null,"seed":1275384070,"version":3,"versionNonce":542951302,"isDeleted":true,"boundElements":null,"updated":1756793665774,"link":null,"locked":false,"text":"","rawText":"","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"","autoResize":true,"lineHeight":1.25},{"id":"icg1Y4sE","type":"text","x":321.25,"y":-60.2421875,"width":8,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"aY","roundness":null,"seed":1513925786,"version":3,"versionNonce":1553583642,"isDeleted":true,"boundElements":null,"updated":1756793853286,"link":null,"locked":false,"text":"","rawText":"","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"","autoResize":true,"lineHeight":1.25}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1971c2","currentItemBackgroundColor":"transparent","currentItemFillStyle":"solid","currentItemStrokeWidth":2,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":5,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemArrowType":"round","scrollX":761.25,"scrollY":476.7578125,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":20,"gridStep":5,"gridModeEnabled":false,"gridColor":{"Bold":"rgba(217, 217, 217, 0.5)","Regular":"rgba(230, 230, 230, 0.5)"},"currentStrokeOptions":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true},"objectsSnapModeEnabled":false,"activeTool":{"type":"selection","customType":null,"locked":false,"fromSelection":false,"lastActiveTool":null}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("abstractionTableexcalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>



### What are the members we can create in abstract class ?

- In abstract class we can create *abstract Method * as well ass * concrete Method*
- Hence we cannot achive 100% abstraction using abstraction class 
- To achive 100 percent of abstraction we need `Interface`

```java
public class Driver {  
    public static void main(String[] args) {  
  
        System.out.println("main start");  
        System.out.println(Dhirubhai.a);  
        Dhirubhai.test();  
        //Dhirubhai ref=new Dhirubhai; Not possible  
        Dhirubhai ref=new Mukesh();  
        System.out.println(ref.b);  
        ref.demo();  
  
        System.out.println("Main End");  
  
    }  
}  
  
abstract class Dhirubhai// concrete class  
{  
    static int a=10;  
    int b=20;  
    public static void test()  
    {  
        System.out.println("Test Static Method");  
    }  
    public void demo()  
    {  
        System.out.println("demo non static method");  
    }  
      
    abstract public void abs();  
      
        static   
{  
            System.out.println("SIB");  
        }  
        {  
            System.out.println("IIB");   
        }  
          
        public Dhirubhai()  
        {  
            System.out.println("Dhirubhai Constructor");  
        }  
}  
class Mukesh extends Dhirubhai  
{  
    @Override  
    public void abs()  
    {  
        System.out.println("Abstract Method");  
    }  
}
```

### Output

```css
main start
SIB
10
Test Static Method
IIB
Dhirubhai Constructor
20
demo non static method
Main End
```


### 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/workspace/3-java/oops-1/interface/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

<div class="markdown-embed-title">

# Interface

</div>





### Type of Interface

1) Normal
- A interface which can contain one or more than one abstract method in known as , normal or regular interface
2) Marker Interface
- A interface which does not have any abstract method
3) Functional Interface
- A interface which has only one abstract method in known functional interface
- For functional interface we use *@functionalInterface* Annotation
- Runnable is a functional interface which has *run()* 


```java
//Write a java program to achive hybrid inheritance  
  
interface GrandFather  
{  
    int gf=10;  
}  
interface GrandMother  
{  
    int gm=20;  
}  
  
class Father implements GrandFather,GrandMother  
{  
    int f=30;  
}  
class Son extends Father  
{  
    int s=40;  
}  
class Daughter extends Father  
{  
    int d=50;  
}  
  
public class Demo {  
    public static void main(String[] args)  
    {  
       GrandFather grandFather =new Son();  
        System.out.println(grandFather.gf);  
          
        GrandMother grandMother=new Daughter();  
  
        System.out.println(grandMother.gm);  
          
          
  
  
    }  
}
```





</div></div>

