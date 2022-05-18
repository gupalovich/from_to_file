# from_to_file
> Data conversions + unit tests (CSV, XML, XLSX, SQL, GoogleDoc)

## Startup
    Create virtualenv
    pip install -r requirements.txt
    git init
    git add .
    git commit -m "initial"
    git remote add origin {GITREPO.git}
    git branch -M main
    git push origin main
    pytest
    python main.py

## Features
- SQLite3
- Pytest
- Sentry

## Composition
    | assets
    | modules
        db.py
        utils.py
        | tests
            test_db.py
            test_utils.py
    .editorconfig
    .gitignore
    config.example.ini
    main.py
    requirements.txt

## Tests
```sh
pytest (run all tests)
pytest -s (with i/o logging)
pytest modules/tests/test_db.py (run separate testcase)
pytest -v -m slow (run only decorated tag-mark: @pytest.mark.slow)
pytest -v -m "not slow" (inverse - exclude tests decorated with 'slow')
```
