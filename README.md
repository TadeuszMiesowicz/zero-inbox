# Zero-inbox
Przykładowy agent AI n8n stworzony na potrzeby prezentacji na konferencji LegalTech Forum 2025.

## Jak zacząć
1. Zainstaluj n8n lokalnie ([How to Install & Update n8n Locally - YouTube](https://www.youtube.com/watch?v=YHsN8jb8A8M)) lub skorzystaj z konta w chmurze.
2. Uruchom n8n.
3. Utwórz nowy workflow.
4. Otwórz plik `workflow.json` ([workflow.json at main · TadeuszMiesowicz/zero-inbox · GitHub](https://github.com/TadeuszMiesowicz/zero-inbox/blob/main/workflow.json)), skopiuj całą zawartość (Ctrl+A, a następnie Ctrl+C), utwórz nowy workflow w n8n i wklej skopiowaną treść (Ctrl+V). Węzły powinny pojawić się automatycznie.
5. Dodaj uprawnienia do Gmaila w n8n ([How to CONNECT Gmail to n8n (Step by Step) 2025 - YouTube](https://www.youtube.com/watch?v=SBPU5a8-8Xo)).
6. Dodaj uprawnienia dla wybranego modelu (Gemini, Anthropic, OpenAI itp.) – potrzebujesz klucza API.
7. Utwórz etykietę `ai-labeled` w swojej skrzynce Gmail.
8. Uruchom workflow.

## Uwaga ⚠️
1. Węzeł `get-inbox-content` jest domyślnie skonfigurowany tak, aby analizować tylko **10 wiadomości**. Jest to ustawienie celowe, ponieważ workflow ma charakter edukacyjny i testowy. Jeśli planujesz wykorzystać go w praktyce, po przetestowaniu zmień to ustawienie.
2. Węzeł `delay` służy do określenia, sprzed ilu dni analizowane są wiadomości (domyślnie wiadomości otrzymane **przedwczoraj** lub wcześniej).
3. W węźle `agent AI` `system-message` dostosuj do swoich potrzeb – możesz modyfikować warunki i eksperymentować z różnymi narzędziami.
