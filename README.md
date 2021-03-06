# t-hoarder_kit
Set of basic tools to extract data from the Twitter API and visualize graphs

## Installation:

Recommended to clone with git, so versions are automatically updated

    git clone https://github.com/congosto/t-hoarder_kit

Dependencies: [tweepy](https://github.com/tweepy/tweepy)

Python 2.7.12 or newer. Python 3.x not supported


## Enviroment

T-hoarder kit works on the following directory structure

     T-hoarder_kit --+-- keys (app keys and users access token for oauth authentication in the API)
                     |
                     +- scripts ( scripts in Python)
                     |
                     +- store -+-- experiment-1 ( A directory for each experiment so the data is not mixed)
                               |
                               +-- experiment-2
                               ....
                               |
                               +-- experiment-n

Assume that the access keys are in the keys directory and the results are deposited in the store/experiment directory

T-hoarder_kit.sh provides a menu for access to python scripts. 


      1. Get a user token access
      2. Get users information (profile | followers | following | relations | tweets | h_index)
      3. Make a query on Twitter
      4. Get tweets on real time
      5. Generate the declared relations graph (followers or following or both)
      6. Generate the dynamic relations graph (RT | reply | mentions)
      7. Processing tweets (sort |entities| classify| users | spread)
      8. Exit

For more information, **visit the [wiki](https://github.com/congosto/t-hoarder_kit/wiki)**

Using the python scripts from the command line the keys and the results is free to place them where you want

      tweet_auth.py [-h] keys_app user

      tweet_rest.py [-h] [--id_user] [--fast]
                     (--profile | --followers | --following | --relations | --connections | --tweets | --h_index)
                     keys_app keys_user file_users

      tweet_search.py [-h] [--query QUERY] [--file_out FILE_OUT]
                       [--language LANGUAGE]
                       keys_app keys_user
 
      tweet_streaming.py [-h] [--users USERS] [--words WORDS]
                          [--locations LOCATIONS]
                          app_keys user_keys dir_out file_dest

      tweets_grafo.py [-h] [--top_size TOP_SIZE] (--RT | --mention | --reply)
                       file_in

      tweets_entity.py [-h] [--top_size TOP_SIZE] [--TZ TZ]
                        file_in path_experiment path_resources

      tweets_classify.py [-h] file_in file_topics path_experiment

      users_types.py [-h] file_in path_experiment

      tweets_spread.py [-h] [--top_size TOP_SIZE] [--TZ TZ]
                        file_in path_experiment

      user_klout.py [-h] file_users APIkey




