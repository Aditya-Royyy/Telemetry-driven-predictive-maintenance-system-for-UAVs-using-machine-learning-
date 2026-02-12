# Telemetry-driven-predictive-maintenance-system-for-UAVs-using-machine-learning-
This work presents an LSTM-based predictive maintenance system for UAVs using real-time multi-sensor telemetry such as IMU, GPS, roll, pitch and yaw data to detect anomalies, predict future states, and support early fault identification, improving UAV reliability, safety, and operational readiness.
This application provides a web interface for UAV IMU (Inertial Measurement Unit) prediction using a pre-trained ONNX model. The app loads a serialized model bundle and performs inference without requiring PyTorch at runtime.

Features
CPU-only inference: Uses ONNX Runtime for efficient CPU-based predictions
Web interface: Built with Streamlit for easy interaction
Real-time predictions: Instant IMU data predictions with demo inputs
Scalable architecture: Uses cached model loading for optimal performance

Requirements:-
Python 3.8+
Streamlit
ONNX Runtime
NumPy
scikit-learn (for scalers)
PyTorch (only for loading serialized model bundle)

The application uses ONNX Runtime for efficient model inference pre-trained model UAV IMU prediction model feature scaling Input/output normalization using scikit-learn scalers
sequence processing Handles time-series IMU data sequences

The application architecture follows a clean and modular design, consisting of four main components. Model loading is handled using cached resources to ensure optimal performance and faster access during runtime. The user interface is built using Streamlit, providing an interactive and user-friendly experience. For prediction tasks, the inference pipeline leverages ONNX Runtime to enable efficient and reliable model execution. Finally, post-processing is applied through inverse scaling of model outputs to convert predictions back to their original real-world values for meaningful interpretation.

To extend the application, real IMU input methods such as sliders, file uploads, or live sensor data streaming can be integrated. Batch prediction capabilities can be implemented to process multiple datasets simultaneously. Additional visualization components may be added to display both input and output data clearly, along with model performance metrics to help evaluate prediction accuracy and system reliability.
