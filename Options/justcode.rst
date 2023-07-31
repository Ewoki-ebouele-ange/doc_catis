  
Just Code
=============

Key Goals
---------------


Options
-------

Scratch
~~~~~~~~


KidsRuby
~~~~~~~~

Python
~~~~~~
Here is some code::

        def predict_price(new_listing):
            temp_df = train_df.copy()
            temp_df['distance'] = temp_df['bedrooms'].apply(lambda x: np.abs(x - new_listing))
            temp_df = temp_df.sort_values('distance')
            nearest_neighbors = temp_df.iloc[0:5]['price']
            predicted_price = nearest_neighbors.mean()
            return(predicted_price)

        test_df['predicted_price'] = test_df['accommodates'].apply(lambda x: predict_price(x))
        test_df['predicted_price'] = test_df['bedrooms'].apply(lambda x: predict_price(x))
        test_df['squared_error'] = (test_df['predicted_price'] - test_df['price'])**2
        mse = test_df['squared_error'].mean()
        print(mse)

Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maxime minima assumenda incidunt provident magnam dolore! Blanditiis consectetur fugit inventore rerum quos labore omnis quia laboriosam, 
numquam odit dolorum pariatur libero::

    def predict_price(new_listing):
    temp_df = train_df.copy()
    temp_df['distance'] = temp_df['bedrooms'].apply(lambda x: np.abs(x - new_listing))
    temp_df = temp_df.sort_values('distance')
    nearest_neighbors = temp_df.iloc[0:5]['price']
    predicted_price = nearest_neighbors.mean()
    return(predicted_price)

    test_df['predicted_price'] = test_df['accommodates'].apply(lambda x: predict_price(x))
    test_df['predicted_price'] = test_df['bedrooms'].apply(lambda x: predict_price(x))
    test_df['squared_error'] = (test_df['predicted_price'] - test_df['price'])**2
    mse = test_df['squared_error'].mean()
    print(mse)



Hopscoth
~~~~~~~~