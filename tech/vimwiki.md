# vimwiki

Un tutorial util (Marcus Kazmierczak):
[VimWiki](https://mkaz.blog/working-with-vim/vimwiki/)

Sa spunem ca rulezi o versiune modificata a structurii de fisiere standard din vimwiki.
Daca rulezi ```,w,w``` din _interiorul_ radacinii centrale (vimwiki/), vimwiki-diary va 
crea un folder `diary/` in care va salva jurnalul abia creat.

Dar daca intri intr-un sub-folder custom al directorului vimwiki central (care a fost creat
de tine in mod manual), atunci cand vei rula vimwiki-diary va fi creat cate un 
diary separat pentru fiecare sub-director.

De aceea e important ca de fiecare data cand vrei sa scrii ceva in diary sa te afli in 
pagina HUB centrala din vimwiki.

Mai mult, chiar si atunci cand lucrezi in alte foldere (diferite de /home/user), daca
intentionezi sa deschizi rapid jurnalul pentru a scrie ceva, o sa te trezesti ca se va 
crea un diary separat in folderul din care ai rulat comanda.

Pentru a evita acest lucru, trebuie intotdeauna sa schimbi :pwd cu ~/. vimwiki va recunoaste 
folderul creat pentru el si nu va mai salva in cine stie ce alte directoare, ci direct in `~/vimwiki`.



## Test markdown

Very nice tutorial about vimwiki:
[Getting started with VimWiki](https://blog.mague.com/?p=602)

And this is a really nice workflow (by Bryan Jenks):
[My Semi-Complete VimWiki Workflow](https://www.youtube.com/watch?v=9Bb8Ljyqpt4)

Let's now test the `code` feature.

```python
# Entry Class that holds the model for Entries table
class Entry(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    title = db.Column(db.String(100))
    slug = db.Column(db.String(100), unique=True)
    body = db.Column(db.Text)
    created_timestamp = db.Column(db.DateTime, default=datetime.datetime.now)
    modified_timestamp = db.Column(
            db.DateTime,
            default = datetime.datetime.now,
            onupdate = datetime.datetime.now)
```

Also on YouTube (helped me setting up Markdown preview):
[Writing and Previewing Markdown in Real Time](https://nickjanetakis.com/blog/writing-and-previewing-markdown-in-real-time-with-vim-8)
This is yet another tutorial that teaches how to setup vimwiki and gollum together to 
create a personal wiki that has all the bells and whistles you'd expect.
[Creating a personal wiki with Vimwiki and Gollum](https://davidyat.es/2017/09/01/vimwiki-plus-gollum/)
#### 2020-10-19 20:23

I'm pretty happy how it turned out. I can edit .MD files in vim and get a pretty decent
formating as is, but also I can review how the page looks in a browser.

Maybe working like this will really help me immerse myself in VIM and also have a solution
for all the little tutorials I wrote--they could now live on GitHub pages, accessible from 
anywhere in the world, and be visible even 
on my website. There is still some configuring to do to be able to achieve that, but nothing as hard
as setting up personal wiki pages seemed to me in the past.

I don't think it will completely make CherryTree obsolete for me for the moment, I have too
many notes stored in it, and some of it may have personal info that I would prefer to keep
separate.separate
