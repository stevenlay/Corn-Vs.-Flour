# Corn-Vs.-Flour
Corn vs. Flour Tortilla Classifier

fast.ai Week 1 and Week 2

## Data

Data was obtained from Google Images and downloaded using 

```javascript
urls = Array.from(document.querySelectorAll('.rg_di .rg_meta')).map(el=>JSON.parse(el.textContent).ou);
window.open('data:text/csv;charset=utf-8,' + escape(urls.join('\n')));
```

The above JavaScript code was executed in the browser's console and the resulting .csv file was used to download the respective images.
Using the fast.ai library, the images were downloaded for both corn tortillas and flour tortillas.

<batch data here>

## Training The Model

Transfer learning will be used and in this case, Resnet34 was used as a pretrained model along with its weights. Learning rate was iterated over to determine the best slices to use while trying to fit.

<confusion matrix>
<top losses>

## Cleaning Up

An important thing to note is that there are images that should not be in our data, either because they are misclassified or because they are irrevalent to our model. As such, it important to validate and clean our data to reduce potential errors.
