# projetolop9n3
//etapa9
var xif=380
var yif=200
var tela=1
var xin2=[]
var yin2=[]
var qtdObjetosn2=10
var vidas=5
var pontos=0
var nivel=1
var vxi=[]
var vyi=[]
var qtdObjetos=10
var raioO=15
var raioP=10
var x=10
var y=200
var xd
var yd
var bpontos=9
var estadoDisparo = false;
var raioD=3
function setup() {
  createCanvas(500, 400);
  for(i=0;i<=qtdObjetos;i++){
  vxi[i]=random(250,400)
  vyi[i]=random(50,400) 
}
   for(i=1;i<qtdObjetosn2;i++){
     xin2[i]=random(50,400)
  yin2[i]=random(50,400)}
}
  function draw() {
 if(tela == 1){
    background(150)
   textSize(39);
text('Bem vindo ao jogo,jogador!',10,50);
  textSize(13)
  text('No nivel 1 o objetivo do jogo é eliminar todos os alvos antes que eles cheguem\n do outro lado da tela. ',10,100);
  text('No nivel 2 o objetivo é apenas chegar ao outro lado.',10,170)
  text('Aperte ENTER para ir ao inicio do jogo.',10,260)
   text('Voce pode atirar usando CTRL e se movimentar usando as setas do teclado.\n boa sorte.',10,330)
  if ( keyIsDown(ENTER) ){
    tela=2;
  }
}


if(tela==2){
  background(100);
   textSize(19);
  text('vidas: '+vidas,10,30);
  text('nivel: '+nivel,200,30)
  text('pontos:  '+pontos,300,30)
  for(i=1;i<=qtdObjetos;i++){
  ellipse(vxi[i],vyi[i],2*raioO,2*raioO)
  }
  ellipse(x,y,2*raioP,2*raioP)
   if ( keyIsDown(RIGHT_ARROW) )
  {
    x=x+4
  }
   if ( keyIsDown(LEFT_ARROW) )
  {
    x=x-4
  }
  if ( keyIsDown(UP_ARROW) )
  {
    y=y-4
  }
    if ( keyIsDown(DOWN_ARROW) )
  {
    y=y+4
  }
    ellipse(xd,yd,1*raioD,1*raioD)
  if ( keyIsDown(CONTROL) && ! estadoDisparo)
  {
    xd=x
    yd=y
    estadoDisparo = true;
  }

if( estadoDisparo ) {
  ellipse(xd,yd,1*raioD,1*raioD)
  xd=xd+10;
}
  if(xd > 400)
  {
    estadoDisparo=false
  }
  if(x!=10 || y!=200){
  vxi[1]=vxi[1]-1}
   if(x!=10 || y!=200){
  vxi[2]=vxi[2]-1}
   if(x!=10 || y!=200){
  vxi[3]=vxi[3]-1}
   if(x!=10 || y!=200){
  vxi[4]=vxi[4]-1}
   if(x!=10 || y!=200){
  vxi[5]=vxi[5]-1}
   if(x!=10 || y!=200){
  vxi[6]=vxi[6]-1}
   if(x!=10 || y!=200){
  vxi[7]=vxi[7]-1}
   if(x!=10 || y!=200){
  vxi[8]=vxi[8]-1}
   if(x!=10 || y!=200){
  vxi[9]=vxi[9]-1}
   if(x!=10 || y!=200){
  vxi[10]=vxi[10]-1}
 
  if(dist(x,y,vxi[1],vyi[1])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,vxi[2],vyi[2])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
   if(dist(x,y,vxi[3],vyi[3])< raioO + raioP)
  {
    x=10
    y=200
    vidas=vidas-1
  }
    if(dist(x,y,vxi[4],vyi[4])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
     if(dist(x,y,vxi[5],vyi[5])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
       if(dist(x,y,vxi[6],vyi[6])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
       if(dist(x,y,vxi[7],vyi[7])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
       if(dist(x,y,vxi[8],vyi[8])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
      if(dist(x,y,vxi[9],vyi[9])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
     if(dist(x,y,vxi[10],vyi[10])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
    if(dist(xd,yd,vxi[1],vyi[1])< raioO + raioD)
  {
    vxi[1]=1000
       vyi[1]=100

      pontos=pontos+1
  }
  if(dist(xd,yd,vxi[2],vyi[2])< raioO + raioD)
  {
   vxi[2]=1000
       vyi[2]=1000
      pontos=pontos+1
  }
   if(dist(xd,yd,vxi[3],vyi[3])< raioO + raioD)
  {
   vxi[3]=1000
       vyi[3]=1000
      pontos=pontos+1
  }
    if(dist(xd,yd,vxi[4],vyi[4])< raioO + raioD)
  {
    vxi[4]=1000
       vyi[4]=1000
      pontos=pontos+1
  }
     if(dist(xd,yd,vxi[5],vyi[5])< raioO + raioD)
  {
   vxi[5]=1000
       vyi[5]=1000
      pontos=pontos+1
  }
       if(dist(xd,yd,vxi[6],vyi[6])< raioO + raioD)
  {
   vxi[6]=1000
       vyi[6]=1000
      pontos=pontos+1
  }
       if(dist(xd,yd,vxi[7],vyi[7])< raioO + raioD)
  {
   vxi[7]=1000
       vyi[7]=1000
      pontos=pontos+1
  }
       if(dist(xd,yd,vxi[8],vyi[8])< raioO + raioD)
  {
    vxi[8]=1000
       vyi[8]=1000
      pontos=pontos+1
  }
      if(dist(xd,yd,vxi[9],vyi[9])< raioO + raioD)
  {
  vxi[9]=1000
       vyi[9]=1000
      pontos=pontos+1
  }
     if(dist(xd,yd,vxi[10],vyi[10])< raioO + raioD)
  {
       vxi[10]=1000
       vyi[10]=1000
      pontos=pontos+1
  }
 if(pontos>bpontos){
    nivel=2;
    bpontos==bpontos+10 ;
   raioO=0
   
   for(i=1;i<qtdObjetosn2;i++){
     ellipse(xin2[i],yin2[i],20,20)}
   yin2[1]=yin2[1]-13
    yin2[2]=yin2[2]-3
     yin2[3]=yin2[3]-8
      yin2[4]=yin2[4]-5
       yin2[5]=yin2[5]-3
        yin2[6]=yin2[6]-13
         yin2[7]=yin2[7]-4
          yin2[8]=yin2[8]-8
           yin2[9]=yin2[9]-4
            yin2[10]=yin2[10]-3
   if(yin2[1]<50){
     yin2[1]=400}
     if(yin2[1]<50){
     yin2[1]=400}
     if(yin2[2]<50){
     yin2[2]=400}
     if(yin2[3]<50){
     yin2[3]=400}
     if(yin2[4]<50){
     yin2[4]=400}
     if(yin2[5]<50){
     yin2[5]=400}
     if(yin2[6]<50){
     yin2[6]=400}
     if(yin2[7]<50){
     yin2[7]=400}
     if(yin2[8]<50){
     yin2[8]=400}
     if(yin2[9]<50){
     yin2[9]=400}
     if(yin2[10]<50){
     yin2[10]=400}
     if(dist(x,y,xin2[1],yin2[1])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[2],yin2[2])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[3],yin2[3])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[4],yin2[4])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[5],yin2[5])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[6],yin2[6])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[7],yin2[7])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[8],yin2[8])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[9],yin2[9])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,xin2[10],yin2[10])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
   if(vidas<=0){
     tela=3;
}
if(x>400){
tela=4
  y=200
  x=10;}
 }
 }
  
 
