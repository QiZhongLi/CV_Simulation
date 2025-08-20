# Non-Gaussian State Simulation
Project for the 10387 Scientific Computing in Quantum Information Science.

Thie project follows Olga Solodovnikova's paper https://arxiv.org/abs/2508.06175, in which she uses coherent state decomposition is simulation non-Gaussian states and circuits. Here, we attempt to recreate part of her results and is not intended to be nearly as comprehensive as her package. Small bits of codes were nipped from her github repository and is labelled accordingly. 

Some information on the math and procedure:
Gaussian states of light has a very well characterized Wigner function precisely due to its Gaussian distribution. Specifically, we can use its covariance matrix and displacement vector to describe it fully. Moreover, any Gaussian operations are simple transformations of the state's covariance matrix and displacement vector.

Fock states, on the other hand, needs a matrix of size infinity by infinity to to have a fully described Wigner function. Therefore, any simulations involving Fock states require a photon number cut-off when plotting the Wigner function. This matters to Gaussian simulations because sometimes we require non-Gaussian operations, such as photon number counter, thus requiring us to switch to a Fock basis.

The referenced paper proposed a way to write a good approximation of Fock states as a linear combination of Gaussian (coherent) states, and efficiently so since the paper has derived the number of Gaussian states required for such an approximation.
