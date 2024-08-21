# et_lab
6-1
clc;clear all; close all;
theta=0:0.05*pi:2*pi;
El=cos((pi/2)*cos(theta));
polar(theta,abs(El)/max(El));
title('radiation pattern ofthe antenna');
figure;
plot(theta.*180/pi, abs(El));
xlabel('angle(in degrees)');
ylabel('absolute gain');
grid on
title('gain of radiation pattern');

6-2

clc;clear all; close all;
theta=0:0.05*pi:2*pi;
El=cos((pi/2)*cos(theta)+(pi/2));
polar(theta,abs(El)/max(El));
title('radiation pattern ofthe antenna');
figure;
plot(theta.*180/pi, abs(El));
xlabel('angle(in degrees)');
ylabel('absolute gain');
grid on
title('gain of radiation pattern');

6-3

clc;clear all; close all;
theta=0:0.05*pi:2*pi;
El=cos((pi/4)*cos(theta)+(pi/4));
polar(theta,abs(El)/max(El));
title('radiation pattern ofthe antenna');
figure;
plot(theta.*180/pi, abs(El));
xlabel('angle(in degrees)');
ylabel('absolute gain');
grid on
title('gain of radiation pattern');

6-4(broadside)

clc; clear all; close all;
n =6;
del =0;
theta=0:0.01*pi:2*pi;
psi =(pi*cos(theta))+del;
El=(sin(n*psi/2))./(sin(psi/2));
polar(theta,abs(El));
title('radiation pattern ofthe antenna');
figure;
plot(theta.*180/pi, abs(El));
xlabel('angle(in degrees)');
ylabel('absolute gain');
grid on
title('gain of radiation pattern');

6-4(end fire)

clc; clear all; close all;
n =4;
del =-pi;
theta=0:0.01*pi:2*pi;
psi =(pi*cos(theta))+del;
El=(sin(n*psi/2))./(sin(psi/2));
polar(theta,abs(El));
title('radiation pattern ofthe antenna');
figure;
plot(theta.*180/pi, abs(El));
xlabel('angle(in degrees)');
ylabel('absolute gain');
grid on
title('gain of radiation pattern');

7th

clc;close all;clear all;
theta=0:0.01:2*pi;
L=input('Enter the value of L:');
e=(cos(pi*L*cos(theta))-cos(pi*L))./sin(theta);
subplot(1,2,1);
polar(theta,abs(e)/max(e));
title('Radiation pattern of antenna');
subplot(1,2,2);
plot(theta.*180/pi,abs(e));
xlabel('Angle in degrees');
ylabel('Absolute gain');
grid on
title('Radiation pattern');


#Backup codes

clc; close all; clear all;
phi=0:0.005*pi:2*pi;

dr=pi/2;
delta=input('enter the initial phase value');
n=input('enter the no of point sources');
psi=abs(dr*cos(phi)+delta);
E=abs((sin(n.*psi/2)./sin(psi/2)));
polar(phi,E);
title('radiation pattern');
figure;
plot(phi.*180/pi,E);
xlabel('angle in degrees');
ylabel('absolute gain');
grid on;
title("gain of radiation pattern");


clc; close all; clear all;
pi=3.142;
l=1;
phi=0:0.005*pi:2*pi;
b=(2*pi)/l;
d=l/2;
dr=b*d;
delta=input('enter the initial phase value');
n=input('enter the no of point sources');
psi=(dr*cos(phi)-delta);
E=abs(((sin(n.*psi/2)./sin(psi/2)))/n);
polar(phi,abs(E)/max(E));
title('radiation pattern');
figure;
plot(phi.*180/pi,E);
xlabel('angle in degrees');
ylabel('absolute gain');
grid on;

