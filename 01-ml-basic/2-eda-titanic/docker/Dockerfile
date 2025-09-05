FROM python:3.11-slim
WORKDIR /app
RUN pip install --no-cache-dir jupyterlab pandas numpy matplotlib
EXPOSE 8888
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--no-browser", "--allow-root"]