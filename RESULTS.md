Experimental Results: RNN vs. LSTM

To evaluate the differences between RNN and LSTM models, we first conducted experiments using identical parameters and the same dataset. The initial results are summarized below.

Figure 1: RNN model with a look-back window of 5 days, MSE = 1.50

Figure 2: LSTM model with a look-back window of 5 days, MSE = 1.75

From these results, it is clear that the RNN model achieved higher accuracy than the LSTM model under short look-back conditions. However, based on prior research and the theoretical advantages of LSTM—particularly its ability to capture long-term dependencies—we further adjusted the model parameters to explore whether LSTM performance could be improved.

Look-back Window = 30 Days

Figure 3: RNN model with look-back = 30 days, MSE = 2.80

Figure 4: LSTM model with look-back = 30 days, MSE = 2.60

After increasing the look-back window, overall model performance deteriorated, with higher MSE values for both models. Although the LSTM model did not show significant improvement, it slightly outperformed the RNN model in this configuration. Based on this observation, we further increased the look-back window to test the effect of longer historical context.

Look-back Window = 60 Days

Figure 5: RNN model with look-back = 60 days, MSE = 2.50

Figure 6: LSTM model with look-back = 60 days, MSE = 4.80

When the look-back window was extended to 60 days, the LSTM model exhibited clear signs of overfitting, resulting in a substantial increase in MSE. This indicates that increasing the look-back window does not necessarily lead to better performance, and excessively long sequences may negatively impact model generalization.

Key Observations

Through progressive experimentation, we found that:

RNN performs well in short-term stock prediction, offering faster computation and stronger performance for next-day forecasting.

LSTM is theoretically better suited for modeling long-term dependencies, as it incorporates gating mechanisms (forget, update, and output gates) that enhance sequence learning.

However, in this study, LSTM did not achieve stable or reliable improvements despite multiple parameter adjustments.

Stock price movements are influenced by numerous external factors, such as political events, earnings announcements, and macroeconomic uncertainty. Additionally, our data analysis suggests that factors such as gold and crude oil prices do not have a deterministic impact on the selected stock. As a result, using excessively long historical windows may introduce noise rather than useful information.

Overall Conclusion

Based on the experimental results and supporting literature, we conclude that:

RNN is more effective for short-term stock price prediction

LSTM has potential advantages for long-term trend modeling, but its performance is highly sensitive to parameter choices and data characteristics

The complexity of financial markets limits the predictability of stock prices, especially when relying solely on historical numerical data

Therefore, careful model selection, parameter tuning, and realistic expectations are essential when applying deep learning techniques to stock market prediction.

4.2 Feature Selection: Single Feature vs. Multiple Features

Through comparative experiments, we found that the number of input features does not necessarily correlate with higher prediction accuracy. Model performance depends heavily on both data characteristics and model design.

Figure 7: Prediction using only the closing price

Figure 8: Prediction using multiple input features

While incorporating more features can provide additional information, it also increases the risk of overfitting, especially when the feature space grows faster than the available data. Higher-dimensional feature spaces lead to sparser samples and require more data to maintain generalization performance.

Our experiments indicate that, for short-term stock prediction tasks, using only the closing price often yields the highest accuracy. This aligns with common industry practices where short-term forecasts primarily rely on price-based signals.

4.3 Future Work

Although the current models can predict next-day stock price movements, there remains significant room for improvement in both predictive depth and practical applicability.

Future directions include:

Extending the prediction horizon toward longer-term forecasting

Experimenting with alternative architectures such as:

Convolutional Neural Networks (CNN)

Gated Recurrent Units (GRU)

Further tuning model parameters to balance performance and overfitting

Expanding feature sets beyond fundamental data to include:

Technical indicators

Market sentiment and news-based features

In addition to deep learning approaches, we plan to study and integrate insights from traditional technical analysis, fundamental analysis, and classical machine learning models. By combining the strengths of multiple methodologies, we aim to build a more robust and adaptable stock analysis framework.

Ultimately, these improvements are intended to enhance predictive accuracy while maintaining reliability in rapidly changing financial markets, providing a more effective decision-support tool for investors operating in complex and uncertain environments.
