# Useful Rails Queries

## Check if associated records do exist
`User.first.expenses.includes(:groups).where(:groups => { id: nil})`

## Check if associated records don't exist
`User.first.expenses.includes(:groups).where.not(:groups => { id: nil})`

or

`User.first.expenses.where.missing(:groups)`
