# Volatility Prediction

Options traders rely heavily on their estimates of future volatility to guide their decisions. A successful predictive model has proven to be highly profitable. The traditional approach to volatility prediction involves an autoregressive model such as GARCH. Nevertheless, such an approach's accuracy is limited due to the inflexibility of the model to describe complex patterns in the financial market. In this research, we applied various machine learning algorithms such as XGBoost and RNN to forecast volatility. Experiment results based on historical stock data of S\&P 500, Dow Jones, and Nasdaq have showcased significant improvements in model performance from using modern machine learning than the traditional econometrics approach.

\begin{center}
\begin{tabular}{||c c c c||} 
 \hline
     Model & Eval MSE & Test MSE & Weighted Eval + Test MSE\\ [0.5ex] 
 \hline\hline
 GARCH & / & / &  0.278 \\ 
 \hline
 XGBoost & / & / &  0.228 \\ 
 \hline
 LSTM\_base & 0.166 & 0.419 &  0.318 \\ 
 \hline
 LSTM\_3layers & 0.042 & 0.342 & 0.222 \\ 
 \hline
 LSTM\_mult\_feats\_base & 0.056 & 0.091 & 0.077 \\ 
 \hline
 LSTM\_mult\_feats\_high\_corr & 0.060 & 0.083 &  0.074 \\ 
 \hline
 LSTM\_mult\_feats\_CNN & 0.106 & 0.095 & 0.100 \\ 
  \hline
 \textbf{GRU\_mult\_feats\_base}  & \textbf{0.026} & \textbf{0.039} & \textbf{0.034} \\ 
 \hline
 GRU\_mult\_feats\_high\_corr & 0.031 & 0.058 & 0.047 \\ 
 \hline
 GRU\_mult\_feats\_lookback\_30 & 0.039 & 0.072 & 0.059 \\ 
 \hline
 GRU\_mult\_feats\_lookback\_126 & 0.261 & 0.261 & 0.261 \\ 
 \hline
\end{tabular}
\captionof{table}{Ablation Study}
\end{center}
