Sa se faca un workflow care ia ca input 2 numere a si b si afiseaza suma acestora. Functia o sa fie intr-un fisier python .py.
 
### 1) Creaza un fisier py cu numele calculator.py. 
Acesta trebuie sa contina o functie "suma" care ia ca argument 2 numere si returneaza suma acestora

### 2) Creaza un folder tests care sa contina un fisier test_calculator.py . 
Acest fisier trebuie sa contina un test simplu care sa verifice ca functia ta create mai sus functioneaza corect. 
 
 
          Plain Text
          from calculator import suma
          def test_suma():
            assert ...(completezi tu)
 
### 3) Creaza un workflow .github/workflows/calculator.yaml

Workflow-ul trebuie sa:

1. Sa se declanseze on workflow dispatch
1. Sa ruleze pe ubuntu-latest
1. Contina 2 inputuri numite numar1 si numar2
1. Cloneaza repository-ul (te vei folosi de GitHub - actions/checkout: Action for checking out a repo · GitHub)
1. Instaleaza python versiunea 3.11 (te vei folosi de GitHub - actions/setup-python: Set up your GitHub Actions workflow with a specific version of Pytho…) 
1. Instaleaza dependintele urmatoare(pytest, black) (folosind pip install)
1. Un pas care sa compileze codul din calculator.py (python -m py_compile calculator.py)
1. Ruleaza scriptul de python calculator.py folosind ca inputuri cele 2 numere introduse de catre user la pasul c)
1. Ruleaza testele folosind pytest
1. Ruleaza black pe fisierul calculator.py ca sa iti formateze codul (adereaza codul la un anume standard)