if(tela==3 || vxi[1]<0 || vxi[2]<0 || vxi[3]<0 || vxi[4]<0 || vxi[5]<0 || vxi[6]<0 || vxi[7]<0 || vxi[8]<0 || vxi[9]<0 || vxi[10]<0){
      background(150)
  textSize(30);
  text('Você perdeu,tente novamente. ',50,200);
  }
  
if(tela==4){
  nivel=3
background(20)
  textSize(20)
  fill(200)
  text('vidas:'+vidas,10,15)
  text('nivel:'+nivel,10,30)
  ellipse(x,y,2*raioP,2*raioP)
   if ( keyIsDown(RIGHT_ARROW) )
  {
    x=x+4
  }
   if ( keyIsDown(LEFT_ARROW) )
  {
    x=x-4
  }
  if ( keyIsDown(UP_ARROW) )
  {
    y=y-4
  }
    if ( keyIsDown(DOWN_ARROW) )
  {
    y=y+4
  }
   if ( keyIsDown(CONTROL) && ! estadoDisparo)
  {
    xd=x
    yd=y
    estadoDisparo = true;
  }

if( estadoDisparo ) {
  ellipse(xd,yd,1*raioD,1*raioD)
  xd=xd+10;
}
  if(xd > 400)
  {
    estadoDisparo=false
  }
  
ellipse(xif,yif,100,150)
if(x>20){
  yif=yif-4}
  if(yif>390){
    yif=yif+4}
  if(yif<20){
    yif=yif-4}
}
}
