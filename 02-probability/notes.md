# Ch. 2: Probability

## Sample Space

- Experiment: any process that generates a set of data
- Sample space (*S*): a set of all possible outcomes of a statistical experiment
  - In a coin tossing experiment, here is the sample space
  
    ```math
    S = \left\{ H, T \right\}
    ```

  - In an experiment consists of flipping a coin and if a head occurs, the coin is flipped again and if a tail occurs, a die is tossed, the sample space is
  
    ```math
    S = \left\{ HH, HT, T1, T2, T3, T4, T5, T6 \right\}
    ```

    it also can be expressed in a tree diagram.

    ```mermaid
    flowchart TD
    
    H1("H")
    H2("H")
    T2("T")
    T1("T")
    D1("1")
    D2("2")
    D3("3")
    D4("4")
    D5("5")
    D6("6")

    H1 --> H2
    H1 --> T2
    T1 --> D1
    T1 --> D2
    T1 --> D3
    T1 --> D4
    T1 --> D5
    T1 --> D6
    ```


- Element: each outcome in a sample space 