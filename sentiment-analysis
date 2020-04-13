#matplot for graph
import matplotlib.pyplot as plt
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer 
#vaderSentiment for sentiment check using polarities

#defining function for analysis which takes a sentence
def sentiment_analysis(sentence):
    sentiment_obj = SentimentIntensityAnalyzer() 
    #object creation
    sentiment_dict = sentiment_obj.polarity_scores(sentence) 
    #adding sentiment dictionary 
    print(sentiment_dict['neg']*100, "% SAD") 
    print(sentiment_dict['neu']*100, "% NEUTRAL") 
    print(sentiment_dict['pos']*100, "% HAPPY") 
    print(end = " ")

    #copying value for graph creation
    x = sentiment_dict['neg'] * 100
    y = sentiment_dict['neu'] * 100
    z = sentiment_dict['pos'] * 100
    #plotting bar graph
    plt.bar([1, 2, 3], [x, y, z])
    #adding name of bars on the x axis
    plt.xticks([1, 2, 3], ["Negative", "Neutral", "Positive"])
    plt.show()
    #if sentiment is greater than 0.05 then is positive
    if sentiment_dict['compound'] >= 0.05 : 
        print("HAPPY") 
    # if less than 0.05 is sad
    elif sentiment_dict['compound'] <= - 0.05 : 
        print("SAD") 
    #else remaining is neutral 
    else : 
        print("NEUTRAL") 

if __name__ == "__main__" : 
	sentence = input("ENTER SENTENCE = ")
	sentiment_analysis(sentence) 

