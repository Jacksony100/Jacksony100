
     ________      ________      ________      ___  ___      _________        _____ ______       _______      
    |\   __  \    |\   __  \    |\   __  \    |\  \|\  \    |\___   ___\     |\   _ \  _   \    |\  ___ \     
    \ \  \|\  \   \ \  \|\ /_   \ \  \|\  \   \ \  \\\  \   \|___ \  \_|     \ \  \\\__\ \  \   \ \   __/|    
     \ \   __  \   \ \   __  \   \ \  \\\  \   \ \  \\\  \       \ \  \       \ \  \\|__| \  \   \ \  \_|/__  
      \ \  \ \  \   \ \  \|\  \   \ \  \\\  \   \ \  \\\  \       \ \  \       \ \  \    \ \  \   \ \  \_|\ \ 
       \ \__\ \__\   \ \_______\   \ \_______\   \ \_______\       \ \__\       \ \__\    \ \__\   \ \_______\
        \|__|\|__|    \|_______|    \|_______|    \|_______|        \|__|        \|__|     \|__|    \|_______|             
    
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
