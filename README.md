# JUTSUS MATLAB

# Transposé
X.' = Transposé simple de X ;
X' = Hermitienne de X = transposé conjugué de X = X* dans cours antennes

# Plots


ylabel('P(\theta)','rotation',0);

scatter(index_peak(1),peaks(1),100,'g+','LineWidth',2.5);

title('P(\theta) pour \theta = 40\circ et M = 5 capteurs');

legend("\sigma_v="+sigma_v_tab(1),"\sigma_v="+sigma_v_tab(2),"\sigma_v="+sigma_v_tab(3));


