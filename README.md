### Ant Lion Optimizer

##### Reference: Mirjalili S. The ant lion optimizer[J]. Advances in Engineering Software, 2015, 83: 80-98.

| Variables   | Meaning                                           |
| ----------- | ------------------------------------------------- |
| pop         | The population size                               |
| iter        | The maximum number of iterations                  |
| lb          | The lower bound (list)                            |
| ub          | The upper bound (list)                            |
| a_pos       | The position of ants (list)                       |
| a_score     | The score of ants (list)                          |
| al_pos      | The position of ant lions (list)                  |
| al_score    | The score of ant lions (list)                     |
| dim         | Dimension                                         |
| elite_score | The score of the elite ant lion                   |
| elite_pos   | The position of the elite ant lion                |
| iter_best   | The global best score of each iteration (list)    |
| con_iter    | The last iteration number when "gbest" is updated |

#### Test problem

$$
f(x)=\sum_{i=1}^{30}x_i^2,\qquad -100\leq x_i\leq100, \quad
i=1,\cdots, 30.
$$


#### Example

```python
if __name__ == '__main__':
    # Parameter settings
    pop = 20
    iter = 2000
    lb = [-100] * 30
    ub = [100] * 30
    print(main(pop, iter, lb, ub))
```

##### Output:

![](https://github.com/Xavier-MaYiMing/Ant-Lion-Optimizer/blob/main/convergence%20curve.png)

The IWO converges at its 2000-th iteration, and the global best value is 4.270541704648386e-08.

```python
{
    'best score': 4.270541704648386e-08, 
    'best solution': [-1.5391999586442185e-05, -1.7056386288551623e-05, -5.107088059014014e-05, -2.432108536136789e-05, -1.4308890774324676e-05, -3.8823790785923835e-06, -9.808114212909759e-05, -5.751616300205372e-05, -4.993437829049893e-05, -5.1607203380939716e-05, -1.8869367885403095e-05, 2.130054106617643e-05, -1.0130747574091335e-05, -3.3092614378570656e-06, 1.938125609972938e-06, 9.724418640964699e-06, 6.622633914203969e-05, 5.395217097802391e-05, 1.3272089053584755e-05, 4.4496518195489484e-05, 2.754550165856821e-05, 4.970789818374019e-05, 2.2878535581998185e-05, -2.2563536843683176e-05, -1.0995661702910254e-05, 5.0054321953539606e-05, 3.0219993298851248e-05, 1.9613764504500345e-05, 2.005490775217857e-05, -4.012568229501054e-05], 
    'convergence iteration': 2000
}
```

