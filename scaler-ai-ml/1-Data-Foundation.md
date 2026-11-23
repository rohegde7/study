# Data Foundation

## Lec 1
- [Lecture link](https://www.scaler.com/academy/mentee-dashboard/class/549062/session)
- [Pre read](https://docs.google.com/document/d/1zi7sBeraM0gV1kvx6FYMDf2Y7EvmMj19ihTXa6WD6wM/edit?tab=t.0#heading=h.c9xvu6vfssms)
- [Post lec content: NumPy Slicing Visualizer](https://aiml-v-izs.vercel.app/v/fd-k7q2x9m4/slicing?embed=1)
- [Lec notes](https://scaler-production-new.s3.ap-southeast-1.amazonaws.com/attachments/attachments/000/499/957/original/Lecture_1__Introduction_to_Numpy_3.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIDNNIRGHAQUQRWYA%2F20260920%2Fap-southeast-1%2Fs3%2Faws4_request&X-Amz-Date=20260920T234706Z&X-Amz-Expires=561600&X-Amz-SignedHeaders=host&X-Amz-Signature=871d0a377ba484ae558850e54cf021b2728b676a4e4651e56b0d303dd9845d80)
- Use .shape to find the structure of the array, .ndim for number of dimensions, and .size for total elements.
- Type Conversion: Use astype() to convert array data types.
Example: Converting string type numeric data to floats for calculations.
- Creating a multi-dimensional array to represent restaurant votes and costs.
two_d_data = np.array([votes, costs]).T


## Lecture 2: Food Delivery Data Exploration and analysis 2

- Notebook code https://colab.research.google.com/drive/1hjWA8rbujJjYUCfNs6WdeZuPXZ4TxYNV?usp=sharing 
- Notebook notes https://colab.research.google.com/drive/15Ot3X6XwXmaVRVdEz037ILcmwDvbH5sA?usp=sharing#scrollTo=yuaFpkrdMIes
- LoRA (in terms of matrix)

## Lecture 3: Food Delivery Data Exploration and analysis 3
- Notebook code: https://colab.research.google.com/drive/1ka5bVMAefQiuvqqAwZ6-yU0F3Z-bimvU?usp=sharing
- Broadcasting
- Z = W^T . X + b --> z = decision, t = transpose, w = weight / experience, x = input, b = bias
- 

### to read
- np.arange
- reshape
- normal array vs numpy array
- A @ B for matrix multi
- For A+B, where A = [1,2,3], B = [[1,2], [3,4]] ...Why doesnt it work just like LCM. 2*6 dim matrices after broadcasting.
- See doubt resolution section

## Lecture 4 | Intro to PANDAS: Food Delivery Data Exploration and analysis 4
- Code notes: https://colab.research.google.com/drive/1B0myMpw5v6CVSl7U6EodTVs__2i0wojB?usp=sharing
- Notebook: https://colab.research.google.com/drive/1Zb6p_OzJlWVb8ZAn9c5IYqph56rjELaT?usp=sharing
- Spliting v Stacking --> in spliting the dimentions are same but after stacking dimentions are not same
- hstack vs vstack for 1D and 2D arrays --> hstack for 1D just concatenates because it has only 1 axis: 0
- Pandas intro
- [10 mins to Pandas](https://pandas.pydata.org/docs/user_guide/10min.html)

## doubts
- axis  / axes? right spelling? or diff or same ?

# All NP methods
- np.tile
- np.array
- np.concatenate() --> dimensions stay the same
- axis --> 0 is cut the matrix horizontally, 1 is cut the matrix vertically
- .shape()
- .size()
- .ndim
- .T --> transpose
- np.split(4) -> 4 equal parts - each one a separate array, so if total 4 elements are there then they will be set of 1 element each as 4 elements are divided into 4 equal parts which is 1 each in each part
- np.split(array, 2, axis=1)
- hstack
- vstack
- 

# All Pandas topics / methods
- pd.read_csv(CSV_FILE)
- [10 mins to Pandas](https://pandas.pydata.org/docs/user_guide/10min.html)
- 


# All topics
- llama code github
- np.vectoriese
- A @ B
- spliting and stacking -> 2 opposite operations -> in spliting the dimentions are same but after stacking dimentions are not same
- 
