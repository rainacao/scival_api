# SciVal Author Lookup

1. create a conda environment, download dependencies
```
conda create -n authorlookup
conda activate authorlookup
conda install python=3.10
conda install jupyter
conda install pandas
conda install -c conda-forge python-dotenv
```
2. download the repo as a zip file, or by going into the directory of your choice `cd desired/file/path` and clone the repository using `git clone https://github.com/rainacao/scival_author_lookup.git`

3. get an api key from scival (https://dev.elsevier.com/)
4. create a file named ".env" and paste the following in. replace the carets <> with your key. no quotation marks are necessary; it should look like API_KEY=1234abcd
```
API_KEY=<your API key here>
```
5. change the necessary components in the jupyter notebook file, marked by !!!
6.  run scival_api.ipynb from a computer which can connect directly from an organization with an Elsevier subscription. VPNs are supposed to work, but I found that I needed to work directly from a university computer
7. the output csv will have "warning" and "subjects" columns, along with a column of ascending numbers, which should be removed before uploading. those columns are meant for manual double checking if necessary. 
   - you can manually look for an author and their author ID in the second part of scival_api. fill out the corresponding information, and copy the relevant parts into the corresponding columns of the output csv.
