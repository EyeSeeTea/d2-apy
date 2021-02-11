# d2-apy
python version of d2-api
# Generate build
python setup.py sdist bdist_wheel
# Push package
sudo twine upload dist/* --verbose -u user -p pass
#import in pycharm example
from d2apy import dhis2api


api = dhis2api.Dhis2Api("https://play.dhis2.org/2.34/", "admin", "district")
print(api.get("/users.json"))
