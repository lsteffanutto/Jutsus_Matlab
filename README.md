# JUTSUS MATLAB

# Transposé
X.' = Transposé simple de X ;
X' = Hermitienne de X = transposé conjugué de X = X* dans cours antennes

# Plots

#affichage plot
ylabel('P(\theta)','rotation',0); 

#scatter
scatter(index_peak(1),peaks(1),100,'g+','LineWidth',2.5);

#titre/legend avec variable
title('P(\theta) pour \theta = 40\circ et M = 5 capteurs');
legend("\sigma_v="+sigma_v_tab(1),"\sigma_v="+sigma_v_tab(2),"\sigma_v="+sigma_v_tab(3));

#mega plot avec scatter et plot
plot(signal,'b-');xlim([0 1024]); %signal
hold on;
scatter(locs,pks,'r+','LineWidth',1);xlim([0 1024]); %points max
hold on;
scatter(locs_min,signal(locs_min),'k+','LineWidth',1);xlim([0 1024]); %points min
hold on;
plot(env_max,'g-','LineWidth',1);xlim([0 1024]); %env_max
hold on;
plot(env_min,'r-','LineWidth',1) %env_min

#Zooms sur plot synchro
linkaxes([h1,h2,h3]); %zoom synchronisé

#Mettre figure direct plein ecran
FigH = figure('Position', get(0, 'Screensize'));
#La save
saveas(FigH, 'Foo.png','png');

#squeeze
t'as 3 plan rgb d'une image, tu fais squeeze, ça les mets tous els uns a cotes des auttres

