if you successfully [installed anvio](https://zetazee.github.io/anvio/installation.html), you can proceed from here.

anvio visualizations look like this:
![anvio interactive](installation/32.png)

when you learn to generate it, you can interact with it by hovering your mouse over each part to see more information. 
now we need to check if this interactive command works correctly, even though we don’t have any data or files to visualize yet. we actually need some files with the `.db` extension, but that’s okay—we’ll fake some. we’ll enter this code and expect to get an error saying the files don’t exist, which confirms that `anvi-interactive` works perfectly. however, if we get another message related to the interactive part, we’ll fix that.  
```bash
anvi-interactive -c CONTIGS.db -p MERGED/PROFILE.db -I localhost
```
![anvio interactive](installation/33.png)

i got the nicest error message, explaining in plain language how to fix the problem. so, i need to set my path correctly, install something called `npm`, and then run `cd -`.  

![anvio interactive](installation/34.png)

let’s run anvio interactive with our fake files again:

```bash
anvi-interactive -c CONTIGS.db -p MERGED/PROFILE.db -I localhost
```

![anvio interactive](installation/35.png)

now we got the correct error saying there’s no data in your system yet.  
now, let’s ask anvio to do a full self-test:  

```bash
anvi-self-test --suite mini
```

![anvio interactive](installation/36.png)

this test will show us how a real `anvi-interactive` works. by opening your localhost in the browser, you can see the newest version and a visualization.

![anvio interactive](installation/37.png)

localhost is a url generated on your system to view visualizations. it can have either of these addresses:  
>http://localhost:8080/
>http://127.0.0.1:8080/

anvio visualizations work best with chrome. so, if you notice any weirdness, try opening the url in chrome.  

also, kudos to whoever is naming the versions. 🎉  

![anvio interactive](installation/38.png)


# finalize and prepare for everything























