> :warning: This is a try to reproduce the ferminet paper results.



### Ferminet paper

Differents papers have been trying to use neural network to approximate solution of schrodinger equation.

The different papers :

- ferminet (one specific architecture to do a kind of PINN on schrodinger equation)
https://journals.aps.org/prresearch/pdf/10.1103/PhysRevResearch.2.033429, title Ab initio solution of the many-electron Schrödinger equation with deep neural networks

- psiformer : A Self-Attention Ansatz for Ab-initio Quantum Chemistry, https://arxiv.org/pdf/2211.13672, attention based architecture

- paper extension to compute all the excited states "Accurate Computation of Quantum Excited States with Neural Networks", https://arxiv.org/abs/2308.16848

The two architecture can be shown here :
![Screenshot 2024-09-23 at 22 53 16](https://github.com/user-attachments/assets/d4166138-6fb8-41cd-9ed8-1236722a2175)


#### The idea 

The main idea of those papers is to use the schrodinger equation in the same way as the classical PINN neural networks use the physical loss to converge to the states that satisfy the physical constraints.

The schrodinger operator is :
![Screenshot 2024-09-23 at 22 52 00](https://github.com/user-attachments/assets/016e85ac-eb71-48d0-8929-cd42619b210d)

And basicly the idea is to minimize the loss :

![Screenshot 2024-09-23 at 22 54 31](https://github.com/user-attachments/assets/124635b8-551b-4b71-96b7-619eba9fa7ec)

with the gradiant of the loss being (nicely compute in the papers):

![Screenshot 2024-09-23 at 22 59 41](https://github.com/user-attachments/assets/55defb02-92ee-40b7-b565-58c8d3fd887a)

Quantum mecanic is of course very complex and to understand the full extend of the scientific method, one should educate himself in quantum mecanics first.

![Screenshot 2024-09-23 at 22 57 35](https://github.com/user-attachments/assets/904109e8-c4f5-4931-b2a6-febf154aea98)
