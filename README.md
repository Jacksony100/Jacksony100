from typing import Tuple, List, Dict

class Jacksony:
    pass

class Attributes(Jacksony):
    @property
    def contact(self) -> Tuple[str, str]:
        telegram = "t.me/Jacksony100"
        channel  = "t.me/Smesharik_lair"
        
        return telegram, channel

    @property
    def life(self) -> Tuple[List[str], int]:
        langs = ['Russian', 'English']
        age   = 19
        
        return langs, age
    
    @property
    def coding(self) -> Tuple[Dict[str, List[str]], List[str], List[str], Dict[str, Dict[str, Dict[str, str]]]]:
        langs = {
            'expert'      : ['c++', 'c#'],
            'intermediate': ['python'],
            'learning'    : ['go', 'asm', 'javascript']
        }
        specialities  = ['cybersecurity', 'web development', 'ai']
        ide           = ['vscode', 'visual studio', 'pycharm']
        pc            = {
            'Windows': {
                'custom': {
                    'processor': 'Intel Core i7-12700K | 12 cores',
                    'ram'      : '32gb',
                    'gpu'      : 'nvidia RTX 4070 | CUDA cores'
                }
            }
        }

        return langs, specialities, ide, pc
    
    def __str__(self) -> str:
        ascii_banner = r"""
 ________      ________      ________      ___  ___      _________        _____ ______       _______      
|\   __  \    |\   __  \    |\   __  \    |\  \|\  \    |\___   ___\     |\   _ \  _   \    |\  ___ \     
\ \  \|\  \   \ \  \|\ /_   \ \  \|\  \   \ \  \\\  \   \|___ \  \_|     \ \  \\\__\ \  \   \ \   __/|    
 \ \   __  \   \ \   __  \   \ \  \\\  \   \ \  \\\  \       \ \  \       \ \  \\|__| \  \   \ \  \_|/__  
  \ \  \ \  \   \ \  \|\  \   \ \  \\\  \   \ \  \\\  \       \ \  \       \ \  \    \ \  \   \ \  \_|\ \ 
   \ \__\ \__\   \ \_______\   \ \_______\   \ \_______\       \ \__\       \ \__\    \ \__\   \ \_______\
    \|__|\|__|    \|_______|    \|_______|    \|_______|        \|__|        \|__|     \|__|    \|_______|                                                                                             
"""
        
        contact_info = (
            f"Contact:\n"
            f"[+] Telegram: {self.contact[0]}\n"
            f"[+] Channel : {self.contact[1]}"
        )
        life_info = (
            f"Life:\n"
            f"[+] Languages: {', '.join(self.life[0])}\n"
            f"[+] Age      : {self.life[1]}"
        )
        
        coding_langs = "\n".join([f"  [+] {level.title()}: {', '.join(langs)}" for level, langs in self.coding[0].items()])
        specialities = ", ".join(self.coding[1])
        ides = ", ".join(self.coding[2])
        pc_info = "\n".join([f"  [+] {os}: {details}" for os, details in self.coding[3].items()])
        
        coding_info = (
            f"Coding:\n"
            f"[+] Languages:\n{coding_langs}\n"
            f"[+] Specialities: {specialities}\n"
            f"[+] IDEs       : {ides}\n"
            f"[+] PC Specs   :\n{pc_info}"
        )
        return f"{ascii_banner}\n{contact_info}\n\n{life_info}\n\n{coding_info}"

attributes = Attributes()
print(attributes)
