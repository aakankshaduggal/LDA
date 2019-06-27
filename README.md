# LDA : Latent Dirichlet Allocation
This python script can be used to identify the topics covered in text(s) files/


Change the path and mallet path. 
Change the filename and you're good to go.
Works for multiple files as well.

LDA:

    1. Create an elbow plot and print the coherence scores by specifying the number of topics to include, with:
        ```
        nlp.compute_coherence(start=5, stop=20, step=3)
        ```
    2. Set the number of topics to use in the model with:
        ```
        nlp.set_number_of_topics(10)
        ```
    3. View the clusters (only available in Jupyter notebook):
        ```
        import pyLDAvis
        pyLDAvis.enable_notebook()
        vis = nlp.view_clusters()
        pyLDAvis.display(vis)
        ```
    4. Get the vocabulary for each topic in the LDA model with (topics can be 'all', a list of integers, or a single integer):
        ```
        nlp.get_topic_vocabulary(topics='all', num_words=10)
        ```
    5. Get the documents most highly associated with the given topics with:
        ```
        nlp.get_representative_documents(topics='all', num_docs=1)
        ```
    6. Get the sentence summaries of the documents most highly associated with the given topics with:
        ```
        nlp.get_representative_sentences(topics='all', num_sentences=3)
        ```
    7.  Provide a name for an LDA topic (if preferred over the numbering system) with:
        ```
        nlp.name_topic(topic_number=1, topic_name='My topic')
   



Reference : https://github.com/raffg/harry_potter_nlp
