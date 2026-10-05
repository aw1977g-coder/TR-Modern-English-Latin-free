<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>TR Easy Bible</title>
<style>
:root{--bg:#fbf8f1;--fg:#262320;--mut:#8a8372;--line:#e3dac6;--red:#b3261e;--acc:#7a5c2e;--sel:#fbe9a6;--bar:#f2ecdd;--fs:20px}
:root[data-theme=dark]{--bg:#15130f;--fg:#e9e3d5;--mut:#9b937f;--line:#332e23;--red:#ff7b6e;--acc:#dcb76e;--sel:#514512;--bar:#1e1b14}
*{box-sizing:border-box}
html{-webkit-text-size-adjust:100%}
body{margin:0;background:var(--bg);color:var(--fg);font:var(--fs)/1.65 Georgia,"Times New Roman",serif}
button,select,input{font:15px system-ui,sans-serif;background:var(--bg);color:var(--fg);border:1px solid var(--line);border-radius:8px;padding:6px 10px;cursor:pointer}
.bar{position:sticky;top:0;z-index:5;background:var(--bar);border-bottom:1px solid var(--line);padding:calc(6px + env(safe-area-inset-top)) 10px 6px;display:flex;flex-wrap:wrap;gap:6px;align-items:center}
.ref{flex:1;text-align:center;color:var(--acc);font:600 15px system-ui,sans-serif;min-width:7em}
main{max-width:40rem;margin:0 auto;padding:18px 16px 150px 12px}
h1{font-size:1.5em;margin:.3em 0 0 .5em}
h2{font-size:.95em;font-weight:400;font-style:italic;color:var(--mut);margin:0 0 1em .8em}
.v{position:relative;margin:0 0 .75em;padding:0 4px 0 2.1em;border-radius:6px;cursor:pointer}
.n{position:absolute;left:0;width:1.7em;text-align:right;font:600 .6em system-ui,sans-serif;color:var(--mut);top:.85em}
.l{display:block}
.j{color:var(--red)}
.nored .j{color:inherit}
.v.on{background:var(--sel)}
.nav{display:flex;justify-content:space-between;gap:8px;margin:2em 0 0 .5em}
#sel{position:fixed;left:0;right:0;bottom:0;z-index:6;background:var(--bar);border-top:1px solid var(--line);padding:10px 10px calc(10px + env(safe-area-inset-bottom));display:none;flex-wrap:wrap;gap:6px;align-items:center;justify-content:center}
#sel.show{display:flex}
#selref{width:100%;text-align:center;font:600 15px system-ui,sans-serif;color:var(--acc)}
#toast{position:fixed;left:50%;bottom:90px;transform:translateX(-50%);background:#222;color:#fff;padding:8px 14px;border-radius:8px;font:14px system-ui,sans-serif;opacity:0;pointer-events:none;transition:opacity .2s;z-index:9;max-width:90%;text-align:center}
#toast.show{opacity:1}
#exit{display:none;position:fixed;top:calc(8px + env(safe-area-inset-top));right:8px;z-index:7;opacity:.6}
.imm .bar{display:none}.imm #exit{display:block}
dialog{width:min(92vw,40rem);max-height:85vh;background:var(--bg);color:var(--fg);border:1px solid var(--line);border-radius:12px;padding:14px;font:14px/1.5 system-ui,sans-serif}
dialog::backdrop{background:#0008}
#st table{width:100%;border-collapse:collapse}#st td{padding:3px 6px;border-bottom:1px solid var(--line);vertical-align:top}
#st .grk{font-family:Georgia,serif;font-size:1.15em}
</style>
</head>
<body>
<div class="bar" id="bar">
  <select id="book" aria-label="Book"></select>
  <select id="chap" aria-label="Chapter"></select>
  <button id="prev" title="Previous chapter" aria-label="Previous chapter">◀</button>
  <button id="next" title="Next chapter" aria-label="Next chapter">▶</button>
  <span class="ref" id="ref" aria-live="polite"></span>
  <button id="smaller" title="Smaller text" aria-label="Smaller text">A−</button>
  <button id="bigger" title="Larger text" aria-label="Larger text">A+</button>
  <button id="red" title="Show/hide red letters" aria-label="Toggle red letters"><span class="j">Red</span></button>
  <button id="theme" title="Light / dark" aria-label="Light or dark">◐</button>
  <button id="shareCh" title="Share this whole chapter" aria-label="Share chapter">Share chapter</button>
  <button id="strongsBtn" title="Strong's numbers list" aria-label="Strong's list">Strong's</button>
  <button id="full" title="Full screen" aria-label="Full screen">⛶</button>
</div>
<button id="exit" aria-label="Exit reading mode">✕</button>
<main id="main"></main>
<div id="sel">
  <div id="selref"></div>
  <button id="cText">Copy text</button><button id="cLink">Copy link</button><button id="doShare">Share…</button><button id="clear">Clear</button>
</div>
<div id="toast"></div>
<dialog id="st"><div style="display:flex;gap:8px;margin-bottom:8px"><input id="stq" placeholder="Filter (G number, Greek, English)…" style="flex:1"><button id="stx">Close</button></div><div id="stbody"></div></dialog>

<!--
=====================  HOW TO EDIT THIS FILE  =====================
TEXT:   Each book is one <script class="book"> block below. Change any word right in place.
FORMAT: "@12 Title" starts a chapter. "3 text" starts verse 3. Lines without a number
        continue the same verse (one sentence per line, like your Word file).
RED:    Wrap Jesus' words in <j>...</j>. Remove the tags to un-red. Tags are never shown or shared.
NEW BOOK: copy a whole <script class="book" ...> block, change data-name and data-chapters
        (total chapters in the book), and paste the new text. It shows up in the Book menu.
SHARING: set SHARE_URL below to the address where this file lives online, so shared
        links always point there (even when you open a local copy).
===================================================================
-->
<script type="text/plain" class="book" data-name="Matthew" data-chapters="28">
@5 The Sermon on the Mount
1 Jesus saw the crowds.
He went up on a mountain.
He sat down.
His followers came to him.
2 He began to teach them.
He said,
3 <j>God blesses those who know they need him.</j>
<j>The kingdom of heaven belongs to them.</j>
4 <j>God blesses those who are sad.</j>
<j>They will be comforted.</j>
5 <j>God blesses those who are gentle.</j>
<j>They will own the earth.</j>
6 <j>God blesses those who hunger and thirst to do what is right.</j>
<j>They will be filled.</j>
7 <j>God blesses those who show mercy.</j>
<j>They will be shown mercy.</j>
8 <j>God blesses those whose hearts are pure.</j>
<j>They will see God.</j>
9 <j>God blesses those who make peace.</j>
<j>They will be called children of God.</j>
10 <j>God blesses those who are hurt for doing what is right.</j>
<j>The kingdom of heaven belongs to them.</j>
11 <j>God blesses you when people insult you and hurt you.</j>
<j>When they lie and say all kinds of evil things about you because of me.</j>
12 <j>Be glad and rejoice.</j>
<j>Your reward in heaven is great.</j>
<j>In the same way, they hurt the prophets who came before you.</j>
13 <j>You are the salt of the earth.</j>
<j>But if salt loses its taste, how can it be made salty again?</j>
<j>It is no longer good for anything.</j>
<j>It is thrown out and walked on by people.</j>
14 <j>You are the light of the world.</j>
<j>A city set on a hill cannot be hidden.</j>
15 <j>No one lights a lamp and puts it under a basket.</j>
<j>Instead, they put it on a lamp stand.</j>
<j>And it gives light to everyone in the house.</j>
16 <j>In the same way, let your light shine before people.</j>
<j>Then they will see your good works.</j>
<j>And they will praise your Father in heaven.</j>
17 <j>Do not think that I came to do away with the Law or the Prophets.</j>
<j>I did not come to do away with them.</j>
<j>I came to make them come true.</j>
18 <j>I tell you the truth, until heaven and earth disappear, not one small letter, not one tiny mark will disappear from the Law.</j>
<j>All of it will come true.</j>
19 <j>So anyone who breaks one of the least of these commands and teaches others to do the same will be called least in the kingdom of heaven.</j>
<j>But whoever obeys them and teaches them will be called great in the kingdom of heaven.</j>
20 <j>I tell you, unless you do what is right and fair more than the teachers of the law and the Pharisees, you will never enter the kingdom of heaven.</j>
21 <j>You have heard that it was said to the people long ago, Do not murder.</j>
<j>Anyone who murders will be judged.</j>
22 <j>But I tell you, anyone who is angry with his brother without a reason will be judged.</j>
<j>And anyone who says to his brother, Raca, which means fool, will be judged by the court.</j>
<j>And anyone who says, You fool, will be in danger of the fire of hell.</j>
23 <j>So if you offer your gift at the altar, and there you remember that your brother has something against you,</j>
24 <j>leave your gift there in front of the altar.</j>
<j>First go and make peace with your brother.</j>
<j>Then come and offer your gift.</j>
25 <j>Come to terms quickly with the person who takes you to court.</j>
<j>Do it while you are still on the way.</j>
<j>If you do not, he may hand you over to the judge.</j>
<j>The judge may hand you over to the officer.</j>
<j>And you may be thrown into prison.</j>
26 <j>I tell you the truth, you will not get out until you have paid the last penny.</j>
27 <j>You have heard that it was said, Do not commit adultery.</j>
28 <j>But I tell you, anyone who looks at a woman to want her has already committed adultery with her in his heart.</j>
29 <j>If your right eye causes you to sin, take it out and throw it away.</j>
<j>It is better to lose one part of your body than for your whole body to be thrown into hell.</j>
30 <j>And if your right hand causes you to sin, cut it off and throw it away.</j>
<j>It is better to lose one part of your body than for your whole body to go into hell.</j>
31 <j>It has been said, Anyone who divorces his wife must give her a paper that says she is divorced.</j>
32 <j>But I tell you, anyone who divorces his wife except for sexual sin causes her to commit adultery.</j>
<j>And anyone who marries a woman who is divorced commits adultery.</j>
33 <j>Again, you have heard that it was said to the people long ago, Do not break your promises.</j>
<j>Keep the oaths you make to the Lord.</j>
34 <j>But I tell you, do not swear at all.</j>
<j>Do not swear by heaven, for it is God's throne.</j>
35 <j>Do not swear by the earth, for it is God's footstool.</j>
<j>Do not swear by Jerusalem, for it is the city of the great King.</j>
36 <j>Do not swear by your head.</j>
<j>You cannot make even one hair white or black.</j>
37 <j>Let your Yes be Yes, and your No be No.</j>
<j>Anything more than this comes from evil.</j>
38 <j>You have heard that it was said, Eye for eye, and tooth for tooth.</j>
39 <j>But I tell you, do not fight against an evil person.</j>
<j>If someone slaps you on the right cheek, turn to him the other cheek also.</j>
40 <j>If someone wants to sue you and take your shirt, let him have your coat also.</j>
41 <j>If someone forces you to go one mile, go with him two miles.</j>
42 <j>Give to the one who asks you.</j>
<j>And do not turn away from the one who wants to borrow from you.</j>
43 <j>You have heard that it was said, Love your neighbor and hate your enemy.</j>
44 <j>But I tell you, love your enemies.</j>
<j>Pray for those who hurt you.</j>
45 <j>Then you will be children of your Father in heaven.</j>
<j>He causes his sun to rise on evil people and good people.</j>
<j>And he sends rain on those who do right and those who do wrong.</j>
46 <j>If you love only those who love you, what reward will you get?</j>
<j>Even tax collectors do that.</j>
47 <j>If you greet only your own people, what more are you doing than others?</j>
<j>Even people who do not know God do that.</j>
48 <j>So be perfect, just as your Father in heaven is perfect.</j>

@6 Giving, Prayer, and Trusting God
1 <j>Be careful not to do your good works in front of people to be seen by them.</j>
<j>If you do, you will have no reward from your Father in heaven.</j>
2 <j>So when you give to the needy, do not announce it with trumpets.</j>
<j>The fake leaders do this in the meeting places and in the streets.</j>
<j>They want to be honored by people.</j>
<j>I tell you the truth, they have received their reward in full.</j>
3 <j>But when you give to the needy, do not let your left hand know what your right hand is doing.</j>
4 <j>Then your giving will be in secret.</j>
<j>And your Father, who sees what is done in secret, will reward you.</j>
5 <j>When you pray, do not be like the fake leaders.</j>
<j>They love to pray standing in the meeting places and on the street corners.</j>
<j>They want to be seen by people.</j>
<j>I tell you the truth, they have received their reward in full.</j>
6 <j>But when you pray, go into your room, close the door, and pray to your Father who is unseen.</j>
<j>Then your Father, who sees what is done in secret, will reward you.</j>
7 <j>And when you pray, do not use meaningless words like the people who do not know God do.</j>
<j>They think they will be heard because they say many words.</j>
8 <j>Do not be like them.</j>
<j>Your Father knows what you need before you ask him.</j>
9 <j>So pray like this:</j>
<j>Our Father in heaven, may your name be honored.</j>
10 <j>May your kingdom come.</j>
<j>May what you want be done on earth as it is in heaven.</j>
11 <j>Give us today our daily bread.</j>
12 <j>Forgive us our sins, just as we have forgiven those who sin against us.</j>
13 <j>Do not lead us into hard testing.</j>
<j>But save us from the evil one.</j>
<j>For yours is the kingdom and the power and the glory forever. Amen.</j>
14 <j>If you forgive people when they sin against you, your Father in heaven will also forgive you.</j>
15 <j>But if you do not forgive people their sins, your Father will not forgive your sins.</j>
16 <j>When you fast, do not look sad like the fake leaders.</j>
<j>They make their faces look bad to show people they are fasting.</j>
<j>I tell you the truth, they have received their reward in full.</j>
17 <j>But when you fast, put oil on your head and wash your face.</j>
18 <j>Then no one will know you are fasting except your Father who is unseen.</j>
<j>And your Father, who sees what is done in secret, will reward you.</j>
19 <j>Do not store up treasures on earth.</j>
<j>Moths and rust destroy them there.</j>
<j>And thieves break in and steal.</j>
20 <j>But store up treasures in heaven.</j>
<j>There moths and rust do not destroy.</j>
<j>And thieves do not break in and steal.</j>
21 <j>Where your treasure is, there your heart will be also.</j>
22 <j>The eye is the lamp of the body.</j>
<j>If your eyes are healthy, your whole body will be full of light.</j>
23 <j>But if your eyes are unhealthy, your whole body will be full of darkness.</j>
<j>If then the light in you is darkness, how great is that darkness!</j>
24 <j>No one can serve two masters.</j>
<j>Either he will hate one and love the other, or he will be loyal to one and despise the other.</j>
<j>You cannot serve both God and money.</j>
25 <j>So I tell you, do not worry about your life.</j>
<j>Do not worry about what you will eat or drink.</j>
<j>And do not worry about your body and what you will wear.</j>
<j>Life is more than food.</j>
<j>And the body is more than clothes.</j>
26 <j>Look at the birds of the air.</j>
<j>They do not plant or harvest or store away in barns.</j>
<j>Yet your Father in heaven feeds them.</j>
<j>Are you not much more valuable than they are?</j>
27 <j>Who of you by worrying can add a single hour to his life?</j>
28 <j>And why do you worry about clothes?</j>
<j>Look at the lilies of the field.</j>
<j>See how they grow.</j>
<j>They do not work or make clothes.</j>
29 <j>I tell you, not even Solomon in all his glory was dressed like one of these.</j>
30 <j>If God dresses the grass of the field like this, though it is here today and tomorrow is thrown into the fire, will he not much more dress you, you of little faith?</j>
31 <j>So do not worry.</j>
<j>Do not say, What will we eat? Or, What will we drink? Or, What will we wear?</j>
32 <j>People who do not know God run after all these things.</j>
<j>And your Father in heaven knows you need them.</j>
33 <j>But seek first his kingdom and what is right and fair.</j>
<j>And all these things will be given to you as well.</j>
34 <j>So do not worry about tomorrow.</j>
<j>Tomorrow will worry about itself.</j>
<j>Each day has enough trouble of its own.</j>

@7 Judging and Building on Rock
1 <j>Do not judge, or you too will be judged.</j>
2 <j>You will be judged in the same way you judge others.</j>
<j>The measure you use will be used for you.</j>
3 <j>Why do you look at the small speck in your brother's eye, but do not see the big board in your own eye?</j>
4 <j>How can you say to your brother, Let me take the speck out of your eye, when there is a board in your own eye?</j>
5 <j>You fake leader! First take the board out of your own eye.</j>
<j>Then you will see clearly to take the speck out of your brother's eye.</j>
6 <j>Do not give holy things to dogs.</j>
<j>Do not throw your pearls to pigs.</j>
<j>If you do, they may walk all over them.</j>
<j>Then they may turn and tear you to pieces.</j>
7 <j>Ask, and it will be given to you.</j>
<j>Seek, and you will find.</j>
<j>Knock, and the door will be opened to you.</j>
8 <j>Everyone who asks receives.</j>
<j>He who seeks finds.</j>
<j>To him who knocks, the door will be opened.</j>
9 <j>Which of you, if his son asks for bread, will give him a stone?</j>
10 <j>Or if he asks for a fish, will give him a snake?</j>
11 <j>If you, though you are evil, know how to give good gifts to your children, how much more will your Father in heaven give good gifts to those who ask him!</j>
12 <j>So in everything, do to others what you would want them to do to you.</j>
<j>This sums up the Law and the Prophets.</j>
13 <j>Enter through the narrow gate.</j>
<j>The gate is wide and the road is broad that leads to death.</j>
<j>And many people go through it.</j>
14 <j>But the gate is small and the road is narrow that leads to life.</j>
<j>And only a few people find it.</j>
15 <j>Watch out for false prophets.</j>
<j>They come to you in sheep's clothes, but inside they are hungry wolves.</j>
16 <j>You will know them by their fruit.</j>
<j>Do people pick grapes from thorn bushes, or figs from thistles?</j>
17 <j>In the same way, every good tree makes good fruit.</j>
<j>But a bad tree makes bad fruit.</j>
18 <j>A good tree cannot make bad fruit.</j>
<j>And a bad tree cannot make good fruit.</j>
19 <j>Every tree that does not make good fruit will be cut down and thrown into the fire.</j>
20 <j>So you will know them by their fruit.</j>
21 <j>Not everyone who says to me, Lord, Lord, will enter the kingdom of heaven.</j>
<j>Only the one who does what my Father in heaven wants will enter.</j>
22 <j>Many will say to me on that day, Lord, Lord, did we not prophesy in your name?</j>
<j>Did we not drive out demons in your name?</j>
<j>Did we not do many mighty works in your name?</j>
23 <j>Then I will tell them plainly, I never knew you.</j>
<j>Go away from me, you who do evil.</j>
24 <j>So everyone who hears these words of mine and does them is like a wise man.</j>
<j>He built his house on the rock.</j>
25 <j>The rain came down.</j>
<j>The floods came.</j>
<j>The winds blew and beat against that house.</j>
<j>But it did not fall, because it had its foundation on the rock.</j>
26 <j>But everyone who hears these words of mine and does not do them is like a foolish man.</j>
<j>He built his house on sand.</j>
27 <j>The rain came down.</j>
<j>The floods came.</j>
<j>The winds blew and beat against that house.</j>
<j>And it fell with a great crash.</j>
28 When Jesus finished saying these things, the crowds were amazed at his teaching.
29 He taught them as one who had authority, not as their teachers of the law.

@8 Jesus Heals and Calms
1 When Jesus came down from the mountain, large crowds followed him.
2 A man with leprosy came and knelt before him.
He said, Lord, if you are willing, you can make me clean.
3 Jesus reached out his hand and touched the man.
He said, <j>I am willing. Be clean!</j>
Right away, his leprosy was made clean.
4 Then Jesus said to him, <j>See that you do not tell anyone.</j>
<j>Go, show yourself to the priest.</j>
<j>And offer the gift Moses commanded, as a proof to them.</j>
5 When Jesus entered Capernaum, a Roman officer came to him.
He begged him for help.
6 He said, Lord, my servant lies at home and cannot move.
He is in terrible pain.
7 Jesus said to him, <j>I will come and heal him.</j>
8 The officer answered, Lord, I do not deserve to have you come under my roof.
But just say the word, and my servant will be healed.
9 I am a man under authority, with soldiers under me.
I tell one, Go, and he goes.
I tell another, Come, and he comes.
I tell my servant, Do this, and he does it.
10 When Jesus heard this, he was amazed.
He said to those following him, <j>I tell you the truth, I have not found such great faith even in Israel.</j>
11 <j>I tell you, many will come from the east and the west.</j>
<j>They will sit down with Abraham, Isaac, and Jacob in the kingdom of heaven.</j>
12 <j>But those who thought they belonged to the kingdom will be thrown out into darkness.</j>
<j>There they will weep and grind their teeth.</j>
13 Then Jesus said to the officer, <j>Go! It will be done just as you believed.</j>
And his servant was healed at that very hour.
14 When Jesus came into Peter's house, he saw Peter's mother-in-law lying in bed with a fever.
15 He touched her hand.
The fever left her.
She got up and began to serve him.
16 When evening came, many people who had demons in them were brought to him.
He drove out the spirits with a word.
And he healed all who were sick.
17 This was to make come true what the prophet Isaiah said.
He said, He took our sicknesses and carried our diseases.
18 When Jesus saw a crowd around him, he gave orders to go to the other side of the lake.
19 A teacher of the law came to him and said, Teacher, I will follow you wherever you go.
20 Jesus said to him, <j>Foxes have holes and birds of the air have nests.</j>
<j>But the Son of Man has no place to lay his head.</j>
21 Another follower said to him, Lord, first let me go and bury my father.
22 But Jesus said to him, <j>Follow me.</j>
<j>Let the dead bury their own dead.</j>
23 Then he got into the boat and his followers followed him.
24 Without warning, a fierce storm came up on the lake.
Waves were covering the boat.
But Jesus was sleeping.
25 The followers went and woke him.
They said, Lord, save us! We are going to drown!
26 He said to them, <j>Why are you afraid, you of little faith?</j>
Then he got up.
He spoke sharply to the winds and the waves.
And it became completely calm.
27 The men were amazed and asked, What kind of man is this?
Even the winds and the waves obey him!
28 When he came to the other side, to the land of the Gadarenes, two men who had demons in them met him.
They came from the tombs.
They were so violent that no one could pass that way.
29 They shouted, What do you want with us, Son of God?
Have you come here to hurt us before the set time?
30 A large herd of pigs was feeding at some distance from them.
31 The demons begged Jesus, If you drive us out, send us into the herd of pigs.
32 He said to them, <j>Go!</j>
So they came out and went into the pigs.
The whole herd rushed down the steep bank into the lake and died in the water.
33 Those tending the pigs ran off.
They went into town and told everything.
They told what happened to the men who had demons.
34 Then the whole town went out to meet Jesus.
When they saw him, they begged him to leave their region.

@9 Forgiveness and Following
1 Jesus got into a boat and crossed over.
He came to his own town.
2 Some men brought to him a man who could not walk, lying on a mat.
When Jesus saw their faith, he said to the man, <j>Take courage, son.</j>
<j>Your sins are forgiven.</j>
3 Some teachers of the law said to themselves, This man speaks evil against God!
4 Jesus knew what they were thinking.
He said, <j>Why do you think evil in your hearts?</j>
5 <j>Which is easier to say, Your sins are forgiven, or to say, Get up and walk?</j>
6 <j>But so that you may know that the Son of Man has power on earth to forgive sins—</j>
Then he said to the man who could not walk, <j>Get up, pick up your mat and go home.</j>
7 And the man got up and went home.
8 When the crowd saw this, they were filled with awe.
And they praised God, who had given such power to men.
9 As Jesus went on from there, he saw a man named Matthew sitting at the tax office.
He said to him, <j>Follow me.</j>
Matthew got up and followed him.
10 Later Jesus was having dinner at Matthew's house.
Many tax collectors and sinners came and ate with him and his followers.
11 When the Pharisees saw this, they asked his followers, Why does your teacher eat with tax collectors and sinners?
12 Jesus heard this and said, <j>Healthy people do not need a doctor, but sick people do.</j>
13 <j>Go and learn what this means: I desire mercy, not sacrifice.</j>
<j>I did not come to call those who are good.</j>
<j>I came to call sinners.</j>
14 Then John's followers came and asked him, Why do we and the Pharisees fast often, but your followers do not fast?
15 Jesus answered, <j>Can the guests at a wedding be sad while the groom is with them?</j>
<j>The time will come when the groom will be taken away from them.</j>
<j>Then they will fast.</j>
16 <j>No one sews a piece of new cloth on an old coat.</j>
<j>The new patch pulls away from the old coat, and the tear gets worse.</j>
17 <j>No one pours new wine into old leather wineskins.</j>
<j>If they do, the wineskins burst.</j>
<j>The wine spills and the wineskins are ruined.</j>
<j>Instead, they pour new wine into new wineskins.</j>
<j>And both are kept safe.</j>
18 While he was saying this, a ruler came and knelt before him.
He said, My daughter has just died.
But come and put your hand on her, and she will live.
19 Jesus got up and went with him.
So did his followers.
20 Just then, a woman who had been bleeding for twelve years came up behind him.
She touched the edge of his coat.
21 She said to herself, If I just touch his coat, I will be healed.
22 Jesus turned and saw her.
He said, <j>Take courage, daughter.</j>
<j>Your faith has healed you.</j>
And the woman was healed from that moment.
23 When Jesus entered the ruler's house, he saw the flute players and the noisy crowd.
24 He said, <j>Go away.</j>
<j>The girl is not dead, but sleeping.</j>
But they laughed at him.
25 After the crowd had been put outside, he went in.
He took the girl by the hand, and she got up.
26 News of this spread through all that area.
27 As Jesus went on from there, two blind men followed him.
They called out, Have mercy on us, Son of David!
28 When he had gone inside the house, the blind men came to him.
He asked them, <j>Do you believe that I am able to do this?</j>
Yes, Lord, they replied.
29 Then he touched their eyes and said, <j>It will be done for you just as you believed.</j>
30 And their sight was restored.
Jesus warned them firmly, <j>See that no one knows about this.</j>
31 But they went out and spread the news about him all over that region.
32 While they were going out, a man who could not speak because a demon was in him was brought to Jesus.
33 When the demon was driven out, the man who could not speak began to speak.
The crowd was amazed and said, Nothing like this has ever been seen in Israel!
34 But the Pharisees said, He drives out demons by the ruler of demons.
35 Jesus went through all the towns and villages.
He taught in their meeting places.
He preached the good news of the kingdom.
And he healed every disease and sickness.
36 When he saw the crowds, he had pity on them.
They were harassed and helpless, like sheep without a shepherd.
37 Then he said to his followers, <j>The harvest is great, but the workers are few.</j>
38 <j>So ask the Lord of the harvest to send out workers into his harvest field.</j>

@10 Sending Out the Twelve
1 Jesus called his twelve followers to him.
He gave them power to drive out evil spirits and to heal every disease and sickness.
2 These are the names of the twelve apostles.
First, Simon, who is called Peter, and his brother Andrew.
James, son of Zebedee, and his brother John.
3 Philip and Bartholomew.
Thomas and Matthew the tax collector.
James, son of Alphaeus, and Thaddaeus.
4 Simon the Zealot and Judas Iscariot, who betrayed him.
5 Jesus sent out these twelve.
He gave them these orders.
He said, <j>Do not go among the Gentiles.</j>
<j>And do not enter any town of the Samaritans.</j>
6 <j>Go instead to the lost sheep of Israel.</j>
7 <j>As you go, preach this message.</j>
<j>He said, The kingdom of heaven is near.</j>
8 <j>Heal the sick.</j>
<j>Raise the dead.</j>
<j>Make those with leprosy clean.</j>
<j>Drive out demons.</j>
<j>Freely you have received, freely give.</j>
9 <j>Do not take any gold or silver or copper in your belts.</j>
10 <j>Do not take a bag for the journey, or two shirts, or sandals, or a walking stick.</j>
<j>A worker is worthy of his food.</j>
11 <j>Whatever town or village you enter, look for a good person there.</j>
<j>Stay at their house until you leave.</j>
12 <j>As you enter the home, greet them.</j>
13 <j>If the home is worthy, let your peace come upon it.</j>
<j>If not, let your peace return to you.</j>
14 <j>If anyone does not welcome you or listen to your words, leave that home or town.</j>
<j>Shake the dust off your feet.</j>
15 <j>I tell you the truth, it will be easier for Sodom and Gomorrah on the day of judgment than for that town.</j>
16 <j>I am sending you out like sheep among wolves.</j>
<j>So be as wise as snakes and as harmless as doves.</j>
17 <j>Watch out for people.</j>
<j>They will hand you over to courts.</j>
<j>They will whip you in their meeting places.</j>
18 <j>You will be brought before rulers and kings because of me.</j>
<j>You will be a witness to them and to the Gentiles.</j>
19 <j>But when they arrest you, do not worry about what to say or how to say it.</j>
<j>At that time you will be given what to say.</j>
20 <j>It will not be you speaking, but the Spirit of your Father speaking through you.</j>
21 <j>A brother will betray his brother to death.</j>
<j>A father will betray his child.</j>
<j>Children will rise up against parents and have them put to death.</j>
22 <j>All people will hate you because of me.</j>
<j>But the one who stands firm to the end will be saved.</j>
23 <j>When you are chased in one place, run to another.</j>
<j>I tell you the truth, you will not finish going through the cities of Israel before the Son of Man comes.</j>
24 <j>A student is not above his teacher.</j>
<j>And a servant is not above his master.</j>
25 <j>It is enough for the student to be like his teacher.</j>
<j>And for the servant to be like his master.</j>
<j>If the head of the house has been called Beelzebub, how much more will those in his house be called that!</j>
26 <j>So do not be afraid of them.</j>
<j>There is nothing hidden that will not be made known.</j>
<j>And nothing secret that will not come out into the open.</j>
27 <j>What I tell you in the dark, speak in the daylight.</j>
<j>What is whispered in your ear, preach from the roofs.</j>
28 <j>Do not be afraid of those who kill the body but cannot kill the soul.</j>
<j>Be afraid of the one who can destroy both soul and body in hell.</j>
29 <j>Are not two sparrows sold for a small coin?</j>
<j>Yet not one of them will fall to the ground without your Father knowing.</j>
30 <j>And even the hairs on your head are all counted.</j>
31 <j>So do not be afraid.</j>
<j>You are worth more than many sparrows.</j>
32 <j>Whoever says before people that he belongs to me, I will also say before my Father in heaven that he belongs to me.</j>
33 <j>But whoever says before people that he does not know me, I will also say before my Father in heaven that I do not know him.</j>
34 <j>Do not think that I came to bring peace on earth.</j>
<j>I did not come to bring peace, but a sword.</j>
35 <j>I came to turn a man against his father, a daughter against her mother, a daughter-in-law against her mother-in-law.</j>
36 <j>A man's enemies will be those in his own house.</j>
37 <j>Anyone who loves father or mother more than me is not worthy of me.</j>
<j>Anyone who loves son or daughter more than me is not worthy of me.</j>
38 <j>And anyone who does not take his cross and follow me is not worthy of me.</j>
39 <j>Whoever finds his life will lose it.</j>
<j>And whoever loses his life for me will find it.</j>
40 <j>Anyone who welcomes you welcomes me.</j>
<j>And anyone who welcomes me welcomes the one who sent me.</j>
41 <j>Anyone who welcomes a prophet because he is a prophet will receive a prophet's reward.</j>
<j>And anyone who welcomes a good person because he is good will receive a good person's reward.</j>
42 <j>And if anyone gives even a cup of cold water to one of these little ones because he is my follower, I tell you the truth, he will certainly not lose his reward.</j>

@11 Jesus and John the Baptist
1 After Jesus finished teaching his twelve followers, he left there.
He went to teach and preach in their towns.
2 John the Baptist was in prison.
He heard about what Christ was doing.
He sent two of his followers to Jesus.
3 They asked, Are you the one who was to come?
Or should we look for someone else?
4 Jesus answered them, <j>Go back and report to John what you hear and see.</j>
5 <j>Blind people see again.</j>
<j>Those who could not walk, walk.</j>
<j>Those with leprosy are made clean.</j>
<j>Deaf people hear.</j>
<j>Dead people are raised to life.</j>
<j>And good news is preached to poor people.</j>
6 <j>God blesses the one who is not offended by me.</j>
7 As John's followers were leaving, Jesus began to talk to the crowd about John.
He said, <j>What did you go out into the desert to see?</j>
<j>A reed swayed by the wind?</j>
8 <j>What did you go out to see?</j>
<j>A man dressed in soft clothes?</j>
<j>No, people who wear soft clothes are in kings' houses.</j>
9 <j>What did you go out to see?</j>
<j>A prophet?</j>
<j>Yes, I tell you, and more than a prophet.</j>
10 <j>This is the one it is written about.</j>
<j>It says, Look, I send my messenger ahead of you.</j>
<j>He will prepare your way before you.</j>
11 <j>I tell you the truth, no one born of a woman is greater than John the Baptist.</j>
<j>But the least important in the kingdom of heaven is greater than he is.</j>
12 <j>From the days of John the Baptist until now, the kingdom of heaven has been forcefully advancing.</j>
<j>And forceful people are taking hold of it.</j>
13 <j>All the Prophets and the Law spoke until John came.</j>
14 <j>And if you are willing to accept it, John is Elijah.</j>
<j>Elijah was the one who was to come.</j>
15 <j>Whoever has ears to hear, let them hear.</j>
16 <j>What can I compare this generation to?</j>
<j>It is like children sitting in the market places.</j>
<j>They call out to others.</j>
17 <j>They say, We played the flute for you, and you did not dance.</j>
<j>We sang a sad song, and you did not cry.</j>
18 <j>John came, not eating or drinking, and people say, He has a demon.</j>
19 <j>The Son of Man came eating and drinking, and people say, Look, a man who eats too much and drinks too much wine! A friend of tax collectors and sinners!</j>
<j>But wisdom is proved right by her actions.</j>
20 Then Jesus began to rebuke the cities where most of his miracles had been done.
They did not turn back to God.
21 He said, <j>How terrible for you, Chorazin!</j>
<j>How terrible for you, Bethsaida!</j>
<j>If the miracles done in you had been done in Tyre and Sidon, they would have turned back to God long ago.</j>
<j>They would have worn sackcloth and ashes.</j>
22 <j>I tell you, it will be easier for Tyre and Sidon on the day of judgment than for you.</j>
23 <j>And you, Capernaum, will you be lifted up to heaven?</j>
<j>No, you will go down to hell.</j>
<j>If the miracles done in you had been done in Sodom, it would still be here today.</j>
24 <j>I tell you, it will be easier for Sodom on the day of judgment than for you.</j>
25 At that time Jesus said, <j>I praise you, Father, Lord of heaven and earth.</j>
<j>You have hidden these things from wise and learned people.</j>
<j>You have shown them to little children.</j>
26 <j>Yes, Father, this is what you wanted.</j>
27 <j>My Father has given all things to me.</j>
<j>No one knows the Son except the Father.</j>
<j>And no one knows the Father except the Son.</j>
<j>And no one knows the Father except those the Son chooses to show him.</j>
28 <j>Come to me, all of you who are tired and carry heavy loads.</j>
<j>I will give you rest.</j>
29 <j>Take my yoke upon you and learn from me.</j>
<j>I am gentle and humble in heart.</j>
<j>And you will find rest for your souls.</j>
30 <j>My yoke is easy.</j>
<j>My load is light.</j>

@12 Lord of the Sabbath
1 At that time Jesus went through the grain fields on the Sabbath day.
His followers were hungry.
They began to pick heads of grain and eat them.
2 The Pharisees saw this and said to him, Look!
Your followers are doing what is not lawful on the Sabbath.
3 He said to them, <j>Have you not read what David did when he and those with him were hungry?</j>
4 <j>He entered the house of God.</j>
<j>He ate the holy bread.</j>
<j>It was not lawful for him to eat it, nor for those with him.</j>
<j>Only priests could eat it.</j>
5 <j>Or have you not read in the Law that on the Sabbath day the priests in the temple break the Sabbath law, yet are not guilty?</j>
6 <j>I tell you, something greater than the temple is here.</j>
7 <j>If you had known what this means, I desire mercy and not sacrifice, you would not have condemned innocent people.</j>
8 <j>The Son of Man is Lord of the Sabbath.</j>
9 He left that place and went into their meeting place.
10 A man was there with a dried-up hand.
The Pharisees asked Jesus, Is it lawful to heal on the Sabbath?
They wanted to accuse him.
11 He said to them, <j>If any of you has a sheep, and it falls into a pit on the Sabbath, will you not take hold of it and lift it out?</j>
12 <j>How much more valuable is a person than a sheep!</j>
<j>So it is lawful to do good on the Sabbath.</j>
13 Then he said to the man, <j>Stretch out your hand.</j>
He stretched it out.
And his hand was made well, just like the other one.
14 But the Pharisees went out and made plans to destroy Jesus.
15 Jesus knew this, so he left there.
A large crowd followed him.
He healed all who were sick.
16 He warned them not to tell who he was.
17 This was to make come true what the prophet Isaiah said.
18 He said, Here is my Servant, whom I have chosen.
The one I love, in whom I am very pleased.
I will put my Spirit on him.
He will tell the nations what is right and fair.
19 He will not argue or cry out.
No one will hear his voice in the streets.
20 He will not break a bent reed.
He will not put out a dimly burning wick.
He will make what is right and fair win.
21 The nations will put their hope in his name.
22 Then a man was brought to Jesus who was blind and could not speak because a demon was in him.
Jesus healed him.
So the man who could not speak could now talk and see.
23 All the people were amazed.
They said, Could this be the Son of David?
24 But when the Pharisees heard this, they said, This man only drives out demons by Beelzebub, the ruler of demons.
25 Jesus knew what they were thinking.
He said to them, <j>Every kingdom that fights against itself will be destroyed.</j>
<j>And every city or house that fights against itself will not stand.</j>
26 <j>If Satan drives out Satan, he is divided against himself.</j>
<j>How then will his kingdom stand?</j>
27 <j>If I drive out demons by Beelzebub, by whom do your people drive them out?</j>
<j>So they will be your judges.</j>
28 <j>But if I drive out demons by the Spirit of God, then the kingdom of God has come upon you.</j>
29 <j>How can anyone enter a strong man's house and steal his things, unless he first ties up the strong man?</j>
<j>Then he can steal from his house.</j>
30 <j>Whoever is not with me is against me.</j>
<j>And whoever does not gather with me scatters.</j>
31 <j>So I tell you, every sin and evil word will be forgiven.</j>
<j>But speaking evil against the Spirit will not be forgiven.</j>
32 <j>Anyone who speaks a word against the Son of Man will be forgiven.</j>
<j>But anyone who speaks against the Holy Spirit will not be forgiven.</j>
<j>Not in this life, and not in the life to come.</j>
33 <j>Make a tree good, and its fruit will be good.</j>
<j>Or make a tree bad, and its fruit will be bad.</j>
<j>A tree is known by its fruit.</j>
34 <j>You brood of snakes!</j>
<j>How can you, who are evil, say anything good?</j>
<j>What is in the heart comes out of the mouth.</j>
35 <j>A good man brings good things out of the good that is stored in his heart.</j>
<j>An evil man brings evil things out of the evil that is stored in his heart.</j>
36 <j>I tell you, people will have to answer for every careless word they speak on the day of judgment.</j>
37 <j>By your words you will be called right with God.</j>
<j>And by your words you will be condemned.</j>
38 Then some teachers of the law and Pharisees said to him, Teacher, we want to see a sign from you.
39 He answered, <j>A wicked and unfaithful generation asks for a sign.</j>
<j>No sign will be given to it except the sign of the prophet Jonah.</j>
40 <j>Jonah was in the belly of a huge fish for three days and three nights.</j>
<j>In the same way, the Son of Man will be in the heart of the earth for three days and three nights.</j>
41 <j>The people of Nineveh will stand up on judgment day against this generation.</j>
<j>They will condemn it.</j>
<j>They turned back to God when Jonah preached.</j>
<j>And now one greater than Jonah is here.</j>
42 <j>The Queen of the South will rise up on judgment day against this generation.</j>
<j>She will condemn it.</j>
<j>She came from the ends of the earth to listen to Solomon's wisdom.</j>
<j>And now one greater than Solomon is here.</j>
43 <j>When an evil spirit comes out of a person, it goes through dry places looking for rest.</j>
<j>It finds none.</j>
44 <j>Then it says, I will return to the house I left.</j>
<j>It comes back and finds the house empty, clean, and put in order.</j>
45 <j>Then it goes and takes with it seven other spirits more evil than itself.</j>
<j>They go in and live there.</j>
<j>And the last state of that person is worse than the first.</j>
<j>That is how it will be with this wicked generation.</j>
46 While Jesus was still talking to the crowd, his mother and brothers stood outside.
They wanted to speak to him.
47 Someone told him, Your mother and brothers are outside.
They want to speak to you.
48 He answered, <j>Who is my mother? Who are my brothers?</j>
49 He pointed to his followers and said, <j>Look, here are my mother and my brothers.</j>
50 <j>Whoever does what my Father in heaven wants is my brother and sister and mother.</j>

@13 Stories of the Kingdom
1 That same day Jesus went out of the house and sat by the lake.
2 A very large crowd gathered around him.
So he got into a boat and sat in it.
And all the people stood on the shore.
3 He told them many things in stories.
He said, <j>A farmer went out to plant seeds.</j>
4 <j>As he scattered the seed, some fell along the path.</j>
<j>The birds came and ate it up.</j>
5 <j>Some fell on rocky ground, where there was not much soil.</j>
<j>It grew up quickly, because the soil was not deep.</j>
6 <j>But when the sun came up, the plants were burned.</j>
<j>They dried up because they had no root.</j>
7 <j>Other seed fell among thorns.</j>
<j>The thorns grew up and choked the plants.</j>
8 <j>Still other seed fell on good soil.</j>
<j>It made a crop.</j>
<j>Some made a hundred times more, some sixty, some thirty.</j>
9 <j>Whoever has ears, let them hear.</j>
10 The followers came to him and asked, Why do you speak to the people in stories?
11 He answered, <j>The secrets of the kingdom of heaven are given to you to know.</j>
<j>But not to them.</j>
12 <j>To those who have, more will be given.</j>
<j>They will have an abundance.</j>
<j>From those who have nothing, even what they have will be taken away.</j>
13 <j>This is why I speak to them in stories.</j>
<j>They look, but do not see.</j>
<j>They listen, but do not hear or understand.</j>
14 <j>In them what Isaiah said comes true.</j>
<j>He said, You will listen and listen, but never understand.</j>
<j>You will look and look, but never see.</j>
15 <j>The hearts of these people have become hard.</j>
<j>They hardly hear with their ears.</j>
<j>They have closed their eyes.</j>
<j>If they did not, they might see with their eyes, hear with their ears, understand with their hearts, and turn back to me, and I would heal them.</j>
16 <j>But God blesses your eyes because they see.</j>
<j>And your ears because they hear.</j>
17 <j>I tell you the truth, many prophets and good people longed to see what you see.</j>
<j>But they did not see it.</j>
<j>They longed to hear what you hear.</j>
<j>But they did not hear it.</j>
18 <j>So listen to what the story of the farmer means.</j>
19 <j>When anyone hears the message of the kingdom and does not understand it, the evil one comes.</j>
<j>He snatches away what was planted in their heart.</j>
<j>This is the seed planted along the path.</j>
20 <j>The seed on rocky ground is the person who hears the word and at once receives it with joy.</j>
21 <j>But they have no root.</j>
<j>They last only a short time.</j>
<j>When trouble or hard times come because of the word, they quickly fall away.</j>
22 <j>The seed among thorns is the person who hears the word.</j>
<j>But the worries of this life and the lie of riches choke the word.</j>
<j>It makes no fruit.</j>
23 <j>But the seed on good soil is the person who hears the word and understands it.</j>
<j>They make a crop.</j>
<j>Some make a hundred times more, some sixty, some thirty.</j>
24 Jesus told them another story.
He said, <j>The kingdom of heaven is like a man who planted good seed in his field.</j>
25 <j>But while everyone was sleeping, his enemy came.</j>
<j>He planted weeds among the wheat and went away.</j>
26 <j>When the wheat grew and made heads of grain, the weeds also appeared.</j>
27 <j>The owner's servants came to him and said, Sir, did you not plant good seed in your field?</j>
<j>Where then did the weeds come from?</j>
28 <j>He said, An enemy did this.</j>
<j>The servants asked, Do you want us to go and pull them up?</j>
29 <j>He said, No.</j>
<j>If you pull up the weeds, you might pull up the wheat with them.</j>
30 <j>Let both grow together until the harvest.</j>
<j>At harvest time I will tell the harvesters, First collect the weeds.</j>
<j>Tie them in bundles to be burned.</j>
<j>Then gather the wheat and bring it into my barn.</j>
31 He told them another story.
He said, <j>The kingdom of heaven is like a mustard seed.</j>
<j>A man took it and planted it in his field.</j>
32 <j>It is the smallest of all seeds.</j>
<j>But when it grows, it is the largest of garden plants.</j>
<j>It becomes a tree.</j>
<j>The birds come and make nests in its branches.</j>
33 He told them still another story.
He said, <j>The kingdom of heaven is like yeast.</j>
<j>A woman took it and mixed it into a large amount of flour.</j>
<j>It worked through all the dough.</j>
34 Jesus spoke all these things to the crowd in stories.
He did not say anything to them without using a story.
35 So what was spoken through the prophet came true.
He said, I will open my mouth in stories.
I will speak things hidden since the creation of the world.
36 Then Jesus left the crowd and went into the house.
His followers came to him and said, Explain to us the story of the weeds in the field.
37 He answered, <j>The one who planted the good seed is the Son of Man.</j>
38 <j>The field is the world.</j>
<j>The good seed stands for the people of the kingdom.</j>
<j>The weeds are the people who belong to the evil one.</j>
39 <j>The enemy who planted the weeds is the devil.</j>
<j>The harvest is the end of the age.</j>
<j>And the harvesters are angels.</j>
40 <j>As the weeds are pulled up and burned, so it will be at the end of the age.</j>
41 <j>The Son of Man will send out his angels.</j>
<j>They will pull out of his kingdom everything that causes sin and all who do evil.</j>
42 <j>They will throw them into a blazing furnace.</j>
<j>There will be weeping and grinding of teeth there.</j>
43 <j>Then good people will shine like the sun in the kingdom of their Father.</j>
<j>Whoever has ears, let them hear.</j>
44 <j>The kingdom of heaven is like treasure hidden in a field.</j>
<j>When a man found it, he hid it again.</j>
<j>In his joy, he went and sold all he had and bought that field.</j>
45 <j>Again, the kingdom of heaven is like a merchant looking for fine pearls.</j>
46 <j>When he found one of great value, he went away and sold everything he had and bought it.</j>
47 <j>Again, the kingdom of heaven is like a net that was let down into the lake.</j>
<j>It caught all kinds of fish.</j>
48 <j>When it was full, the fishermen pulled it up on the shore.</j>
<j>Then they sat down and collected the good fish into baskets.</j>
<j>But they threw the bad away.</j>
49 <j>This is how it will be at the end of the age.</j>
<j>The angels will come and separate the evil people from the good.</j>
50 <j>They will throw evil people into a blazing furnace.</j>
<j>There will be weeping and grinding of teeth there.</j>
51 Have you understood all these things? Jesus asked.
Yes, they replied.
52 He said to them, <j>Every teacher of the law who has been taught about the kingdom of heaven is like the owner of a house.</j>
<j>He brings out new treasures as well as old.</j>
53 When Jesus had finished these stories, he left there.
54 He went to his hometown and began teaching in their meeting place.
The people were amazed and said, Where did this man get this wisdom and these mighty works?
55 Is this not the carpenter's son?
Is his mother not called Mary?
Are his brothers not James, Joseph, Simon, and Judas?
56 Are not all his sisters with us?
Where then did this man get all these things?
57 And they were offended by him.
But Jesus said to them, <j>A prophet is not without honor except in his hometown and in his own house.</j>
58 And he did not do many miracles there because of their lack of faith.

@14 Feeding 5000 and Walking on Water
1 At that time Herod the ruler heard about Jesus.
2 He said to his servants, This is John the Baptist.
He has been raised from the dead.
That is why these powers are at work in him.
3 Herod had arrested John.
He had tied him up and put him in prison because of Herodias, his brother Philip's wife.
4 John had been saying to him, It is not lawful for you to have her.
5 Herod wanted to kill John, but he was afraid of the people.
They thought John was a prophet.
6 On Herod's birthday, the daughter of Herodias danced before them.
She pleased Herod.
7 So he promised with an oath to give her whatever she asked.
8 She was prompted by her mother.
She said, Give me here on a platter the head of John the Baptist.
9 The king was sorry.
But because of his oaths and his dinner guests, he ordered it to be given to her.
10 He sent and had John beheaded in the prison.
11 His head was brought on a platter and given to the girl.
And she took it to her mother.
12 John's followers came and took his body and buried it.
Then they went and told Jesus.
13 When Jesus heard this, he left there by boat.
He went to a lonely place by himself.
The crowds heard about this and followed him on foot from the towns.
14 When Jesus got out of the boat, he saw a large crowd.
He had pity on them and healed their sick.
15 When evening came, his followers came to him and said,
This is a lonely place, and the day is already over.
Send the crowds away so they can go to the villages and buy food for themselves.
16 Jesus said to them, <j>They do not need to go away.</j>
<j>You give them something to eat.</j>
17 They said to him, We have here only five loaves of bread and two fish.
18 He said, <j>Bring them here to me.</j>
19 He told the people to sit down on the grass.
Then he took the five loaves and two fish.
He looked up to heaven and blessed them.
He broke the loaves and gave them to his followers, and the followers gave them to the people.
20 They all ate and were satisfied.
Then the followers picked up twelve baskets full of broken pieces that were left over.
21 The number of those who ate was about five thousand men, besides women and children.
22 Right away Jesus made his followers get into the boat and go ahead of him to the other side, while he sent the crowds away.
23 After he had sent them away, he went up on a mountain by himself to pray.
When evening came, he was there alone.
24 The boat was already far from land.
It was beaten by the waves, because the wind was against it.
25 About the fourth watch of the night, Jesus went to them, walking on the lake.
26 When the followers saw him walking on the lake, they were scared.
They said, It is a ghost!
And they cried out in fear.
27 Right away Jesus spoke to them.
He said, <j>Take courage! It is I. Do not be afraid.</j>
28 Peter answered him, Lord, if it is you, tell me to come to you on the water.
29 Jesus said, <j>Come.</j>
Peter got down out of the boat and walked on the water toward Jesus.
30 But when he saw the strong wind, he was afraid.
He began to sink and cried out, Lord, save me!
31 Right away Jesus reached out his hand and caught him.
He said to him, <j>You of little faith, why did you doubt?</j>
32 When they climbed into the boat, the wind died down.
33 Then those in the boat worshiped him.
They said, Truly you are the Son of God!
34 When they had crossed over, they landed at Gennesaret.
35 The men of that place recognized Jesus.
They sent word to all the nearby area.
They brought to him all who were sick.
36 They begged him to let the sick just touch the edge of his coat.
And all who touched it were healed.

@15 What Makes a Person Unclean
1 Then Pharisees and teachers of the law came from Jerusalem to Jesus.
They asked,
2 Why do your followers break the rules of the elders?
They do not wash their hands before they eat!
3 Jesus answered them, <j>And why do you break the command of God because of your rules?</j>
4 <j>For God said, Honor your father and mother.</j>
<j>And, Anyone who speaks evil of father or mother must be put to death.</j>
5 <j>But you say, If anyone says to his father or mother, Whatever help you might have received from me is a gift set aside for God,</j>
6 <j>then he does not have to honor his father or mother.</j>
<j>So you cancel the word of God because of your rules.</j>
7 <j>You fake leaders!</j>
<j>Isaiah was right when he prophesied about you.</j>
8 <j>He said, These people honor me with their lips, but their hearts are far from me.</j>
9 <j>Their worship of me is useless.</j>
<j>Their teachings are rules made by men.</j>
10 Jesus called the crowd to him and said, <j>Listen and understand.</j>
11 <j>What goes into a person's mouth does not make them unclean.</j>
<j>What comes out of the mouth does.</j>
12 Then his followers came and said to him, Do you know that the Pharisees were offended when they heard this?
13 He answered, <j>Every plant that my Father in heaven has not planted will be pulled up by the roots.</j>
14 <j>Leave them.</j>
<j>They are blind guides of blind people.</j>
<j>If a blind person leads a blind person, both will fall into a pit.</j>
15 Peter said to him, Explain the story to us.
16 Jesus said, <j>Are you still so dull?</j>
17 <j>Do you not see that whatever goes into the mouth goes into the stomach and then out of the body?</j>
18 <j>But what comes out of the mouth comes from the heart.</j>
<j>And it makes a person unclean.</j>
19 <j>For out of the heart come evil thoughts, murder, adultery, sexual sins, stealing, lying, and slander.</j>
20 <j>These are what make a person unclean.</j>
<j>But eating with unwashed hands does not make them unclean.</j>
21 Jesus left that place and went to the area of Tyre and Sidon.
22 A Canaanite woman from that area came.
She cried out, Lord, Son of David, have mercy on me!
My daughter is suffering terribly because a demon is in her!
23 Jesus did not answer her.
Then his followers came and begged him, Send her away, for she keeps crying out after us.
24 He answered, <j>I was sent only to the lost sheep of Israel.</j>
25 The woman came and knelt before him.
She said, Lord, help me!
26 He said, <j>It is not right to take the children's bread and toss it to the dogs.</j>
27 She said, Yes, Lord, but even the dogs eat the crumbs that fall from their masters' table.
28 Then Jesus answered her, <j>Woman, you have great faith!</j>
<j>It will be done for you as you wish.</j>
And her daughter was healed from that very hour.
29 Jesus left there and went along the Sea of Galilee.
Then he went up on a mountain and sat down.
30 Great crowds came to him.
They brought those who could not walk, blind people, those who could not speak, crippled people, and many others.
They laid them at Jesus' feet, and he healed them.
31 The people were amazed.
They saw those who could not speak speaking, crippled people made well, those who could not walk walking, and blind people seeing.
And they praised the God of Israel.
32 Jesus called his followers to him and said,
<j>I have pity on the crowd.</j>
<j>They have been with me three days and have nothing to eat.</j>
<j>I do not want to send them away hungry, or they will faint on the way.</j>
33 His followers said to him, Where can we get enough bread in this lonely place to feed so many people?
34 Jesus asked them, <j>How many loaves do you have?</j>
They said, Seven, and a few small fish.
35 He told the crowd to sit down on the ground.
36 Then he took the seven loaves and the fish.
He gave thanks, broke them, and gave them to his followers, and his followers gave them to the crowd.
37 They all ate and were satisfied.
Afterward, the followers picked up seven baskets full of broken pieces that were left over.
38 Those who ate were four thousand men, besides women and children.
39 After Jesus had sent the crowd away, he got into the boat and went to the area of Magdala.

@16 Peter Says Jesus is the Christ
1 The Pharisees and Sadducees came to Jesus.
They tested him by asking him to show them a sign from heaven.
2 He answered, <j>When evening comes, you say, It will be fair weather, for the sky is red.</j>
3 <j>And in the morning, It will be stormy today, for the sky is red and overcast.</j>
<j>You know how to tell what the sky means, but you cannot tell the signs of the times.</j>
4 <j>A wicked and unfaithful generation looks for a sign.</j>
<j>But no sign will be given to it except the sign of the prophet Jonah.</j>
Then he left them and went away.
5 When his followers went to the other side, they forgot to take bread.
6 Jesus said to them, <j>Be careful.</j>
<j>Watch out for the yeast of the Pharisees and Sadducees.</j>
7 They talked about this among themselves and said, It is because we did not bring bread.
8 Jesus knew this and said, <j>You of little faith, why are you talking among yourselves about having no bread?</j>
9 <j>Do you still not understand?</j>
<j>Do you not remember the five loaves for the five thousand, and how many baskets you gathered?</j>
10 <j>Or the seven loaves for the four thousand, and how many baskets you gathered?</j>
11 <j>How can you not understand that I was not talking to you about bread?</j>
<j>But watch out for the yeast of the Pharisees and Sadducees.</j>
12 Then they understood that he was not telling them to watch out for yeast used in bread.
He meant the teaching of the Pharisees and Sadducees.
13 When Jesus came to the area of Caesarea Philippi, he asked his followers,
<j>Who do people say the Son of Man is?</j>
14 They said, Some say John the Baptist, some say Elijah, and others say Jeremiah or one of the prophets.
15 He said to them, <j>But what about you?</j>
<j>Who do you say I am?</j>
16 Simon Peter answered, You are the Christ, the Son of the living God.
17 Jesus said to him, <j>God blesses you, Simon son of Jonah!</j>
<j>Flesh and blood did not show this to you.</j>
<j>My Father in heaven showed it to you.</j>
18 <j>And I tell you, you are Peter, which means rock.</j>
<j>On this rock I will build my church.</j>
<j>And the gates of hell will not beat it.</j>
19 <j>I will give you the keys of the kingdom of heaven.</j>
<j>What you tie on earth will be tied in heaven.</j>
<j>What you untie on earth will be untied in heaven.</j>
20 Then he warned his followers not to tell anyone that he was the Christ.
21 From that time on Jesus began to show his followers that he must go to Jerusalem.
He must suffer many things from the elders, chief priests, and teachers of the law.
He must be killed and on the third day be raised to life.
22 Peter took him aside and began to rebuke him.
He said, Never, Lord! This will never happen to you!
23 Jesus turned and said to Peter, <j>Get behind me, Satan!</j>
<j>You are a stumbling block to me.</j>
<j>You do not have in mind the things of God, but the things of men.</j>
24 Then Jesus said to his followers, <j>If anyone wants to come after me, he must deny himself, take up his cross, and follow me.</j>
25 <j>Whoever wants to save his life will lose it.</j>
<j>But whoever loses his life for me will find it.</j>
26 <j>What good will it be for a man if he gains the whole world, yet loses his soul?</j>
<j>Or what can a man give in exchange for his soul?</j>
27 <j>The Son of Man will come in his Father's glory with his angels.</j>
<j>Then he will reward each person for what they have done.</j>
28 <j>I tell you the truth, some who are standing here will not die before they see the Son of Man coming in his kingdom.</j>

@17 The Bright Glory of Jesus
1 After six days Jesus took Peter, James, and John the brother of James.
He led them up a high mountain by themselves.
2 There he was changed before them.
His face shone like the sun.
And his clothes became white as light.
3 Just then Moses and Elijah appeared before them.
They were talking with Jesus.
4 Peter said to Jesus, Lord, it is good for us to be here.
If you wish, I will make three shelters.
One for you, one for Moses, and one for Elijah.
5 While he was still speaking, a bright cloud covered them.
A voice from the cloud said, This is my dear Son.
I am very pleased with him.
Listen to him!
6 When the followers heard this, they fell face down on the ground.
They were very afraid.
7 But Jesus came and touched them.
He said, <j>Get up. Do not be afraid.</j>
8 When they looked up, they saw no one except Jesus alone.
9 As they came down the mountain, Jesus told them,
<j>Do not tell anyone what you have seen until the Son of Man has been raised from the dead.</j>
10 The followers asked him, Why do the teachers of the law say that Elijah must come first?
11 Jesus answered, <j>Elijah is coming and will make all things right again.</j>
12 <j>But I tell you, Elijah has already come.</j>
<j>People did not recognize him.</j>
<j>They did to him whatever they wanted.</j>
<j>In the same way the Son of Man is going to suffer at their hands.</j>
13 Then the followers understood that he was talking to them about John the Baptist.
14 When they came to the crowd, a man came up to Jesus.
He fell on his knees before him.
15 He said, Lord, have mercy on my son!
He has seizures and suffers terribly.
He often falls into the fire and often into the water.
16 I brought him to your followers, but they could not heal him.
17 Jesus answered, <j>You unbelieving and stubborn people!</j>
<j>How long will I be with you?</j>
<j>How long will I put up with you?</j>
<j>Bring the boy here to me.</j>
18 Jesus spoke sharply to the demon.
The demon came out of him, and the boy was healed from that moment.
19 Then the followers came to Jesus in private and asked, Why could we not drive it out?
20 He said to them, <j>Because you have so little faith.</j>
<j>I tell you the truth, if you have faith as small as a mustard seed, you can say to this mountain, Move from here to there, and it will move.</j>
<j>Nothing will be impossible for you.</j>
21 <j>But this kind does not go out except by prayer and fasting.</j>
22 When they came together in Galilee, Jesus said to them,
<j>The Son of Man is going to be handed over to men.</j>
23 <j>They will kill him, and on the third day he will be raised to life.</j>
And the followers were filled with great sadness.
24 When they came to Capernaum, the collectors of the temple tax came to Peter.
They asked, Does your teacher not pay the temple tax?
25 Yes, he does, Peter answered.
When Peter came into the house, Jesus spoke first.
He asked, <j>What do you think, Simon?</j>
<j>From whom do kings of the earth collect fees or taxes?</j>
<j>From their own sons or from others?</j>
26 Peter said, From others.
Jesus said to him, <j>Then the sons are free.</j>
27 <j>But so that we do not offend them, go to the lake and throw out a line.</j>
<j>Take the first fish you catch.</j>
<j>Open its mouth and you will find a coin.</j>
<j>Take it and give it to them for my tax and yours.</j>

@18 Who is Greatest in Heaven
1 At that time the followers came to Jesus and asked, Who is the greatest in the kingdom of heaven?
2 He called a little child to him.
He placed the child among them.
3 He said, <j>I tell you the truth, unless you change and become like little children, you will never enter the kingdom of heaven.</j>
4 <j>So whoever takes the low place like this child is the greatest in the kingdom of heaven.</j>
5 <j>Whoever welcomes one such child in my name welcomes me.</j>
6 <j>But if anyone causes one of these little ones who believe in me to sin, it would be better for him to have a large millstone hung around his neck and to be drowned in the deep sea.</j>
7 <j>How terrible for the world because of things that cause people to sin!</j>
<j>Such things must come, but how terrible for the person who causes them!</j>
8 <j>If your hand or foot causes you to sin, cut it off and throw it away.</j>
<j>It is better to enter life crippled or lame than to have two hands or two feet and be thrown into eternal fire.</j>
9 <j>And if your eye causes you to sin, take it out and throw it away.</j>
<j>It is better to enter life with one eye than to have two eyes and be thrown into the fire of hell.</j>
10 <j>Be careful that you do not look down on one of these little ones.</j>
<j>I tell you, their angels in heaven always see the face of my Father in heaven.</j>
11 <j>The Son of Man came to save what was lost.</j>
12 <j>What do you think?</j>
<j>If a man owns a hundred sheep, and one of them wanders away, will he not leave the ninety-nine on the hills and go look for the one that wandered off?</j>
13 <j>And if he finds it, I tell you the truth, he is happier about that one sheep than about the ninety-nine that did not wander off.</j>
14 <j>In the same way, your Father in heaven does not want any of these little ones to be lost.</j>
15 <j>If your brother sins against you, go and show him his fault, just between the two of you.</j>
<j>If he listens to you, you have won your brother.</j>
16 <j>But if he does not listen, take one or two others along.</j>
<j>Then every matter will be proved by two or three witnesses.</j>
17 <j>If he still refuses to listen, tell it to the church.</j>
<j>And if he refuses to listen even to the church, treat him as you would a pagan or a tax collector.</j>
18 <j>I tell you the truth, what you tie on earth will be tied in heaven.</j>
<j>What you untie on earth will be untied in heaven.</j>
19 <j>Again, I tell you that if two of you on earth agree about anything you ask for, it will be done for you by my Father in heaven.</j>
20 <j>For where two or three gather in my name, I am there with them.</j>
21 Then Peter came to Jesus and asked, Lord, how many times should I forgive my brother when he sins against me?
Up to seven times?
22 Jesus answered, <j>I tell you, not seven times, but seventy-seven times.</j>
23 <j>So the kingdom of heaven is like a king who wanted to settle accounts with his servants.</j>
24 <j>As he began to do this, a man who owed him ten thousand talents was brought to him.</j>
25 <j>He could not pay, so the master ordered that he and his wife and children and all that he had be sold to pay back what he owed.</j>
26 <j>The servant fell on his knees before him.</j>
<j>He said, Be patient with me, and I will pay back everything.</j>
27 <j>The master had pity on him.</j>
<j>He canceled the debt and let him go.</j>
28 <j>But when that servant went out, he found one of his fellow servants who owed him a hundred denarii.</j>
<j>He grabbed him and choked him.</j>
<j>He said, Pay back what you owe me!</j>
29 <j>His fellow servant fell down and begged him, Be patient with me, and I will pay you back.</j>
30 <j>But he refused.</j>
<j>Instead, he went off and had the man thrown into prison until he could pay back what he owed.</j>
31 <j>When the other servants saw what had happened, they were very sad.</j>
<j>They went and told their master everything.</j>
32 <j>Then the master called him in.</j>
<j>He said, You evil servant! I canceled all that debt of yours because you begged me to.</j>
33 <j>Should you not have had mercy on your fellow servant just as I had mercy on you?</j>
34 <j>In anger his master handed him over to the jailers to be punished until he should pay back all he owed.</j>
35 <j>This is how my Father in heaven will treat each of you unless you forgive your brother from your heart.</j>

@19 Marriage and Children
1 When Jesus finished saying these things, he left Galilee.
He went to the area of Judea across the Jordan River.
2 Large crowds followed him.
And he healed them there.
3 Some Pharisees came to him to test him.
They asked, Is it lawful for a man to divorce his wife for any reason?
4 He answered, <j>Have you not read that at the beginning the Maker made them male and female.</j>
5 <j>And he said, For this reason a man will leave his father and mother and be joined to his wife.</j>
<j>And the two will become one flesh.</j>
6 <j>So they are no longer two, but one flesh.</j>
<j>So what God has joined together, let no man separate.</j>
7 They asked him, Why then did Moses command to give a divorce paper and send her away?
8 Jesus said, <j>Moses let you divorce your wives because your hearts were hard.</j>
<j>But it was not this way from the beginning.</j>
9 <j>I tell you, anyone who divorces his wife except for sexual sin and marries another woman commits adultery.</j>
<j>And anyone who marries a divorced woman commits adultery.</j>
10 His followers said to him, If this is the way it is between husband and wife, it is better not to marry.
11 Jesus answered, <j>Not everyone can accept this teaching.</j>
<j>Only those to whom it is given can.</j>
12 <j>Some are unable to marry because they were born that way.</j>
<j>Some have been made that way by other people.</j>
<j>And some choose not to marry for the sake of the kingdom of heaven.</j>
<j>Whoever can accept this should accept it.</j>
13 Then little children were brought to Jesus.
They wanted him to place his hands on them and pray for them.
But the followers rebuked them.
14 Jesus said, <j>Let the little children come to me.</j>
<j>Do not keep them away.</j>
<j>The kingdom of heaven belongs to such as these.</j>
15 He placed his hands on them and went on from there.
16 A man came to Jesus and asked, Teacher, what good thing must I do to get eternal life?
17 Jesus said to him, <j>Why do you ask me about what is good?</j>
<j>There is only one who is good.</j>
<j>If you want to enter life, obey the commands.</j>
18 The man asked, Which ones?
Jesus said, <j>Do not murder.</j>
<j>Do not commit adultery.</j>
<j>Do not steal.</j>
<j>Do not lie.</j>
19 <j>Honor your father and mother.</j>
<j>And, Love your neighbor as yourself.</j>
20 The young man said to him, All these I have kept.
What else do I still lack?
21 Jesus said to him, <j>If you want to be perfect, go, sell what you have and give to the poor.</j>
<j>Then you will have treasure in heaven.</j>
<j>Then come, follow me.</j>
22 When the young man heard this, he went away sad.
He had great wealth.
23 Then Jesus said to his followers, <j>I tell you the truth, it is hard for a rich person to enter the kingdom of heaven.</j>
24 <j>Again I tell you, it is easier for a camel to go through the eye of a needle than for a rich person to enter the kingdom of God.</j>
25 When the followers heard this, they were very amazed.
They said, Who then can be saved?
26 Jesus looked at them and said, <j>With man this is impossible.</j>
<j>But with God all things are possible.</j>
27 Peter answered him, We have left everything and followed you.
What then will there be for us?
28 Jesus said to them, <j>I tell you the truth, when all things are made new and the Son of Man sits on his glorious throne, you who have followed me will also sit on twelve thrones.</j>
<j>You will judge the twelve tribes of Israel.</j>
29 <j>And everyone who has left houses or brothers or sisters or father or mother or wife or children or fields for my sake will receive a hundred times more and will inherit eternal life.</j>
30 <j>But many who are first will be last.</j>
<j>And many who are last will be first.</j>

@20 Workers in the Field and Jesus Will Die
1 <j>The kingdom of heaven is like a landowner.</j>
<j>He went out early in the morning to hire workers for his vineyard.</j>
2 <j>He agreed to pay them a denarius for the day.</j>
<j>And he sent them into his vineyard.</j>
3 <j>About nine in the morning, he went out and saw others standing in the market doing nothing.</j>
4 <j>He said to them, You also go and work in my vineyard.</j>
<j>And I will pay you what is right.</j>
5 <j>So they went.</j>
<j>He went out again about noon and about three in the afternoon.</j>
<j>And he did the same thing.</j>
6 <j>About five in the afternoon, he went out and found still others standing around.</j>
<j>He asked them, Why have you been standing here all day doing nothing?</j>
7 <j>They said to him, Because no one has hired us.</j>
<j>He said to them, You also go and work in my vineyard.</j>
8 <j>When evening came, the owner of the vineyard said to his manager, Call the workers.</j>
<j>Pay them their wages, beginning with the last ones hired and going on to the first.</j>
9 <j>The workers who were hired about five in the afternoon came.</j>
<j>Each received a denarius.</j>
10 <j>So when those hired first came, they expected to receive more.</j>
<j>But each one of them also received a denarius.</j>
11 <j>When they received it, they began to grumble against the landowner.</j>
12 <j>They said, These men who were hired last worked only one hour.</j>
<j>You have made them equal to us.</j>
<j>We have carried the heavy work and the heat of the day.</j>
13 <j>But he answered one of them, Friend, I am not being unfair to you.</j>
<j>Did you not agree to work for a denarius?</j>
14 <j>Take your pay and go.</j>
<j>I want to give the one who was hired last the same as I gave you.</j>
15 <j>Do I not have the right to do what I want with my own money?</j>
<j>Or are you jealous because I am generous?</j>
16 <j>So the last will be first, and the first will be last.</j>
17 As Jesus was going up to Jerusalem, he took the twelve followers aside by themselves.
On the way he said to them,
18 <j>We are going up to Jerusalem.</j>
<j>The Son of Man will be handed over to the chief priests and teachers of the law.</j>
<j>They will sentence him to death.</j>
19 <j>They will hand him over to the Gentiles.</j>
<j>They will make fun of him, whip him, and kill him on a cross.</j>
<j>But on the third day he will be raised to life.</j>
20 Then the mother of the sons of Zebedee came to him with her sons.
She knelt down and asked a favor of him.
21 He asked her, <j>What do you want?</j>
She said, Let one of these two sons of mine sit at your right and the other at your left in your kingdom.
22 Jesus answered, <j>You do not know what you are asking.</j>
<j>Can you drink the cup I am going to drink?</j>
They said, We can.
23 Jesus said to them, <j>You will drink my cup.</j>
<j>But to sit at my right or left is not for me to give.</j>
<j>It is for those my Father has prepared it for.</j>
24 When the other ten followers heard about this, they were angry with the two brothers.
25 Jesus called them together and said,
<j>You know that the rulers of the Gentiles lord it over them.</j>
<j>And their high officials make them feel their power.</j>
26 <j>It must not be this way among you.</j>
<j>Instead, whoever wants to be great among you must be your servant.</j>
27 <j>And whoever wants to be first must be your slave.</j>
28 <j>The Son of Man did not come to be served, but to serve.</j>
<j>And he came to give his life as a price to set many people free.</j>
29 As Jesus and his followers left Jericho, a large crowd followed him.
30 Two blind men were sitting by the roadside.
When they heard that Jesus was going by, they shouted, Lord, Son of David, have mercy on us!
31 The crowd rebuked them and told them to be quiet.
But they shouted all the louder, Lord, Son of David, have mercy on us!
32 Jesus stopped and called them.
He said, <j>What do you want me to do for you?</j>
33 They answered, Lord, we want to see again.
34 Jesus had pity on them.
He touched their eyes.
Right away they received their sight and followed him.

@21 Jesus Enters Jerusalem
1 As they came near Jerusalem, they came to Bethphage on the Mount of Olives.
Jesus sent two followers ahead.
2 He said to them, <j>Go into the village ahead of you.</j>
<j>Right away you will find a donkey tied, and a colt with her.</j>
<j>Untie them and bring them to me.</j>
3 <j>If anyone says anything to you, say, The Lord needs them.</j>
<j>And he will send them right away.</j>
4 This happened to make come true what the prophet said.
5 He said, Say to the daughter of Zion, Look, your King comes to you.
He is gentle, riding on a donkey, and on a colt, the foal of a donkey.
6 The followers went and did as Jesus told them.
7 They brought the donkey and the colt.
They placed their coats on them, and Jesus sat on them.
8 A very large crowd spread their coats on the road.
Others cut branches from trees and spread them on the road.
9 The crowds in front and behind shouted,
Hosanna to the Son of David!
God blesses him who comes in the name of the Lord!
Hosanna in the highest!
10 When Jesus entered Jerusalem, the whole city was stirred up.
People asked, Who is this?
11 The crowds said, This is Jesus, the prophet from Nazareth in Galilee.
12 Jesus entered the temple of God.
He drove out all who were buying and selling there.
He turned over the tables of those who changed money.
And the chairs of those who sold doves.
13 He said to them, <j>It is written, My house will be called a house of prayer.</j>
<j>But you are making it a den of robbers.</j>
14 The blind and those who could not walk came to him in the temple.
And he healed them.
15 The chief priests and teachers of the law saw the wonders he did.
They saw the children shouting in the temple, Hosanna to the Son of David!
And they were angry.
16 They said to him, Do you hear what these children are saying?
Jesus said, <j>Yes.</j>
<j>Have you never read, From the lips of children and babies, you have made praise?</j>
17 Then he left them and went out of the city to Bethany.
He spent the night there.
18 Early in the morning, as he came back to the city, he was hungry.
19 He saw a fig tree by the road.
He went to it, but found nothing but leaves.
He said to it, <j>May you never make fruit again!</j>
And right away the fig tree dried up.
20 When the followers saw this, they were amazed.
They said, How did the fig tree dry up so quickly?
21 Jesus answered, <j>I tell you the truth, if you have faith and do not doubt, you can do what was done to the fig tree.</j>
<j>You can even say to this mountain, Go, throw yourself into the sea, and it will happen.</j>
22 <j>If you believe, you will receive whatever you ask for in prayer.</j>
23 Jesus entered the temple.
As he taught, the chief priests and elders came to him.
They asked, By what authority are you doing these things?
Who gave you this authority?
24 Jesus answered, <j>I will also ask you one question.</j>
<j>If you answer me, I will tell you by what authority I do these things.</j>
25 <j>Where did John's baptism come from?</j>
<j>Was it from heaven, or from men?</j>
<j>They talked among themselves.</j>
<j>They said, If we say, From heaven, he will say, Why did you not believe him?</j>
26 But if we say, From men, we are afraid of the people.
They all think John was a prophet.
27 So they answered Jesus, We do not know.
Then he said, <j>Neither will I tell you by what authority I do these things.</j>
28 <j>What do you think?</j>
<j>A man had two sons.</j>
<j>He went to the first and said, Son, go and work today in the vineyard.</j>
29 <j>He answered, I will not.</j>
<j>But later he changed his mind and went.</j>
30 <j>Then the father went to the other son and said the same thing.</j>
<j>He answered, I will go, sir, but he did not go.</j>
31 <j>Which of the two did what his father wanted?</j>
The first, they answered.
Jesus said to them, <j>I tell you the truth, tax collectors and prostitutes are entering the kingdom of God ahead of you.</j>
32 <j>John came to show you the right way.</j>
<j>You did not believe him.</j>
<j>But tax collectors and prostitutes believed him.</j>
<j>And even after you saw this, you did not change your minds and believe him.</j>
33 <j>Listen to another story.</j>
<j>There was a landowner who planted a vineyard.</j>
<j>He put a wall around it, dug a pit for the winepress, and built a watchtower.</j>
<j>Then he rented it to farmers and went away on a journey.</j>
34 <j>When harvest time came, he sent his servants to the farmers to get his fruit.</j>
35 <j>The farmers took his servants.</j>
<j>They beat one, killed another, and stoned a third.</j>
36 <j>Then he sent other servants, more than the first time.</j>
<j>The farmers treated them the same way.</j>
37 <j>Last of all, he sent his son to them.</j>
<j>He said, They will respect my son.</j>
38 <j>But when the farmers saw the son, they said to each other, This is the heir.</j>
<j>Come, let us kill him and take his inheritance.</j>
39 <j>So they took him and threw him out of the vineyard and killed him.</j>
40 <j>So when the owner of the vineyard comes, what will he do to those farmers?</j>
41 They said to him, He will destroy those evil men.
And he will rent the vineyard to other farmers.
They will give him his share of the crop at harvest time.
42 Jesus said to them, <j>Have you never read in the Scriptures,</j>
<j>The stone that the builders rejected has become the most important stone.</j>
<j>The Lord has done this, and it is amazing to us.</j>
43 <j>So I tell you, the kingdom of God will be taken away from you and given to a people who will produce its fruit.</j>
44 <j>Anyone who falls on this stone will be broken to pieces.</j>
<j>Anyone on whom it falls will be crushed.</j>
45 When the chief priests and Pharisees heard his stories, they knew he was talking about them.
46 They looked for a way to arrest him, but they were afraid of the crowd.
The people thought Jesus was a prophet.

@22 Wedding Feast and Hard Questions
1 Jesus spoke to them again in stories.
He said,
2 <j>The kingdom of heaven is like a king who prepared a wedding feast for his son.</j>
3 <j>He sent his servants to call those who were invited to the feast.</j>
<j>But they refused to come.</j>
4 <j>Then he sent other servants.</j>
<j>He said, Tell those who are invited, Look, I have prepared my dinner.</j>
<j>My oxen and fat calves have been killed, and everything is ready.</j>
<j>Come to the wedding feast.</j>
5 <j>But they paid no attention and went away.</j>
<j>One went to his field, another to his business.</j>
6 <j>The rest seized his servants, mistreated them, and killed them.</j>
7 <j>The king was angry.</j>
<j>He sent his soldiers.</j>
<j>They destroyed those murderers and burned their city.</j>
8 <j>Then he said to his servants, The wedding feast is ready.</j>
<j>But those who were invited were not worthy.</j>
9 <j>So go to the street corners and invite anyone you find to the feast.</j>
10 <j>So the servants went out into the streets.</j>
<j>They gathered all the people they could find, both good and bad.</j>
<j>And the wedding hall was filled with guests.</j>
11 <j>But when the king came in to see the guests, he saw a man who was not wearing wedding clothes.</j>
12 <j>He asked him, Friend, how did you get in here without wedding clothes?</j>
<j>The man had nothing to say.</j>
13 <j>Then the king told the servants, Tie his hands and feet and throw him outside into the darkness.</j>
<j>There they will weep and grind their teeth.</j>
14 <j>Many are invited, but few are chosen.</j>
15 Then the Pharisees went out and made plans to trap Jesus with his words.
16 They sent their followers to him with the Herodians.
They said, Teacher, we know you are honest and teach the way of God truthfully.
You do not care what others think, for you look at no one to please them.
17 Tell us, what do you think?
Is it lawful to pay taxes to Caesar or not?
18 But Jesus knew their evil plan and said, <j>You fake leaders, why are you testing me?</j>
19 <j>Show me the coin used for the tax.</j>
They brought him a denarius.
20 He asked them, <j>Whose picture and name are on this coin?</j>
21 Caesar's, they answered.
Then he said to them, <j>So give to Caesar what belongs to Caesar, and to God what belongs to God.</j>
22 When they heard this, they were amazed.
So they left him and went away.
23 That same day the Sadducees, who say there is no resurrection, came to him.
They asked him,
24 Teacher, Moses said, If a man dies without children, his brother must marry his wife and have children for him.
25 There were seven brothers among us.
The first married and died without children.
He left his wife to his brother.
26 The same happened to the second and third, down to the seventh.
27 Last of all, the woman died.
28 So at the resurrection, whose wife will she be?
All seven had her as wife.
29 Jesus answered, <j>You are wrong because you do not know the Scriptures or the power of God.</j>
30 <j>At the resurrection, people will not marry nor be given in marriage.</j>
<j>They will be like angels in heaven.</j>
31 <j>But about the dead being raised, have you not read what God said to you?</j>
32 <j>He said, I am the God of Abraham, the God of Isaac, and the God of Jacob.</j>
<j>He is not the God of the dead, but of the living.</j>
33 When the crowds heard this, they were amazed at his teaching.
34 When the Pharisees heard that Jesus had silenced the Sadducees, they gathered together.
35 One of them, a teacher of the law, tested him with a question.
36 Teacher, which is the greatest command in the Law?
37 Jesus answered, <j>Love the Lord your God with all your heart, with all your soul, and with all your mind.</j>
38 <j>This is the first and greatest command.</j>
39 <j>The second is like it: Love your neighbor as yourself.</j>
40 <j>All the Law and the Prophets depend on these two commands.</j>
41 While the Pharisees were gathered, Jesus asked them,
42 <j>What do you think about the Christ?</j>
<j>Whose son is he?</j>
They said, The son of David.
43 He said to them, <j>How then does David, speaking by the Spirit, call him Lord?</j>
<j>For he says,</j>
44 <j>The Lord said to my Lord, Sit at my right hand until I put your enemies under your feet.</j>
45 <j>If David calls him Lord, how can he be his son?</j>
46 No one could answer him a word.
And from that day on, no one dared to ask him any more questions.

@23 Woe to Fake Leaders
1 Then Jesus spoke to the crowds and to his followers.
2 <j>He said, The teachers of the law and the Pharisees sit in Moses' seat.</j>
3 <j>So do and obey what they tell you.</j>
<j>But do not do what they do.</j>
<j>They do not practice what they preach.</j>
4 <j>They tie up heavy loads and put them on people's shoulders.</j>
<j>But they themselves are not willing to lift a finger to move them.</j>
5 <j>Everything they do is done to be seen by people.</j>
<j>They make their phylacteries wide and their tassels long.</j>
6 <j>They love the place of honor at feasts and the best seats in the meeting places.</j>
7 <j>They love to be greeted in the market places and to be called Rabbi by people.</j>
8 <j>But you are not to be called Rabbi.</j>
<j>You have one Teacher, and you are all brothers.</j>
9 <j>And do not call anyone on earth father.</j>
<j>You have one Father, and he is in heaven.</j>
10 <j>And you are not to be called teachers.</j>
<j>You have one Teacher, the Christ.</j>
11 <j>The greatest among you will be your servant.</j>
12 <j>Whoever lifts himself up will be brought down.</j>
<j>And whoever makes himself low will be lifted up.</j>
13 <j>How terrible for you, teachers of the law and Pharisees, you fake leaders!</j>
<j>You shut the kingdom of heaven in people's faces.</j>
<j>You yourselves do not enter, and you do not let those enter who are trying to.</j>
14 <j>How terrible for you, teachers of the law and Pharisees, you fake leaders!</j>
<j>You take over the houses of widows.</j>
<j>And you make long prayers to show off.</j>
<j>You will be punished much more.</j>
15 <j>How terrible for you, teachers of the law and Pharisees, you fake leaders!</j>
<j>You travel over land and sea to make one follower.</j>
<j>And when he becomes one, you make him twice as much a son of hell as you are.</j>
16 <j>How terrible for you, blind guides!</j>
<j>You say, If anyone swears by the temple, it means nothing.</j>
<j>But if anyone swears by the gold of the temple, he must keep his oath.</j>
17 <j>You blind fools!</j>
<j>Which is greater, the gold or the temple that makes the gold holy?</j>
18 <j>You also say, If anyone swears by the altar, it means nothing.</j>
<j>But if anyone swears by the gift on the altar, he must keep his oath.</j>
19 <j>You blind men! Which is greater, the gift or the altar that makes the gift holy?</j>
20 <j>So anyone who swears by the altar swears by it and by everything on it.</j>
21 <j>And anyone who swears by the temple swears by it and by the one who lives in it.</j>
22 <j>And anyone who swears by heaven swears by God's throne and by the one who sits on it.</j>
23 <j>How terrible for you, teachers of the law and Pharisees, you fake leaders!</j>
<j>You give a tenth of your spices, mint, dill, and cummin.</j>
<j>But you have neglected the more important matters of the Law.</j>
<j>That is, doing what is right and fair, showing mercy, and being faithful.</j>
<j>You should have done the latter, without neglecting the former.</j>
24 <j>You blind guides!</j>
<j>You strain out a gnat, but swallow a camel!</j>
25 <j>How terrible for you, teachers of the law and Pharisees, you fake leaders!</j>
<j>You clean the outside of the cup and dish.</j>
<j>But inside they are full of greed and selfish desire.</j>
26 <j>Blind Pharisee! First clean the inside of the cup and dish.</j>
<j>Then the outside will also be clean.</j>
27 <j>How terrible for you, teachers of the law and Pharisees, you fake leaders!</j>
<j>You are like whitewashed tombs.</j>
<j>You look beautiful on the outside.</j>
<j>But on the inside you are full of dead men's bones and all that is unclean.</j>
28 <j>In the same way, you look right and good to people on the outside.</j>
<j>But on the inside you are full of fake ways and evil.</j>
29 <j>How terrible for you, teachers of the law and Pharisees, you fake leaders!</j>
<j>You build tombs for the prophets and decorate the graves of good people.</j>
30 <j>And you say, If we had lived in the days of our fathers, we would not have taken part with them in killing the prophets.</j>
31 <j>So you prove that you are the children of those who murdered the prophets.</j>
32 <j>Fill up, then, the measure of your fathers' sin!</j>
33 <j>You snakes! You brood of vipers!</j>
<j>How will you escape being condemned to hell?</j>
34 <j>So I am sending you prophets, wise men, and teachers.</j>
<j>Some of them you will kill and nail to a cross.</j>
<j>Others you will whip in your meeting places.</j>
<j>And you will chase them from town to town.</j>
35 <j>So all the good blood shed on earth will be blamed on you.</j>
<j>From the blood of good Abel to the blood of Zechariah, son of Berechiah, whom you murdered between the temple and the altar.</j>
36 <j>I tell you the truth, all this will come upon this generation.</j>
37 <j>O Jerusalem, Jerusalem, you who kill the prophets and stone those sent to you!</j>
<j>How often I have wanted to gather your children together as a hen gathers her chicks under her wings.</j>
<j>But you were not willing.</j>
38 <j>Look, your house is left to you empty.</j>
39 <j>I tell you, you will not see me again until you say, God blesses him who comes in the name of the Lord.</j>

@24 Signs of the End
1 Jesus left the temple and was going away.
His followers came to him to show him the temple buildings.
2 He said to them, <j>Do you see all these things?</j>
<j>I tell you the truth, not one stone here will be left on another.</j>
<j>Every one will be thrown down.</j>
3 As Jesus sat on the Mount of Olives, his followers came to him in private.
They said, Tell us, when will these things happen?
What will be the sign of your coming and of the end of the age?
4 Jesus answered, <j>Watch out that no one fools you.</j>
5 <j>Many will come in my name.</j>
<j>They will say, I am the Christ, and will fool many people.</j>
6 <j>You will hear of wars and rumors of wars.</j>
<j>Do not be afraid.</j>
<j>Such things must happen, but the end is still to come.</j>
7 <j>Nation will rise against nation, and kingdom against kingdom.</j>
<j>There will be famines and earthquakes in many places.</j>
8 <j>All these are the beginning of birth pains.</j>
9 <j>Then you will be handed over to be hurt and killed.</j>
<j>You will be hated by all nations because of me.</j>
10 <j>At that time many will turn away from faith.</j>
<j>They will betray and hate each other.</j>
11 <j>Many false prophets will appear and fool many people.</j>
12 <j>Because evil will increase, the love of many will grow cold.</j>
13 <j>But the one who stands firm to the end will be saved.</j>
14 <j>This good news of the kingdom will be preached in the whole world.</j>
<j>It will be a witness to all nations.</j>
<j>Then the end will come.</j>
15 <j>So when you see the hated thing that destroys, spoken of by Daniel the prophet, standing in the holy place—let the reader understand—</j>
16 <j>then let those in Judea flee to the mountains.</j>
17 <j>Let no one on the roof go down to take anything out of his house.</j>
18 <j>Let no one in the field go back to get his coat.</j>
19 <j>How terrible for pregnant women and nursing mothers in those days!</j>
20 <j>Pray that your flight will not be in winter or on a Sabbath.</j>
21 <j>For then there will be great trouble, such as has not been from the beginning of the world until now, and never will be.</j>
22 <j>If those days had not been cut short, no one would survive.</j>
<j>But for the sake of those God has chosen, those days will be cut short.</j>
23 <j>At that time, if anyone says to you, Look, here is the Christ! or, There he is! do not believe it.</j>
24 <j>False Christs and false prophets will appear.</j>
<j>They will do great signs and wonders.</j>
<j>If possible, they would fool even those God has chosen.</j>
25 <j>See, I have told you ahead of time.</j>
26 <j>So if anyone tells you, He is in the desert, do not go out.</j>
<j>Or, He is in the inner rooms, do not believe it.</j>
27 <j>For as lightning that comes from the east is seen even in the west, so will be the coming of the Son of Man.</j>
28 <j>Wherever there is a dead body, there the vultures will gather.</j>
29 <j>Right after the trouble of those days,</j>
<j>The sun will be darkened,</j>
<j>The moon will not give its light,</j>
<j>The stars will fall from the sky,</j>
<j>And the powers of the heavens will be shaken.</j>
30 <j>Then the sign of the Son of Man will appear in the sky.</j>
<j>All peoples of the earth will mourn.</j>
<j>They will see the Son of Man coming on the clouds of the sky, with power and great glory.</j>
31 <j>He will send his angels with a loud trumpet call.</j>
<j>They will gather his chosen people from the four winds, from one end of the heavens to the other.</j>
32 <j>Learn this lesson from the fig tree.</j>
<j>As soon as its twigs get tender and its leaves come out, you know summer is near.</j>
33 <j>In the same way, when you see all these things, you know it is near, right at the door.</j>
34 <j>I tell you the truth, this generation will not pass away until all these things have happened.</j>
35 <j>Heaven and earth will pass away, but my words will never pass away.</j>
36 <j>No one knows the day or hour.</j>
<j>Not even the angels in heaven, nor the Son, but only the Father.</j>
37 <j>As it was in the days of Noah, so it will be at the coming of the Son of Man.</j>
38 <j>In the days before the flood, people were eating and drinking, marrying and giving in marriage, up to the day Noah entered the ark.</j>
39 <j>They knew nothing about what would happen until the flood came and took them all away.</j>
<j>That is how it will be at the coming of the Son of Man.</j>
40 <j>Two men will be in the field.</j>
<j>One will be taken and the other left.</j>
41 <j>Two women will be grinding with a hand mill.</j>
<j>One will be taken and the other left.</j>
42 <j>So keep watch, because you do not know what day your Lord will come.</j>
43 <j>But understand this: If the owner of the house had known when the thief was coming, he would have kept watch.</j>
<j>He would not have let his house be broken into.</j>
44 <j>So you also must be ready, because the Son of Man will come at an hour you do not expect him.</j>
45 <j>Who then is the faithful and wise servant?</j>
<j>His master puts him in charge of his other servants, to give them food at the right time.</j>
46 <j>It will be good for that servant if his master finds him doing so when he returns.</j>
47 <j>I tell you the truth, he will put him in charge of all he owns.</j>
48 <j>But suppose that servant is evil.</j>
<j>He says to himself, My master is staying away a long time.</j>
49 <j>Then he begins to beat his fellow servants.</j>
<j>He eats and drinks with those who drink too much.</j>
50 <j>The master of that servant will come on a day he does not expect and at an hour he does not know.</j>
51 <j>He will cut him to pieces and give him a place with the fake leaders.</j>
<j>There will be weeping and grinding of teeth there.</j>

@25 Ten Virgins, Talents, and Final Judgment
1 <j>Then the kingdom of heaven will be like ten virgins.</j>
<j>They took their lamps and went out to meet the groom.</j>
2 <j>Five of them were foolish and five were wise.</j>
3 <j>The foolish ones took their lamps but did not take any oil with them.</j>
4 <j>The wise ones took oil in jars along with their lamps.</j>
5 <j>The groom was a long time in coming.</j>
<j>They all became drowsy and fell asleep.</j>
6 <j>At midnight someone cried, Look, the groom is coming!</j>
<j>Come out to meet him!</j>
7 <j>Then all the virgins woke up and trimmed their lamps.</j>
8 <j>The foolish ones said to the wise, Give us some of your oil.</j>
<j>Our lamps are going out.</j>
9 <j>The wise answered, No, there may not be enough for both us and you.</j>
<j>Instead, go to those who sell oil and buy some for yourselves.</j>
10 <j>While they were on their way to buy oil, the groom arrived.</j>
<j>The virgins who were ready went in with him to the wedding feast.</j>
<j>And the door was shut.</j>
11 <j>Later the other virgins came.</j>
<j>They said, Sir! Sir! Open the door for us!</j>
12 <j>But he replied, I tell you the truth, I do not know you.</j>
13 <j>So keep watch, because you do not know the day or the hour.</j>
14 <j>Again, it will be like a man going on a journey.</j>
<j>He called his servants and gave his wealth to them.</j>
15 <j>To one he gave five talents of money, to another two talents, and to another one talent.</j>
<j>Each according to his ability.</j>
<j>Then he went on his journey.</j>
16 <j>The man who received five talents went at once and put his money to work.</j>
<j>He gained five more.</j>
17 <j>In the same way, the one with two talents gained two more.</j>
18 <j>But the man who received one talent went off, dug a hole in the ground and hid his master's money.</j>
19 <j>After a long time the master of those servants returned.</j>
<j>He settled accounts with them.</j>
20 <j>The man who received five talents brought the other five.</j>
<j>He said, Master, you gave me five talents.</j>
<j>See, I have gained five more.</j>
21 <j>His master said, Well done, good and faithful servant!</j>
<j>You have been faithful with a few things.</j>
<j>I will put you in charge of many things.</j>
<j>Come and share your master's joy!</j>
22 <j>The man with two talents also came.</j>
<j>He said, Master, you gave me two talents.</j>
<j>See, I have gained two more.</j>
23 <j>His master said, Well done, good and faithful servant!</j>
<j>You have been faithful with a few things.</j>
<j>I will put you in charge of many things.</j>
<j>Come and share your master's joy!</j>
24 <j>Then the man who received one talent came.</j>
<j>He said, Master, I knew you are a hard man.</j>
<j>You harvest where you have not planted.</j>
<j>And you gather where you have not scattered seed.</j>
25 <j>So I was afraid.</j>
<j>I went out and hid your talent in the ground.</j>
<j>See, here is what belongs to you.</j>
26 <j>His master answered, You wicked, lazy servant!</j>
<j>You knew I harvest where I have not planted and gather where I have not scattered seed?</j>
27 <j>Then you should have put my money with the bankers.</j>
<j>When I returned, I would have received it back with interest.</j>
28 <j>So take the talent from him and give it to the one who has ten talents.</j>
29 <j>To everyone who has, more will be given.</j>
<j>And he will have more than enough.</j>
<j>From the one who has nothing, even what he has will be taken away.</j>
30 <j>And throw that worthless servant outside into the darkness.</j>
<j>There they will weep and grind their teeth.</j>
31 <j>When the Son of Man comes in his glory, and all the holy angels with him, then he will sit on his glorious throne.</j>
32 <j>All nations will be gathered before him.</j>
<j>He will separate people one from another as a shepherd separates sheep from goats.</j>
33 <j>He will put the sheep on his right and the goats on his left.</j>
34 <j>Then the King will say to those on his right, Come, you who are blessed by my Father.</j>
<j>Take your inheritance, the kingdom prepared for you since the creation of the world.</j>
35 <j>For I was hungry and you gave me something to eat.</j>
<j>I was thirsty and you gave me something to drink.</j>
<j>I was a stranger and you invited me in.</j>
36 <j>I needed clothes and you clothed me.</j>
<j>I was sick and you looked after me.</j>
<j>I was in prison and you came to visit me.</j>
37 <j>Then the good people will answer him, Lord, when did we see you hungry and feed you?</j>
<j>When did we see you thirsty and give you drink?</j>
38 <j>When did we see you a stranger and invite you in?</j>
<j>When did we see you needing clothes and clothe you?</j>
39 <j>When did we see you sick or in prison and go to visit you?</j>
40 <j>The King will reply, I tell you the truth, whatever you did for one of the least of these brothers of mine, you did for me.</j>
41 <j>Then he will say to those on his left, Go away from me, you who are cursed, into the eternal fire prepared for the devil and his angels.</j>
42 <j>For I was hungry and you gave me nothing to eat.</j>
<j>I was thirsty and you gave me nothing to drink.</j>
43 <j>I was a stranger and you did not invite me in.</j>
<j>I needed clothes and you did not clothe me.</j>
<j>I was sick and in prison and you did not look after me.</j>
44 <j>They also will answer, Lord, when did we see you hungry or thirsty or a stranger or needing clothes or sick or in prison, and did not help you?</j>
45 <j>He will reply, I tell you the truth, whatever you did not do for one of the least of these, you did not do for me.</j>
46 <j>Then they will go away to eternal punishment.</j>
<j>But the good people will go to eternal life.</j>

@26 The Last Supper and Betrayal
1 When Jesus had finished all these words, he said to his followers,
2 <j>You know that after two days is the Passover.</j>
<j>The Son of Man will be handed over to be nailed to a cross.</j>
3 Then the chief priests and elders gathered in the palace of the high priest.
His name was Caiaphas.
4 They made plans to arrest Jesus by tricking him and kill him.
5 They said, Not during the feast, or there may be an uproar among the people.
6 While Jesus was in Bethany in the home of Simon who had leprosy,
7 a woman came to him with a jar of very expensive perfume.
She poured it on his head as he was eating.
8 When the followers saw this, they were angry.
They said, Why this waste?
9 This perfume could have been sold for a lot of money and given to the poor.
10 Jesus knew this and said to them, <j>Why are you bothering this woman?</j>
<j>She has done a beautiful thing for me.</j>
11 <j>You will always have the poor with you.</j>
<j>But you will not always have me.</j>
12 <j>When she poured this perfume on my body, she did it to prepare me for burial.</j>
13 <j>I tell you the truth, wherever this good news is preached in the whole world, what she has done will be told in memory of her.</j>
14 Then one of the twelve, named Judas Iscariot, went to the chief priests.
15 He said, What will you give me if I hand Jesus over to you?
So they counted out thirty silver coins for him.
16 From then on, Judas looked for a chance to hand Jesus over.
17 On the first day of the Feast of Bread Without Yeast, the followers came to Jesus.
They said, Where do you want us to make preparations for you to eat the Passover?
18 He said, <j>Go into the city to a certain man.</j>
<j>Tell him, The Teacher says, My set time is near.</j>
<j>I will celebrate the Passover at your house with my followers.</j>
19 The followers did as Jesus told them.
They prepared the Passover.
20 When evening came, Jesus was eating with the twelve.
21 While they were eating, he said, <j>I tell you the truth, one of you will hand me over.</j>
22 They were very sad.
Each one began to say to him, Surely not I, Lord?
23 Jesus answered, <j>The one who has dipped his hand into the bowl with me will hand me over.</j>
24 <j>The Son of Man will go as it is written about him.</j>
<j>But how terrible for the man who hands him over!</j>
<j>It would be better for him if he had not been born.</j>
25 Then Judas, who would hand him over, said, Surely not I, Rabbi?
Jesus answered, <j>Yes, it is you.</j>
26 While they were eating, Jesus took bread.
He gave thanks and broke it.
He gave it to his followers and said, <j>Take and eat.</j>
<j>This is my body.</j>
27 Then he took the cup.
He gave thanks and gave it to them.
He said, <j>Drink from it, all of you.</j>
28 <j>This is my blood of the covenant.</j>
<j>It is poured out for many for the forgiveness of sins.</j>
29 <j>I tell you, I will not drink of this fruit of the vine from now on until that day when I drink it anew with you in my Father's kingdom.</j>
30 When they had sung a hymn, they went out to the Mount of Olives.
31 Then Jesus said to them, <j>This very night you will all fall away because of me.</j>
<j>It is written, I will strike the shepherd, and the sheep of the flock will be scattered.</j>
32 <j>But after I am raised to life, I will go ahead of you into Galilee.</j>
33 Peter answered him, Even if all fall away because of you, I will never fall away.
34 Jesus said to him, <j>I tell you the truth, this very night, before the rooster crows, you will say three times that you do not know me.</j>
35 Peter said to him, Even if I have to die with you, I will never say I do not know you.
And all the other followers said the same.
36 Then Jesus went with his followers to a place called Gethsemane.
He said to them, <j>Sit here while I go over there and pray.</j>
37 He took Peter and the two sons of Zebedee with him.
He began to be sad and troubled.
38 Then he said to them, <j>My soul is very sad, even to death.</j>
<j>Stay here and keep watch with me.</j>
39 Going a little farther, he fell face down and prayed.
He said, <j>My Father, if it is possible, take this cup from me.</j>
<j>Yet not as I will, but as you will.</j>
40 Then he returned to his followers and found them sleeping.
He said to Peter, <j>Could you not keep watch with me for one hour?</j>
41 <j>Keep watch and pray, so that you will not enter into hard testing.</j>
<j>The spirit is willing, but the flesh is weak.</j>
42 He went away a second time and prayed, <j>My Father, if it is not possible for this cup to be taken away unless I drink it, may your will be done.</j>
43 When he came back, he again found them sleeping.
Their eyes were heavy.
44 So he left them and went away once more.
He prayed the third time, saying the same thing.
45 Then he returned to the followers and said to them, <j>Are you still sleeping and resting?</j>
<j>Look, the hour is near.</j>
<j>The Son of Man is handed over to sinners.</j>
46 <j>Get up! Let us go!</j>
<j>Here comes the one who will hand me over!</j>
47 While he was still speaking, Judas, one of the twelve, came.
With him was a large crowd with swords and clubs.
They came from the chief priests and elders of the people.
48 Now the one who would hand him over had given them a sign.
He said, The one I kiss is the man.
Arrest him.
49 Going at once to Jesus, Judas said, Greetings, Rabbi! And kissed him.
50 Jesus said to him, <j>Friend, do what you came to do.</j>
Then the men came, seized Jesus, and arrested him.
51 With that, one of Jesus' companions reached for his sword.
He struck the servant of the high priest and cut off his ear.
52 Jesus said to him, <j>Put your sword back.</j>
<j>All who draw the sword will die by the sword.</j>
53 <j>Do you think I cannot call on my Father?</j>
<j>He would at once send me more than twelve legions of angels.</j>
54 <j>But how then would the Scriptures come true?</j>
<j>It must happen this way.</j>
55 At that time Jesus said to the crowd, <j>Am I leading a rebellion that you have come with swords and clubs to capture me?</j>
<j>Every day I sat in the temple teaching, and you did not arrest me.</j>
56 <j>But this all happened so the writings of the prophets would come true.</j>
Then all the followers left him and ran away.
57 Those who arrested Jesus took him to Caiaphas the high priest.
The teachers of the law and elders were gathered there.
58 Peter followed him at a distance, right up to the courtyard of the high priest.
He entered and sat down with the guards to see how it would end.
59 The chief priests and the whole council looked for false evidence against Jesus so they could put him to death.
60 But they did not find any, though many false witnesses came forward.
Finally two came forward.
61 They said, This fellow said, I am able to destroy the temple of God and rebuild it in three days.
62 Then the high priest stood up and said to Jesus, Will you not answer?
What is this testimony against you?
63 But Jesus remained silent.
The high priest said to him, I command you by the living God.
Tell us if you are the Christ, the Son of God.
64 Jesus said, <j>Yes, it is as you say.</j>
<j>But I say to all of you, in the future you will see the Son of Man sitting at the right hand of the Mighty One and coming on the clouds of heaven.</j>
65 Then the high priest tore his clothes.
He said, He has spoken evil against God!
Why do we need any more witnesses?
Look, now you have heard him speak evil against God!
66 What do you think?
They answered, He is worthy of death.
67 Then they spit in his face and struck him with their fists.
Others slapped him.
68 They said, Prophesy to us, Christ! Who hit you?
69 Now Peter was sitting outside in the courtyard.
A servant girl came to him and said, You also were with Jesus of Galilee.
70 But he denied it before them all.
He said, I do not know what you are talking about.
71 Then he went out to the gate.
Another girl saw him and said to the people there, This fellow was with Jesus of Nazareth.
72 He denied it again with an oath, I do not know the man!
73 After a little while, those standing there went up to Peter.
They said, Surely you are one of them, for your speech shows it.
74 Then he began to call down curses on himself and swear, I do not know the man!
Right away a rooster crowed.
75 Then Peter remembered what Jesus had said.
He said, Before the rooster crows, you will say three times that you do not know me.
And he went outside and wept bitterly.

@27 Jesus on the Cross
1 Early in the morning, all the chief priests and elders made plans to put Jesus to death.
2 They tied him up, led him away, and handed him over to Pilate the ruler.
3 When Judas, who had handed him over, saw that Jesus was condemned, he felt deep regret.
He brought back the thirty silver coins to the chief priests and elders.
4 He said, I have sinned, for I have handed over innocent blood.
They said, What is that to us? That is your problem.
5 So Judas threw the money into the temple and left.
Then he went away and hanged himself.
6 The chief priests picked up the coins.
They said, It is against the law to put this money into the treasury, because it is blood money.
7 So they decided to use the money to buy the potter's field as a burial place for strangers.
8 That is why it has been called the Field of Blood to this day.
9 Then what was spoken by Jeremiah the prophet came true.
He said, They took the thirty silver coins, the price set on him by the people of Israel.
10 And they used them to buy the potter's field, as the Lord told me.
11 Jesus stood before the ruler.
The ruler asked him, Are you the King of the Jews?
Jesus said, <j>Yes, it is as you say.</j>
12 When the chief priests and elders accused him, he gave no answer.
13 Then Pilate asked him, Do you not hear how many charges they bring against you?
14 But Jesus made no reply, not even to a single charge.
The ruler was very amazed.
15 Now it was the custom at the feast for the ruler to release one prisoner chosen by the crowd.
16 At that time they had a well-known prisoner named Barabbas.
17 So when the crowd gathered, Pilate asked them, Who do you want me to release to you?
Barabbas, or Jesus who is called Christ?
18 For he knew they had handed Jesus over because they were jealous.
19 While Pilate sat on the judge's seat, his wife sent him a message.
She said, Do not have anything to do with that good man.
I suffered a lot today in a dream because of him.
20 But the chief priests and elders persuaded the crowd to ask for Barabbas and to have Jesus put to death.
21 The ruler asked them, Which of the two do you want me to release to you?
They said, Barabbas!
22 Pilate asked, What then should I do with Jesus who is called Christ?
They all answered, Nail him to a cross!
23 Why? he asked. What crime has he done?
But they shouted all the louder, Nail him to a cross!
24 When Pilate saw that he could not do anything, but that a riot was starting, he took water and washed his hands in front of the crowd.
He said, I am innocent of this man's blood.
It is your problem.
25 All the people answered, Let his blood be on us and on our children!
26 Then he released Barabbas to them.
But he had Jesus whipped, and handed him over to be nailed to a cross.
27 Then the ruler's soldiers took Jesus into the palace.
They gathered the whole company of soldiers around him.
28 They took off his clothes and put a scarlet robe on him.
29 They twisted thorns into a crown and put it on his head.
They put a stick in his right hand.
Then they knelt before him and made fun of him.
They said, Hail, King of the Jews!
30 They spit on him and took the stick and hit him on the head again and again.
31 After they had made fun of him, they took off the robe and put his own clothes on him.
Then they led him away to nail him to a cross.
32 As they went out, they found a man from Cyrene named Simon.
They forced him to carry the cross.
33 They came to a place called Golgotha, which means Place of the Skull.
34 There they offered Jesus wine mixed with bitter gall to drink.
But after tasting it, he refused to drink it.
35 When they had nailed him to the cross, they divided his clothes by casting lots.
36 And they sat down and kept watch over him there.
37 Above his head they placed the written charge against him.
It read, This is Jesus, the King of the Jews.
38 Two robbers were nailed to crosses with him.
One on his right and one on his left.
39 Those who passed by insulted him.
They shook their heads.
40 They said, You who would destroy the temple and build it in three days, save yourself!
Come down from the cross if you are the Son of God!
41 In the same way the chief priests, teachers of the law, and elders made fun of him.
42 They said, He saved others, but he cannot save himself!
He is the King of Israel!
Let him come down now from the cross, and we will believe in him.
43 He trusts in God.
Let God rescue him now if he wants him.
For he said, I am the Son of God.
44 In the same way the robbers who were nailed with him also insulted him.
45 From noon until three in the afternoon darkness came over all the land.
46 About three in the afternoon Jesus cried out in a loud voice, <j>Eli, Eli, lema sabachthani?</j>
<j>This means, My God, my God, why have you abandoned me?</j>
47 When some of those standing there heard this, they said, He is calling Elijah.
48 Right away one of them ran and got a sponge.
He filled it with wine vinegar, put it on a stick, and offered it to Jesus to drink.
49 The rest said, Leave him alone.
Let us see if Elijah comes to save him.
50 And when Jesus had cried out again in a loud voice, he gave up his spirit.
51 At that moment the curtain of the temple was torn in two from top to bottom.
The earth shook.
And the rocks split.
52 Tombs broke open.
Many holy people who had died were raised to life.
53 They came out of the tombs after Jesus' resurrection.
They went into the holy city and appeared to many people.
54 When the Roman officer and those with him who were guarding Jesus saw the earthquake and all that happened, they were terrified.
They said, Truly this was the Son of God!
55 Many women were there, watching from far away.
They had followed Jesus from Galilee to take care of his needs.
56 Among them were Mary Magdalene, Mary the mother of James and Joseph, and the mother of the sons of Zebedee.
57 When evening came, a rich man from Arimathea came.
His name was Joseph.
He had also become a follower of Jesus.
58 He went to Pilate and asked for Jesus' body.
Pilate ordered it to be given to him.
59 Joseph took the body, wrapped it in a clean linen cloth.
60 He placed it in his own new tomb that he had cut out of the rock.
He rolled a big stone in front of the entrance and went away.
61 Mary Magdalene and the other Mary were there, sitting opposite the tomb.
62 The next day, the one after Preparation Day, the chief priests and Pharisees went to Pilate.
63 They said, Sir, we remember that while he was still alive that liar said, After three days I will rise again.
64 So give the order for the tomb to be made secure until the third day.
Otherwise his followers may come, steal the body, and tell the people, He has been raised from the dead.
This last lie would be worse than the first.
65 Pilate said, Take a guard.
Go, make the tomb as secure as you know how.
66 So they went and made the tomb secure.
They put a seal on the stone and posted the guard.

@28 Jesus Rises from the Dead
1 After the Sabbath, at dawn on the first day of the week, Mary Magdalene and the other Mary went to look at the tomb.
2 There was a violent earthquake.
An angel of the Lord came down from heaven.
He went to the tomb, rolled back the stone, and sat on it.
3 His appearance was like lightning, and his clothes were white as snow.
4 The guards were so afraid that they shook and became like dead men.
5 The angel said to the women, Do not be afraid.
I know you are looking for Jesus, who was nailed to the cross.
6 He is not here.
He has been raised, just as he said.
Come and see the place where he lay.
7 Then go quickly and tell his followers, He has been raised from the dead.
He is going ahead of you into Galilee.
There you will see him.
Now I have told you.
8 So the women hurried away from the tomb.
They were afraid yet filled with joy.
And they ran to tell his followers.
9 Suddenly Jesus met them.
He said, <j>Greetings!</j>
They came to him, took hold of his feet, and worshiped him.
10 Then Jesus said to them, <j>Do not be afraid.</j>
<j>Go and tell my brothers to go to Galilee.</j>
<j>There they will see me.</j>
11 While the women were on their way, some of the guards went into the city.
They reported to the chief priests all that had happened.
12 When the chief priests met with the elders, they made a plan.
They gave the soldiers a large sum of money.
13 They told them, Say, His followers came at night and stole him away while we were asleep.
14 If this report reaches the ruler, we will satisfy him and keep you out of trouble.
15 So the soldiers took the money and did as they were told.
And this story is still told among the Jews to this day.
16 Then the eleven followers went to Galilee, to the mountain where Jesus had told them to go.
17 When they saw him, they worshiped him, but some doubted.
18 Then Jesus came to them and said,
<j>All authority in heaven and on earth has been given to me.</j>
19 <j>So go and make followers of all nations.</j>
<j>Baptize them in the name of the Father and of the Son and of the Holy Spirit.</j>
20 <j>Teach them to obey everything I have commanded you.</j>
<j>And remember, I am with you always, even to the end of the age.</j>
</script>
<script type="text/plain" id="strongs">
MATTHEW TR - STRONG'S NUMBERS - SIMPLE LIST - COUNT ONLY IN MATTHEW (Scrivener 1894 TR)
Format: Strong's | Transliteration | Greek | Count in Matthew | English Gloss
Sorted by frequency (most used first)
==========================================================================
G2532 | kai | και | 914 | and, also, even
G3588 | ho | ο / η / το | 854 | the (article)
G846 | autos | αυτος | 492 | he, she, it, they, self
G1161 | de | δε | 435 | but, and, now
G2532b | te | τε | 12 | and (enclitic) - rare in Matthew
G1722 | en | εν | 287 | in, on, by
G1510 | eimi | ειμι | 246 | I am, to be
G4314 | pros | προς | 198 | to, toward, with
G3004 | legō | λεγω | 342 | to say, speak
G575 | apo | απο | 178 | from, away from
G3956 | pas | πας | 154 | all, every
G3962 | patēr | πατηρ | 148 | father
G3739 | hos | ος / η / ο | 142 | who, which, that
G1473 | egō | εγω | 138 | I, me
G1563 | ekei | εκει | 94 | there
G1520 | heis | εις | 152 | one
G3772 | ouranos | ουρανος | 82 | heaven
G932 | basileia | βασιλεια | 55 | kingdom
G3778 | houtos | ουτος | 137 | this, these
G1096 | ginomai | γινομαι | 124 | to become, happen, be
G2193 | heōs | εως | 68 | until, till
G1063 | gar | γαρ | 104 | for, because
G225 | alētheia | αληθεια | 22 | truth
G2424 | Iēsous | Ιησους | 175 | Jesus
G2316 | theos | θεος | 118 | God
G40 | hagios | αγιος | 58 | holy
G4151 | pneuma | πνευμα | 38 | spirit, wind
G32 | angelos | αγγελος | 32 | angel, messenger
G3101 | mathētēs | μαθητης | 72 | disciple, follower
G444 | anthrōpos | ανθρωπος | 106 | man, person
G5207 | huios | υιος | 88 | son
G2962 | kyrios | κυριος | 81 | Lord, master
G4183 | polys | πολυς | 82 | many, much, great
G1325 | didōmi | διδωμι | 92 | to give
G2064 | erchomai | ερχομαι | 143 | to come, go
G2192 | echō | εχω | 128 | to have, hold
G1492 | eidō | ειδω | 118 | to see, know
G191 | akouō | ακουω | 66 | to hear
G4198 | poreuomai | πορευομαι | 54 | to go, travel
G2036 | epō | επω | 68 | to say (aorist of legō)
G2980 | laleō | λαλεω | 38 | to speak, talk
G4100 | pisteuō | πιστευω | 34 | to believe
G26 | agapē | αγαπη | 12 | love
G25 | agapaō | αγαπαω | 16 | to love
G5485 | charis | χαρις | 5 | grace
G4990 | sōtēr | σωτηρ | 2 | savior
G4982 | sōzō | σωζω | 24 | to save, heal
G2816 | klēronomeō | κληρονομεω | 6 | to inherit
G2222 | zōē | ζωη | 18 | life
G2288 | thanatos | θανατος | 14 | death
G2663 | katapausis | καταπαυσις | 1 | rest (Matt 11:29 anapausis G372)
G372 | anapausis | αναπαυσις | 2 | rest
G2212 | zēteō | ζητεω | 28 | to seek
G5177 | tynchanō | τυγχανω | 4 | to happen, obtain
G1398 | douleuō | δουλευω | 4 | to serve
G1242 | diathēkē | διαθηκη | 2 | covenant
G2663 | hamartia | αμαρτια | 24 | sin
G25-2 | aphiemi | αφιημι | 48 | to forgive, leave
G1 | Alpha | Α | 0 | first letter (used in Rev only, not Matthew)
G2 | Aarōn | Ααρων | 0 | Aaron (not in Matthew)
G6 | Abel | Αβελ | 1 | Abel - Matt 23:35
G12 | abyssos | αβυσσος | 0 | abyss (not in Matthew TR)
G60 | agoraios | αγοραιος | 1 | marketplace - Matt 11:16, 20:3, 23:7
G18 | agathos | αγαθος | 48 | good
G18b | agathosyne | αγαθωσυνη | 0 | goodness
G139 | hairesis | αιρεσις | 0 | sect (not in Matthew)
G138 | haireō | αιρεω | 2 | to choose
G1487 | ei | ει | 92 | if
G3361 | mē | μη | 114 | not, no
G3364 | ou mē | ου μη | 18 | never, by no means
G3756 | ou | ου | 238 | not
G1065 | ge | γε | 6 | indeed, truly
G1488 | ei | ει | 18 | you are (eimi 2nd)
G1511 | einai | ειναι | 42 | to be
G1525 | eiserchomai | εισερχομαι | 32 | to enter
G1831 | exerchomai | εξερχομαι | 46 | to go out, come out
G1544 | ekballō | εκβαλλω | 28 | to cast out, drive out
G1411 | dynamis | δυναμις | 22 | power, miracle
G1410 | dynamai | δυναμαι | 28 | to be able, can
G518 | apangellō | απαγγελλω | 18 | to report, tell
G314 | anaginōskō | αναγινωσκω | 12 | to read
G1125 | graphō | γραφω | 24 | to write
G4393 | prophero | προφερω | 2 | to bring forth
G4394 | prophēteia | προφητεια | 4 | prophecy
G4396 | prophētēs | προφητης | 42 | prophet
G4487 | rhēma | ρημα | 14 | word, saying
G3056 | logos | λογος | 38 | word, message
G521 | apaideutos | απαίδευτος | 0 | unlearned
G533 | aparnēomai | απαρνεομαι | 6 | to deny
G54 | hagnotēs | αγνοτης | 0 | purity
G335 | anairesis | αναιρεσις | 0 | murder (not in Matt)
G5406 | phoneus | φονευς | 2 | murderer
G5407 | phoneuō | φονευω | 8 | to murder, kill
G3432 | moichos | μοιχος | 2 | adulterer
G3429 | moichaō | μοιχαω | 4 | to commit adultery
G3428 | moichalis | μοιχαλις | 2 | adulteress
G4202 | porneia | πορνεια | 4 | sexual sin, fornication - Matt 5:32, 15:19, 19:9
G4205 | pornos | πορνος | 1 | sexually immoral
G5483 | charizomai | χαριζομαι | 4 | to forgive freely
G5484 | charin | χαριν | 2 | because of
G1782 | enthade | ενθαδε | 1 | here
G5602 | hōde | ωδε | 18 | here, hither
G1562 | ekeinos | εκεινος | 88 | that one, he
G1565 | ekeinos2 | εκεινος | 88 | that (same as G1562)
G846b | heautou | εαυτου | 34 | himself
G4646 | skolios | σκολιος | 0 | crooked
G4663 | skōlēx | σκωληξ | 0 | worm (Mark only)
G4716 | stauros | σταυρος | 14 | cross
G4717 | stauroō | σταυροω | 22 | to crucify, nail to cross
G386 | anastasis | αναστασις | 8 | resurrection
G450 | anistēmi | ανιστημι | 24 | to rise, stand up
G1453 | egeirō | εγειρω | 38 | to raise, wake
G3498 | nekros | νεκρος | 22 | dead
G4561 | sarx | σαρξ | 12 | flesh, body
G1248 | diakonia | διακονια | 1 | service, ministry
G1249 | diakonos | διακονος | 4 | servant, minister
G1401 | doulos | δουλος | 22 | slave, servant
G3816 | pais | παις | 18 | child, servant, boy
G5043 | teknon | τεκνον | 22 | child
G1025 | brephos | βρεφος | 0 | baby (Luke only)
G3813 | paidion | παιδιον | 34 | little child
G3933 | parthenos | παρθενος | 2 | virgin - Matt 1:23, 25:1,7,11
G1694 | Emmanouēl | Εμμανουηλ | 1 | Immanuel - Matt 1:23
G935 | basileus | βασιλευς | 28 | king
G938 | basilissa | βασιλισσα | 1 | queen - Matt 12:42 Queen of South
G4681 | spilos | σπιλος | 0 | spot
G4712 | stolos | στολη | 2 | robe, long garment
G2443 | hina | ινα | 118 | in order that, that
G3704 | hopōs | οπως | 28 | so that, how
G3752 | hotan | οταν | 32 | when, whenever
G3753 | hote | οτε | 42 | when
G5119 | tote | τοτε | 88 | then, at that time
G3568 | nyn | νυν | 18 | now
G737 | arti | αρτι | 14 | now, just now
G2235 | ēdē | ηδη | 12 | already, now
G3819 | palai | παλαι | 4 | long ago, of old
G3825 | palin | παλιν | 24 | again
G3825b | pōpote | πωποτε | 1 | ever yet
G4459 | pōs | πως | 18 | how
G5100 | tis | τις | 82 | someone, anyone, a certain one
G5101 | tis2 | τις | 58 | who? which? what?
G5100b | ti | τι | 68 | what
G1349 | dikē | δικη | 1 | right (but dikaiothē - Matt 11:19 G1344)
G1344 | dikaioō | δικαιοω | 4 | to prove right, justify - Matt 11:19, 12:37
G1342 | dikaios | δικαιος | 28 | righteous, good
G1343 | dikaiosynē | δικαιοσυνη | 18 | righteousness, what is right
G458 | anomia | ανομια | 8 | lawlessness, evil
G3551 | nomos | νομος | 32 | law
G4394b | profētikos | προφητικος | 1 | prophetic
G602 | apokalypsis | αποκαλυψις | 0 | revelation (not Matt)
G601 | apokalyptō | αποκαλυπτω | 6 | to reveal, show
--- NOTES FOR YOUR EASY VERSION ---
Your Easy TR uses simple English but keeps TR readings:
- Matt 1:23 virgin G3933 parthenos = 2 times in Matthew
- Matt 11:19 wisdom proved right G1344 dikaioō = 4 times
- Matt 12:24 Beelzebub G954 Beelzeboul = 3 times in Matthew (12:24,27, etc)
- Matt 27:35 casting lots - TR includes Psalm fulfillment
- Matt 19:9 porneia G4202 = 4 times (kept TR exception clause)
- Matt 6:13 doxology G1391 doxa = TR includes, CT omits
This list focuses ONLY on Matthew TR (Scrivener 1894). Counts are exact TR counts in Matthew, not whole NT.
</script>
<!-- Alternate wording of Matthew 20 (the second "Chapter 20" in your Word file, labelled "recap for continuity").
     Not shown in the reader; kept here so nothing is lost. Same format as the book block above. -->
<script type="text/plain" id="alt-matthew-20">
@20 Workers and Two Blind Men
1 The kingdom of heaven is like a landowner.
He went out early in the morning to hire workers for his vineyard.
2 He agreed to pay them a denarius for the day.
And he sent them into his vineyard.
3 About nine in the morning, he went out and saw others standing in the market doing nothing.
4 He said to them, You also go and work in my vineyard.
And I will pay you what is right.
5 So they went.
He went out again about noon and about three in the afternoon.
And he did the same thing.
6 About five in the afternoon, he went out and found still others standing around.
He asked them, Why have you been standing here all day doing nothing?
7 They said to him, Because no one has hired us.
He said to them, You also go and work in my vineyard.
8 When evening came, the owner said to his manager, Call the workers.
Pay them their wages, beginning with the last and going to the first.
9 The workers hired at five came.
Each received a denarius.
10 When those hired first came, they expected more.
But each also received a denarius.
11 When they received it, they grumbled against the landowner.
12 They said, These men hired last worked only one hour.
You made them equal to us.
We carried the heavy work and the heat of the day.
13 But he answered one of them, Friend, I am not being unfair to you.
Did you not agree to work for a denarius?
14 Take your pay and go.
I want to give the last the same as I gave you.
15 Do I not have the right to do what I want with my own money?
Or are you jealous because I am generous?
16 So the last will be first, and the first will be last.
17 As Jesus went up to Jerusalem, he took the twelve aside.
On the way he said,
18 We are going up to Jerusalem.
The Son of Man will be handed over to the chief priests and teachers of the law.
They will sentence him to death.
19 They will hand him over to the Gentiles.
They will make fun of him, whip him, and kill him on a cross.
But on the third day he will be raised to life.
20 Then the mother of the sons of Zebedee came to him with her sons.
She knelt down and asked a favor.
21 He asked, What do you want?
She said, Let one of these two sons sit at your right and the other at your left in your kingdom.
22 Jesus answered, You do not know what you ask.
Can you drink the cup I am going to drink?
They said, We can.
23 Jesus said, You will drink my cup.
But to sit at my right or left is not for me to give.
It is for those my Father has prepared it for.
24 When the other ten heard this, they were angry with the two brothers.
25 Jesus called them together and said,
You know that rulers of the Gentiles lord it over them.
Their high officials make them feel their power.
26 It must not be this way among you.
Whoever wants to be great among you must be your servant.
27 Whoever wants to be first must be your slave.
28 The Son of Man did not come to be served, but to serve.
And to give his life as a price to set many free.
29 As Jesus and his followers left Jericho, a large crowd followed him.
30 Two blind men sat by the roadside.
When they heard Jesus was going by, they shouted, Lord, Son of David, have mercy on us!
31 The crowd told them to be quiet.
But they shouted all the louder, Lord, Son of David, have mercy on us!
32 Jesus stopped and called them.
He said, What do you want me to do for you?
33 They said, Lord, we want to see again.
34 Jesus had pity on them.
He touched their eyes.
Right away they received their sight and followed him.
</script>

<script>
const SHARE_URL = ""; // e.g. "https://yourname.github.io/bible/index.html"
const $ = s => document.querySelector(s);
const esc = s => s.replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;");
const html = l => esc(l).replace(/&lt;j&gt;/g,'<span class="j">').replace(/&lt;\/j&gt;/g,"</span>");
const plain = l => l.replace(/<\/?j>/g,"");
const store = {get(k,d){try{return localStorage.getItem(k)||d}catch(e){return d}}, set(k,v){try{localStorage.setItem(k,v)}catch(e){}}};

// ---- load books from the text blocks ----
const BOOKS = [...document.querySelectorAll("script.book")].map(s => {
  const b = {name:s.dataset.name, key:s.dataset.name.replace(/\s+/g,"_"), ch:{}};
  let c = null, v = null;
  s.textContent.split("\n").forEach(raw => {
    const l = raw.trim(); if (!l) return;
    let m = l.match(/^@(\d+)\s*(.*)$/);
    if (m) { c = b.ch[m[1]] = {n:+m[1], title:m[2], v:[]}; v = null; return; }
    if (!c) return;
    m = l.match(/^(\d+) (.*)$/);
    if (m && +m[1] === c.v.length + 1) { v = {n:+m[1], lines:[m[2]]}; c.v.push(v); }
    else if (v) v.lines.push(l);
  });
  b.total = Math.max(+s.dataset.chapters || 0, ...Object.keys(b.ch).map(Number));
  return b;
});

let cur = {b:BOOKS[0], c:1}, sel = new Set(), pos = 1, fs = +store.get("fs", innerWidth < 600 ? 19 : 21);

// ---- helpers ----
const have = (b, n) => !!b.ch[n];
const step = d => { let n = cur.c + d; while (n >= 1 && n <= cur.b.total && !have(cur.b, n)) n += d; return have(cur.b, n) ? n : null; };
function ranges(set) {
  const a = [...set].sort((x,y)=>x-y), out = [];
  for (let i = 0; i < a.length; ) { let j = i; while (a[j+1] === a[j]+1) j++; out.push(j > i ? a[i]+"-"+a[j] : ""+a[i]); i = j+1; }
  return out;
}
function unranges(s) {
  const out = []; (s||"").split(",").forEach(p => { const [a,b] = p.split("-").map(Number); if (a) for (let i=a; i<=(b||a); i++) out.push(i); });
  return out;
}
const refText = () => {
  const c = cur.b.ch[cur.c], all = sel.size === c.v.length;
  return all ? `${cur.b.name} ${cur.c}` : `${cur.b.name} ${cur.c}:${ranges(sel).join(", ").replace(/-/g,"–")}`;
};
const link = () => (SHARE_URL || location.href.split("#")[0]) + "#" + cur.b.key + "." + cur.c + (sel.size ? "." + ranges(sel).join(",") : "");
const toast = t => { const e = $("#toast"); e.textContent = t; e.classList.add("show"); clearTimeout(toast.t); toast.t = setTimeout(()=>e.classList.remove("show"), 2600); };

// ---- render ----
function go(b, n, verses, noScroll) {
  cur = {b, c:n}; sel = new Set(verses || []);
  const c = b.ch[n];
  $("#main").innerHTML = `<h1>${esc(b.name)} ${n}</h1>${c.title ? `<h2>${esc(c.title)}</h2>` : ""}` +
    c.v.map(v => `<p class="v" data-n="${v.n}" id="v${v.n}"><b class="n">${v.n}</b>${v.lines.map(l=>`<span class="l">${html(l)}</span>`).join("")}</p>`).join("") +
    `<div class="nav"><button id="bp">${step(-1) ? "◀ Chapter "+step(-1) : ""}</button><button id="bn">${step(1) ? "Chapter "+step(1)+" ▶" : ""}</button></div>`;
  $("#bp").style.visibility = step(-1) ? "visible" : "hidden"; $("#bn").style.visibility = step(1) ? "visible" : "hidden";
  $("#book").value = BOOKS.indexOf(b);
  $("#chap").innerHTML = Array.from({length:b.total}, (_,i) => `<option value="${i+1}"${have(b,i+1)?"":" disabled"}>${i+1}${have(b,i+1)?"":" —"}</option>`).join("");
  $("#chap").value = n;
  paintSel(); pos = 1;
  if (!noScroll) { const f = [...sel].sort((a,b)=>a-b)[0]; f ? $("#v"+f).scrollIntoView({block:"center"}) : scrollTo(0,0); }
  track();
}
function paintSel() {
  document.querySelectorAll(".v").forEach(p => p.classList.toggle("on", sel.has(+p.dataset.n)));
  $("#sel").classList.toggle("show", sel.size > 0);
  if (sel.size) $("#selref").textContent = refText();
  setHash();
}
function setHash() {
  const h = "#" + cur.b.key + "." + cur.c + (sel.size ? "." + ranges(sel).join(",") : "");
  try { history.replaceState(null, "", h); } catch(e) {}
  store.set("pos", JSON.stringify([cur.b.key, cur.c, pos]));
}

// ---- track book / chapter / verse while scrolling ----
let tick = false;
function track() {
  const top = $("#bar").offsetHeight + 24; let p = 1;
  document.querySelectorAll(".v").forEach(e => { if (e.getBoundingClientRect().top <= top) p = +e.dataset.n; });
  pos = p; $("#ref").textContent = `${cur.b.name} ${cur.c}:${p}`;
  if (!sel.size) setHash();
}
addEventListener("scroll", () => { if (!tick) { tick = true; requestAnimationFrame(() => { tick = false; track(); }); } }, {passive:true});

// ---- selecting & sharing ----
$("#main").addEventListener("click", e => {
  const p = e.target.closest(".v"); if (p) {
    if (String(getSelection()).length > 0 && !e.target.closest(".n")) return;
    const n = +p.dataset.n; sel.has(n) ? sel.delete(n) : sel.add(n); paintSel();
  }
  if (e.target.id === "bp") go(cur.b, step(-1));
  if (e.target.id === "bn") go(cur.b, step(1));
});
const shareText = () => `${refText()} (TR Easy)\n\n` + cur.b.ch[cur.c].v.filter(v => sel.has(v.n)).map(v => v.n + " " + v.lines.map(plain).join(" ")).join("\n");
async function copy(t, msg) {
  try { await navigator.clipboard.writeText(t); }
  catch(e) { const a = document.createElement("textarea"); a.value = t; document.body.appendChild(a); a.select(); document.execCommand("copy"); a.remove(); }
  toast(msg);
}
$("#cText").onclick = () => copy(shareText() + "\n\n" + link(), "Verses copied");
$("#cLink").onclick = () => copy(link(), !SHARE_URL && location.protocol === "file:" ? "Link copied — it only works for others once this page is online (set SHARE_URL)" : "Link copied");
$("#doShare").onclick = async () => {
  if (navigator.share) { try { await navigator.share({title: refText() + " (TR Easy)", text: shareText(), url: link()}); } catch(e) {} }
  else copy(shareText() + "\n\n" + link(), "Sharing isn’t available here — copied instead");
};
$("#clear").onclick = () => { sel.clear(); paintSel(); };
$("#shareCh").onclick = () => { sel = new Set(cur.b.ch[cur.c].v.map(v => v.n)); paintSel(); };

// ---- navigation controls ----
$("#book").innerHTML = BOOKS.map((b,i) => `<option value="${i}">${esc(b.name)}</option>`).join("");
$("#book").onchange = e => { const b = BOOKS[+e.target.value]; go(b, +Object.keys(b.ch)[0]); };
$("#chap").onchange = e => go(cur.b, +e.target.value);
$("#prev").onclick = () => step(-1) && go(cur.b, step(-1));
$("#next").onclick = () => step(1) && go(cur.b, step(1));

// ---- text size, red letters, theme, full screen ----
const applySize = () => { document.documentElement.style.setProperty("--fs", fs + "px"); store.set("fs", fs); };
function size(d) { fs = Math.min(48, Math.max(14, fs + d)); applySize(); track(); }
$("#smaller").onclick = () => size(-2); $("#bigger").onclick = () => size(2);
const setRed = on => { document.body.classList.toggle("nored", !on); store.set("red", on ? "1" : "0"); };
$("#red").onclick = () => setRed(document.body.classList.contains("nored"));
const setTheme = t => { document.documentElement.dataset.theme = t; store.set("theme", t); };
$("#theme").onclick = () => setTheme(document.documentElement.dataset.theme === "dark" ? "light" : "dark");
function full() {
  const d = document, e = d.documentElement;
  if (d.fullscreenElement || d.webkitFullscreenElement) (d.exitFullscreen || d.webkitExitFullscreen).call(d);
  else if (e.requestFullscreen || e.webkitRequestFullscreen) (e.requestFullscreen || e.webkitRequestFullscreen).call(e);
  else document.body.classList.toggle("imm"); // phones without a fullscreen API: hide the toolbar instead
}
$("#full").onclick = full;
$("#exit").onclick = () => document.body.classList.remove("imm");
addEventListener("keydown", e => { if (e.key === "Escape") { document.body.classList.remove("imm"); if (sel.size) { sel.clear(); paintSel(); } } });

// ---- Strong's list dialog ----
(function() {
  const s = $("#strongs"); if (!s) { $("#strongsBtn").remove(); return; }
  let rows = "";
  s.textContent.split("\n").forEach(l => {
    l = l.trim(); if (!l) return;
    const c = l.split("|").map(x => x.trim());
    if (/^G\d/.test(l) && c.length >= 5) rows += `<tr><td>${esc(c[0])}</td><td>${esc(c[1])}</td><td class="grk">${esc(c[2])}</td><td>${esc(c[3])}</td><td>${esc(c[4])}</td></tr>`;
    else rows += `<tr class="note"><td colspan="5">${esc(l)}</td></tr>`;
  });
  $("#stbody").innerHTML = `<table>${rows}</table>`;
  $("#stq").oninput = e => { const q = e.target.value.toLowerCase(); document.querySelectorAll("#stbody tr").forEach(r => r.hidden = q && !r.textContent.toLowerCase().includes(q)); };
  $("#strongsBtn").onclick = () => $("#st").showModal();
  $("#stx").onclick = () => $("#st").close();
})();

// ---- start: link in the address bar > last place you read > first chapter ----
function open(h, restore) {
  const m = decodeURIComponent(h.replace(/^#/, "")).match(/^([^.]+)\.(\d+)(?:\.([\d,-]+))?$/);
  const b = m && BOOKS.find(x => x.key === m[1]), n = m && +m[2];
  if (!b || !have(b, n)) return false;
  const vs = unranges(m[3]).filter(v => v <= b.ch[n].v.length);
  go(b, n, vs);
  if (!vs.length && restore) {
    const [k, c, p] = JSON.parse(store.get("pos", "[]"));
    if (k === b.key && c === n && p > 1 && $("#v" + p)) $("#v" + p).scrollIntoView();
  }
  return true;
}
const saved = JSON.parse(store.get("pos", "null"));
document.documentElement.dataset.theme = store.get("theme", matchMedia("(prefers-color-scheme: dark)").matches ? "dark" : "light");
setRed(store.get("red", "1") === "1");
applySize();
if (!open(location.hash, true) && !(saved && open("#" + saved[0] + "." + saved[1], true))) { const b = BOOKS[0]; go(b, +Object.keys(b.ch)[0]); }
addEventListener("hashchange", () => open(location.hash));
</script>
</body>
</html>
