# Pandas

{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "88f0ab85",
   "metadata": {},
   "source": [
    "# Pandas\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "64ad0d06",
   "metadata": {},
   "source": [
    "# Series:-\n",
    "# series Object is one-dimensional labeled array."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "8b4d96e5",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "d99a3a3c",
   "metadata": {},
   "outputs": [],
   "source": [
    "s1=pd.Series([10,20,30,40,50])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "988cdc3f",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0    10\n",
       "1    20\n",
       "2    30\n",
       "3    40\n",
       "4    50\n",
       "dtype: int64"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "s1\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "d4b96fdb",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "pandas.core.series.Series"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(s1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "0fb9cf15",
   "metadata": {},
   "outputs": [],
   "source": [
    "s1=pd.Series([10,20,30,40,50],index=['a','b','c','d','e'])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "1466b8d8",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "a    10\n",
       "b    20\n",
       "c    30\n",
       "d    40\n",
       "e    50\n",
       "dtype: int64"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "s1"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "cc0e3fa9",
   "metadata": {},
   "source": [
    "# Series Object from Dictionary"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c27e704c",
   "metadata": {},
   "source": [
    "# create Dictionary"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "id": "fd7f0219",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "{'a': 10, 'b': 20, 'c': 30, 'd': 40}"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "d1={\"a\":10,\"b\":20,\"c\":30,\"d\":40}\n",
    "d1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "6f634fba",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "a    10\n",
       "b    20\n",
       "c    30\n",
       "d    40\n",
       "dtype: int64"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pd.Series(d1)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b8be8e5e",
   "metadata": {},
   "source": [
    "# Changing index position"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "77566e57",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "c    30\n",
       "b    20\n",
       "a    10\n",
       "d    40\n",
       "dtype: int64"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pd.Series(d1,index=[\"c\",\"b\",\"a\",\"d\"])"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1799094f",
   "metadata": {},
   "source": [
    "# Extracting individual Elements"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "id": "1e583ce8",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "4"
      ]
     },
     "execution_count": 20,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "import pandas as pd\n",
    "s2=pd.Series([1,2,3,4,5,6,7,8,9])\n",
    "s2[3]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "id": "cd23b97c",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0    1\n",
       "1    2\n",
       "2    3\n",
       "3    4\n",
       "4    5\n",
       "5    6\n",
       "6    7\n",
       "7    8\n",
       "8    9\n",
       "dtype: int64"
      ]
     },
     "execution_count": 21,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "s2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "id": "1c504317",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "6    7\n",
       "7    8\n",
       "8    9\n",
       "dtype: int64"
      ]
     },
     "execution_count": 22,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "s2[-3:]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "94bb1032",
   "metadata": {},
   "source": [
    "# Basic math operations on the Series"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "id": "6285e6d8",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "a    10\n",
       "b    20\n",
       "c    30\n",
       "d    40\n",
       "e    50\n",
       "dtype: int64"
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "s1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "id": "15560645",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0    1\n",
       "1    2\n",
       "2    3\n",
       "3    4\n",
       "4    5\n",
       "5    6\n",
       "6    7\n",
       "7    8\n",
       "8    9\n",
       "dtype: int64"
      ]
     },
     "execution_count": 24,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "s3=pd.Series([7,8,9,4,6,3])\n",
    "s2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "id": "84c71eff",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0     8.0\n",
       "1    10.0\n",
       "2    12.0\n",
       "3     8.0\n",
       "4    11.0\n",
       "5     9.0\n",
       "6     NaN\n",
       "7     NaN\n",
       "8     NaN\n",
       "dtype: float64"
      ]
     },
     "execution_count": 26,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "s2+s3"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "5ed8a87a",
   "metadata": {},
   "source": [
    "# Pandas Dataframe:-\n",
    "# Dataframe is a 2-dimensional labelled data structure."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1c9a8e25",
   "metadata": {},
   "source": [
    "# Creating a Dataframe"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "id": "af883c96",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd\n",
    "df=pd.DataFrame({\"Name\":['Shibu','simran','Sonam'],\"Marks\":[87,75,76]})"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "id": "514236d7",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Name</th>\n",
       "      <th>Marks</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Shibu</td>\n",
       "      <td>87</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>simran</td>\n",
       "      <td>75</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Sonam</td>\n",
       "      <td>76</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "     Name  Marks\n",
       "0   Shibu     87\n",
       "1  simran     75\n",
       "2   Sonam     76"
      ]
     },
     "execution_count": 30,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "id": "45a15587",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "pandas.core.frame.DataFrame"
      ]
     },
     "execution_count": 31,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(df)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c9d3e0e8",
   "metadata": {},
   "source": [
    "# Dataframe in-build function"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 39,
   "id": "ede7c9c2",
   "metadata": {},
   "outputs": [],
   "source": [
    "f=pd.read_csv('C:/Users/abhay kumar yadav/Downloads/Freedman.csv','r')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "id": "b02640f6",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>,\"population\",\"nonwhite\",\"density\",\"c</th>\n",
       "      <th>ime\"</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Akron,675,7.3,746,2602</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Albany,713,2.6,322,1388</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Albuquerque,NA,3.3,NA,5018</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Allentown,534,0.8,491,1182</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Anaheim,1261,1.4,1612,3341</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>105</th>\n",
       "      <td>Wilkes,340,0.3,383,613</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>106</th>\n",
       "      <td>Wilmington,488,11.7,419,2393</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>107</th>\n",
       "      <td>Worcester,612,0.9,405,2874</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>108</th>\n",
       "      <td>York,316,2,220,1062</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>109</th>\n",
       "      <td>Youngstown,528,9.2,513,1698</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>110 rows × 2 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "    ,\"population\",\"nonwhite\",\"density\",\"c  ime\"\n",
       "0                  Akron,675,7.3,746,2602   NaN\n",
       "1                 Albany,713,2.6,322,1388   NaN\n",
       "2              Albuquerque,NA,3.3,NA,5018   NaN\n",
       "3              Allentown,534,0.8,491,1182   NaN\n",
       "4              Anaheim,1261,1.4,1612,3341   NaN\n",
       "..                                    ...   ...\n",
       "105                Wilkes,340,0.3,383,613   NaN\n",
       "106          Wilmington,488,11.7,419,2393   NaN\n",
       "107            Worcester,612,0.9,405,2874   NaN\n",
       "108                   York,316,2,220,1062   NaN\n",
       "109           Youngstown,528,9.2,513,1698   NaN\n",
       "\n",
       "[110 rows x 2 columns]"
      ]
     },
     "execution_count": 40,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "f"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "id": "1bdf1b7f",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>,\"population\",\"nonwhite\",\"density\",\"c</th>\n",
       "      <th>ime\"</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Akron,675,7.3,746,2602</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Albany,713,2.6,322,1388</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Albuquerque,NA,3.3,NA,5018</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Allentown,534,0.8,491,1182</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Anaheim,1261,1.4,1612,3341</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "  ,\"population\",\"nonwhite\",\"density\",\"c  ime\"\n",
       "0                Akron,675,7.3,746,2602   NaN\n",
       "1               Albany,713,2.6,322,1388   NaN\n",
       "2            Albuquerque,NA,3.3,NA,5018   NaN\n",
       "3            Allentown,534,0.8,491,1182   NaN\n",
       "4            Anaheim,1261,1.4,1612,3341   NaN"
      ]
     },
     "execution_count": 41,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "f.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "id": "4a8a3757",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>,\"population\",\"nonwhite\",\"density\",\"c</th>\n",
       "      <th>ime\"</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>105</th>\n",
       "      <td>Wilkes,340,0.3,383,613</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>106</th>\n",
       "      <td>Wilmington,488,11.7,419,2393</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>107</th>\n",
       "      <td>Worcester,612,0.9,405,2874</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>108</th>\n",
       "      <td>York,316,2,220,1062</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>109</th>\n",
       "      <td>Youngstown,528,9.2,513,1698</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "    ,\"population\",\"nonwhite\",\"density\",\"c  ime\"\n",
       "105                Wilkes,340,0.3,383,613   NaN\n",
       "106          Wilmington,488,11.7,419,2393   NaN\n",
       "107            Worcester,612,0.9,405,2874   NaN\n",
       "108                   York,316,2,220,1062   NaN\n",
       "109           Youngstown,528,9.2,513,1698   NaN"
      ]
     },
     "execution_count": 42,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "f.tail()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "id": "55032b7b",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(110, 2)"
      ]
     },
     "execution_count": 44,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "f.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "id": "90199bf8",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>ime\"</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>count</th>\n",
       "      <td>0.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mean</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>std</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>min</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25%</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>50%</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>75%</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>max</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       ime\"\n",
       "count   0.0\n",
       "mean    NaN\n",
       "std     NaN\n",
       "min     NaN\n",
       "25%     NaN\n",
       "50%     NaN\n",
       "75%     NaN\n",
       "max     NaN"
      ]
     },
     "execution_count": 45,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "f.describe()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "id": "d9915169",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>,\"population\",\"nonwhite\",\"density\",\"c</th>\n",
       "      <th>ime\"</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Akron,675,7.3,746,2602</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Albany,713,2.6,322,1388</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Albuquerque,NA,3.3,NA,5018</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Allentown,534,0.8,491,1182</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Anaheim,1261,1.4,1612,3341</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "  ,\"population\",\"nonwhite\",\"density\",\"c  ime\"\n",
       "0                Akron,675,7.3,746,2602   NaN\n",
       "1               Albany,713,2.6,322,1388   NaN\n",
       "2            Albuquerque,NA,3.3,NA,5018   NaN\n",
       "3            Allentown,534,0.8,491,1182   NaN\n",
       "4            Anaheim,1261,1.4,1612,3341   NaN"
      ]
     },
     "execution_count": 46,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "f.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "id": "a7b29f49",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>30</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>31</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>32</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>33</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>34</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>35</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>36</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>37</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>38</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>39</th>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "Empty DataFrame\n",
       "Columns: []\n",
       "Index: [30, 31, 32, 33, 34, 35, 36, 37, 38, 39]"
      ]
     },
     "execution_count": 48,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "f.iloc[30:40,3:]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "c32d80c7",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.8"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}

