# Chapter 3: Time Series Forecasting

Chương này trình bày các phương pháp dự báo chuỗi thời gian phổ biến trong Machine Learning, bao gồm **FBProphet**, **Auto-ARIMA** và **VAR Model**, được minh họa qua các bộ dữ liệu thực tế.

## Dữ liệu sử dụng
`avocado.csv`: Giá bán lẻ bơ theo tuần tại Mỹ (2015–2018) | Recipe 3-1 đến 3-5 
`champagne.csv`: Doanh số champagne theo tháng (1964–1972) | Recipe 3-6 |
`AirQualityUCI.xlsx`: Chất lượng không khí theo giờ tại Ý | Recipe 3-7 |

## Thư viện cần cài đặt

```bash
pip install prophet
pip install pmdarima
pip install statsmodels
pip install scikit-learn
pip install pandas numpy matplotlib plotly
pip install openpyxl
```