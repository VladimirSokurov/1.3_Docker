FROM python:3.8

WORKDIR /stocks_products

COPY ./stocks_products /stocks_products

RUN pip install -r /stocks_products/requirements.txt

ENV SECRET_KEY ojfhjdhfg33434sdoigfj
ENV DEBUG True

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]