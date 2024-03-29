# GPT, Fine-tuning

> For embedding vectors approach checkout [WCAG GPT 2](https://github.com/planetabhi/wcag-gpt-2).

### Install
```npm install``` <br>
```pip install --upgrade openai openai"[datalib]"```

### Create .env
```OPENAI_KEY="<YOUR_SECRET_API_KEY>"```

### Prepare data
```openai tools fine_tunes.prepare_data -f ./data/YOUR_DATA_FILE.jsonl```

### Update uploadFile.js
```fs.createReadStream('./data/YOUR_PREPARED_DATA_FILE.jsonl'),```

### Upload the training data and generate file ID
```node uploadFile.js```

### Update createFineTune.js
```training_file: 'YOUR_FILE_ID'```

### Tune model
```node createFineTune.js```

### Check status
```node listFineTunes.js```

### Try your model
```node createCompletion.js```
