# Assignment

## Brief

Write the YML for the following questions.

## Instructions

Paste the answer as YML in the answer code section below each question.

### Question 1

Question: Add 2 more tests each using `dbt_utils` and `dbt-expectations` to `fact_sales`.

Answer:

Specs for `dbt_utils`:

```yml
models:
  - name: fact_sales
    columns:
        - name: invoice_and_item_number
        description: 'Ensures values are unique'
        tests:
          - dbt_utils.not_constant
```

Specs for `dbt-expectations`:

```yml
models:
  - name: fact_sales
    columns:
      - name: bottles_sold
        description: 'Ensures bottles_sold is not null'
        tests:
          - dbt_expectations.expect_column_values_to_not_be_null
```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
