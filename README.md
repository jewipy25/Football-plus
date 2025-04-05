# Football-plus  import tkinter as tk
from tkinter import messagebox

class FootballApp:
    def __init__(self, root):
        self.root = root
        self.root.title("Football History and Laws App")
        
        # Language options
        self.language = "English"
        
        # Set up the window size
        self.root.geometry("500x400")
        
        # Language Selection Buttons
        self.language_label = tk.Label(root, text="Select Language", font=("Arial", 14))
        self.language_label.pack(pady=10)

        self.english_button = tk.Button(root, text="English", command=self.set_english, font=("Arial", 12))
        self.english_button.pack(pady=5)

        self.french_button = tk.Button(root, text="Français", command=self.set_french, font=("Arial", 12))
        self.french_button.pack(pady=5)

        self.creole_button = tk.Button(root, text="Kreyòl Ayisyen", command=self.set_creole, font=("Arial", 12))
        self.creole_button.pack(pady=5)

        # Menu options
        self.menu_label = tk.Label(root, text="Select a Topic", font=("Arial", 14))
        self.menu_label.pack(pady=20)

        self.history_button = tk.Button(root, text="History of Football", command=self.history, font=("Arial", 12))
        self.history_button.pack(pady=5)

        self.laws_button = tk.Button(root, text="Laws of Football", command=self.laws, font=("Arial", 12))
        self.laws_button.pack(pady=5)

        self.controversy_button = tk.Button(root, text="Controversial Decisions", command=self.controversy, font=("Arial", 12))
        self.controversy_button.pack(pady=5)

    def set_english(self):
        self.language = "English"
        messagebox.showinfo("Language", "Language set to English")

    def set_french(self):
        self.language = "French"
        messagebox.showinfo("Language", "Langue définie sur le français")

    def set_creole(self):
        self.language = "Creole"
        messagebox.showinfo("Language", "Lang langaj la se Kreyòl Ayisyen")

    def history(self):
        if self.language == "English":
            messagebox.showinfo("History of Football", "Football, also known as soccer in some countries, has evolved over centuries, starting with ancient games involving a ball.")
        elif self.language == "French":
            messagebox.showinfo("Histoire du Football", "Le football, également appelé soccer dans certains pays, a évolué au fil des siècles, à partir de jeux anciens impliquant un ballon.")
        elif self.language == "Creole":
            messagebox.showinfo("Istwa Football", "Football, yo rele'l tou 'soccer' nan kèk peyi, li devlope sou plizyè syèk kòmanse ak jwèt ansyen ki te gen yon balon.")

    def laws(self):
        if self.language == "English":
            messagebox.showinfo("Laws of Football", "The Laws of Football include rules such as the offside rule, penalty kicks, and the role of referees in managing the game.")
        elif self.language == "French":
            messagebox.showinfo("Lois du Football", "Les lois du football incluent des règles telles que la règle du hors-jeu, les pénaltys et le rôle des arbitres dans la gestion du jeu.")
        elif self.language == "Creole":
            messagebox.showinfo("Lwa Football", "Lwa Football yo gen règ tankou règ hors-jeu, penalti, ak wòl juj yo nan jere jwèt la.")

    def controversy(self):
        if self.language == "English":
            messagebox.showinfo("Controversial Decisions", "Famous controversial decisions include the 'Hand of God' goal by Maradona and the 2010 World Cup goal that wasn't given to England.")
        elif self.language == "French":
            messagebox.showinfo("Décisions Controversées", "Des décisions controversées célèbres incluent le but 'Hand of God' de Maradona et le but du Mondial 2010 qui n'a pas été accordé à l'Angleterre.")
        elif self.language == "Creole":
            messagebox.showinfo("Desizyon Kontwovèsyal", "Desizyon ki fè anpil diskisyon gen ladan 'Hand of God' pa Maradona ak gòl 2010 Mondyal la ki pa t bay Angletè.")

if __name__ == "__main__":
    root = tk.Tk()
    app = FootballApp(root)
    root.mainloop()
