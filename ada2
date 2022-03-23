#
# Complete the 'subscription_summary' function below.
#

def subscription_summary(months_subscribed, ad_free_months, video_on_demand_purchases):
    """
    Parameters:
      months_subscribed: How many months each account purchased.
      ad_free_months: How many months each account paid for ad free viewing.
      video_on_demand_purchases: How many Videos on Demand each account purchased.
    """
    print("Welcome to the Ada+ Account Dashboard\n")
    #set list and dictionary      
    max_key_list = [] #  put the key of maximum value
    user_dictionary = {} # pair the account number (keys) and  sum purchase in account ( value)
    sum_ad_and_v_list = [] # each account pay for ad-free and movie
    
    # all formulas
    for i in range(len(months_subscribed)):
        if months_subscribed[i] % 3 == 0: # 3 month bundle
            ms = format(int(months_subscribed[i] / 3) * 18, '.2f')
        else:
            ms = format(int(months_subscribed[i] / 3) * 18 + int(months_subscribed[i] % 3) *7, '.2f')
            
        ad =  format(ad_free_months[i] * 2, '.2f') 
        v =  format(video_on_demand_purchases[i] * 27.99, '.2f') 
               
        sum_ad_and_v = float(ad) + float(v)
        sum_account = format(float(ms)+ sum_ad_and_v, '.2f') # each user pay all
         
        
        sum_ad_and_v_list.append(sum_ad_and_v)
        sum_all_ad_and_v = format(sum(sum_ad_and_v_list), '.2f')
        
        
        user_dictionary[str(i+1)] = float(sum_account) # pair account and total payment
        
        sum_all_account = format(sum(user_dictionary.values()), '.2f')
        
        
        print(f"Account {i+1} made ${sum_account} total")
    
        print(f">>> ${ms} from monthly subscription fees")
    
        print(f">>> ${ad} from Ad-free upgrades")       
        
        print(f">>> ${v} from Video on Demand purchases\n")
        
    
        
    print(f"Combined all accounts made ${sum_all_account} total")
      
    print(f"Premium content (Ad-free watching and Video on Demand) made ${sum_all_ad_and_v} total\n")
    
    max_v = max(user_dictionary.values())    # the max payment
    print(f"${max_v} was the most earned by any single account")
    
    
    # find the account, which made most payment
    
    for key,value in user_dictionary.items():
        if value == max_v:
           
            s = "#"+ key 
            
            max_key_list.append(s)
    
    y = ", ".join(str(i) for i in max_key_list) 
    
        
    print(f"The accounts that earned the most were: {y}")
        
    
    
    
    

if __name__ == '__main__':    
    months_subscribed = []
    ad_free_months = []
    video_on_demand_purchases = []
    
    header = input().strip()

    while header == "months_subscribed:":
        line = input().strip()
        try:
            months_subscribed.append(int(line))
        except ValueError:
            header = line

    while header == "ad_free_months:":
        line = input().strip()
        try:
            ad_free_months.append(int(line))
        except ValueError:
            header = line

    while header == "video_on_demand_purchases:":
        try:
            line = input().strip()

            video_on_demand_purchases.append(int(line))
        except EOFError:
            header = None
            
    subscription_summary(months_subscribed, ad_free_months, video_on_demand_purchases)
