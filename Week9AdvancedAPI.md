


print("Part two: Combining API's")
import requests

# Crypto Explorer

# # Fetch Bitcoin price
# btc_response = requests.get('https://api.coinpaprika.com/v1/tickers/btc-bitcoin')

# if btc_response.status_code == 200:
#     btc_json_data = btc_response.json()
#     btc_price = btc_json_data['quotes']['USD']['price']
#     print("Bitcoin price in USD:", btc_price)
# else:
#     print("Bitcoin API call status code:", btc_response.status_code)
#     print("Error fetching Bitcoin price")

# # Fetch Ethereum price
# eth_response = requests.get('https://api.coinpaprika.com/v1/tickers/eth-ethereum')

# if eth_response.status_code == 200:
#     eth_json_data = eth_response.json()
#     eth_price = eth_json_data['quotes']['USD']['price']
#     print("Ethereum price in USD:", eth_price)
# else:
#     print("Ethereum API call status code:", eth_response.status_code)
#     print("Error fetching Ethereum price")



# Country explorer

# country_code = "us"
# response = requests.get(f'https://restcountries.com/v3.1/alpha/{country_code}')

# if response.status_code == 200:
#     json_data = response.json()[0]
    
#     country_name = json_data['name']['common']
#     capital = json_data['capital'][0]
#     region = json_data['region']
#     population = json_data['population']
#     area = json_data['area']
#     currency_code = list(json_data['currencies'].keys())[0]
#     currency_name = json_data['currencies'][currency_code]['name']
    
#     print(f"Country: {country_name}")
#     print(f"Capital: {capital}")
#     print(f"Region: {region}")
#     print(f"Population: {population}")
#     print(f"Area: {area} km²")
#     print(f"Currency: {currency_name} ({currency_code})")
    
# else:
#     print("API call status code:", response.status_code)
#     print("Error fetching country data")


# Currency explorer

# import requests

# def get_exchange_rate(base_currency, target_currency):
#     response = requests.get(f'http://www.floatrates.com/daily/{base_currency.lower()}.json')
#     if response.status_code == 200:
#         return response.json()[target_currency.lower()]['rate']
#     else:
#         return None

# base_currency = input("Enter the base currency code (e.g., 'USD' for US Dollar): ").upper()
# target_currency = input("Enter the target currency code (e.g., 'EUR' for Euro): ").upper()

# exchange_rate = get_exchange_rate(base_currency, target_currency)

# if exchange_rate is not None:
#     print(f"Exchange rate from {base_currency} to {target_currency}: {exchange_rate:.4f}")
# else:
#     print("Error fetching exchange rate")


# POWER comes, when you combine API's : now you have the product
# import requests

# def get_crypto_prices():
#     response = requests.get('https://api.coinpaprika.com/v1/tickers/btc-bitcoin')
#     btc_usd = response.json()['quotes']['USD']['price']

#     response = requests.get('https://api.coinpaprika.com/v1/tickers/eth-ethereum')
#     eth_usd = response.json()['quotes']['USD']['price']

#     return btc_usd, eth_usd

# def get_country_info(country_code):
#     response = requests.get(f'https://restcountries.com/v3.1/alpha/{country_code}')
#     country_data = response.json()[0]

#     return {
#         'name': country_data['name']['common'],
#         'currency_code': list(country_data['currencies'].keys())[0],
#         'currency_name': country_data['currencies'][list(country_data['currencies'].keys())[0]]['name']
#     }

# def get_exchange_rate(currency_code):
#     response = requests.get(f'http://www.floatrates.com/daily/usd.json')
#     return response.json()[currency_code.lower()]['rate']

# def convert_to_local_currency(amount_in_usd, usd_to_local_currency):
#     return amount_in_usd * usd_to_local_currency

# country_code = input("Enter a 2-letter country code (e.g., 'us' for the United States): ").lower()
# country_info = get_country_info(country_code)
# btc_usd, eth_usd = get_crypto_prices()

# usd_to_local_currency = get_exchange_rate(country_info['currency_code'])
# btc_local_currency = convert_to_local_currency(btc_usd, usd_to_local_currency)
# eth_local_currency = convert_to_local_currency(eth_usd, usd_to_local_currency)

# print(f"Country: {country_info['name']}")
# print(f"Currency: {country_info['currency_name']} ({country_info['currency_code']})")
# print(f"Bitcoin price: {btc_local_currency:.2f} {country_info['currency_code']}")
# print(f"Ethereum price: {eth_local_currency:.2f} {country_info['currency_code']}")
