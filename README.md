

Для того чтобы видеть, что ты пишешь в section(отвечая на вопросы) используйте(ниже), а после написания вопроса удалите эту часть , чтобы не ломать основной документ
\documentclass[a4paper,12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[russian]{babel}
\usepackage{physics}
\usepackage{tikz}
\usepackage{wrapfig} % Для обтекания текста
\usepackage{amsmath, amssymb}
\usepackage{graphicx} % Для работы с изображениями
\usepackage{geometry}
\geometry{top=2cm, bottom=2cm, left=2.5cm, right=2.5cm}

% Увеличиваем размер основного текста
\renewcommand{\normalsize}{\fontsize{14}{17}\selectfont}

% Команда для курсива
\newcommand{\kr}[1]{\textit{#1}}

% Команда для вставки математического выражения
\newcommand{\fc}[1]{\[#1\]}

% Команда для вставки математического
\newcommand{\mm}[1]{\mathrm{#1}}

%Настраиваемый вид замкнутого тройного интеграла(при умножении, в дроби)
\newcommand{\oiiint}{%
  \mathchoice%
    {\mathop{\raisebox{0.2ex}{\scalebox{1.5}[1]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\!\!\!\!\!\!\!\int\!\!\!\int\!\!\!\int}% Displaystyle
    {\mathop{\raisebox{0.2ex}{\scalebox{1.2}[1]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\!\!\!\!\!\int\!\!\!\int\!\!\!\int}% Textstyle
    {\mathop{\raisebox{0.1ex}{\scalebox{1}[1]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\!\!\!\int\!\!\!\int\!\!\!\int}% Scriptstyle
    {\mathop{\raisebox{0.05ex}{\scalebox{0.8}[1]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\!\!\int\!\!\!\int\!\!\!\int}% Scriptscriptstyle
}

%Настраиваемый вид замкнутого двойного интеграла(при умножении, в дроби)
\newcommand{\oiint}{%
  \mathchoice%
    {\mathop{\raisebox{0.1ex}{\scalebox{1.7}[0.7]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\!\!\!\!\int\!\!\!\int}% Displaystyle
    {\mathop{\raisebox{0.3ex}{\scalebox{1.}[0.5]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\int\!\!\!\int}% Textstyle
    {\mathop{\raisebox{0.1ex}{\scalebox{1}[0.8]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\!\!\int\!\!\!\int}% Scriptstyle
    {\mathop{\raisebox{0.05ex}{\scalebox{0.8}[0.8]{\(\bigcirc\)}}}%
     \!\!\!\!\!\!\!\!\int\!\!\!\int}% Scriptscriptstyle
}

% уменьшенный и сдвинутый градиент
\newcommand{\gradd}{\hspace{0.2cm}\scriptsize \nabla}   

% Команда для изображения в центре
\newcommand{\imc}[2][0.7\textwidth]{%
    \begin{figure}[h!]
        \centering
        \includegraphics[width=#1]{im/#2}  % Указание папки 'im' для изображений
    \end{figure}%
}
