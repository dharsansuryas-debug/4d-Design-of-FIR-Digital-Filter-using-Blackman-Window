# FIR-FILTER-DESIGN
# EXP 4 d: Design-of-FIR-Digital-Filter-using-Blackman-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Blackman-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=Wc/%pi;
else
hd(n)=sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.42-(0.5*cos((2*%pi*(n-1))/(M-1)))+(0.08*cos((4*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR LPF using Blackman Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR LPF using Blackman Window');
```

# OUTPUT: 
<img width="727" height="580" alt="image" src="https://github.com/user-attachments/assets/b770ef89-c2fa-49b8-80f3-69298e12ab58" />


# RESULT: 

Thus design of low pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=1-Wc/%pi;
else
hd(n)=-sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.42-(0.5*cos((2*%pi*(n-1))/(M-1)))+(0.08*cos((4*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR HPF using Blackman Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR HPF using Blackman Window');
```

# OUTPUT: 
<img width="721" height="582" alt="image" src="https://github.com/user-attachments/assets/55ea9f99-cab6-4087-b4a0-8e3124ca1a52" />


# RESULT: 
Thus design of HIGH pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
Wc2=Wc(2);
Wc1=Wc(1);
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=(Wc2-Wc1)/%pi;
else
hd(n)=(sin(Wc2*((n-1)-alpha))-sin(Wc1*((n-1)-alpha)))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.42-(0.5*cos((2*%pi*(n-1))/(M-1)))+(0.08*cos((4*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR BPF using Blackman Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR BPF using Blackman Window');
```

# OUTPUT: 
<img width="712" height="585" alt="image" src="https://github.com/user-attachments/assets/18c18eb5-e862-4486-a7f3-09eb169a50c2" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
Wc2=Wc(2);
Wc1=Wc(1);
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=1-((Wc2-Wc1)/%pi);
else
hd(n)=(sin(Wc1*((n-1)-alpha))-sin(Wc2*((n-1)-alpha)))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.42-(0.5*cos((2*%pi*(n-1))/(M-1)))-(0.08*cos((4*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR BSF using Blackman Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR BSF using Blackman Window');
```

# OUTPUT: 
<img width="725" height="582" alt="image" src="https://github.com/user-attachments/assets/88b7fe55-d5c1-4eae-b7b7-3449155c9673" />


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.
