# Zed-Settings

```json

{
  // IA / Agent: provedores de agente externos e configuração do painel do agente
  "agent_servers": {
    "opencode": {
      "type": "registry",
    },
    "grok-build": {
      "type": "registry",
    },
    "gemini": {
      "type": "registry",
    },
    "github-copilot-cli": {
      "type": "registry",
    },
    "cursor": {
      "type": "registry",
    },
    "codex-acp": {
      "type": "registry",
    },
    "claude-acp": {
      "default_config_options": {
        "mode": "plan",
        "effort": "medium",
        "fast": false,
        "model": "sonnet",
      },
      "type": "registry",
    },
  },
  "agent_ui_font_size": 15,
  "agent_buffer_font_size": 14,
  "agent": {
    "flexible": true,
    "dock": "right",
    "tool_permissions": {
      "default": "allow",
    },
  },

  // Comportamento do editor: salvar, formatar, indentação, autocompletar
  "ensure_final_newline_on_save": true,
  "format_on_save": "on",
  "tab_size": 2,
  "autosave": {
    "after_delay": {
      "milliseconds": 500,
    },
  },
  "close_on_file_delete": true,
  "use_on_type_format": false,
  "show_completions_on_input": true,
  "inlay_hints": {
    "enabled": false,
  },

  // Largura de linha e quebra de texto
  "preferred_line_length": 120,
  "soft_wrap": "bounded",
  "wrap_guides": [120],
  "show_wrap_guides": false,

  // LSP: só configura o vtsls (TS/JS) pra sempre atualizar imports ao mover arquivo
  "lsp": {
    "vtsls": {
      "settings": {
        "typescript": {
          "updateImportsOnFileMove": {
            "enabled": "always",
          },
        },
        "javascript": {
          "updateImportsOnFileMove": {
            "enabled": "always",
          },
        },
      },
    },
  },

  // Status bar: some com os botões que não uso no dia a dia
  "debugger": {
    "button": false,
  },
  "diagnostics": {
    "button": false,
  },
  "global_lsp_settings": {
    "button": false,
  },
  "status_bar": {
    "cursor_position_button": false,
  },

  // Painéis laterais: todos ancorados à esquerda, exceto o agente (acima)
  "outline_panel": {
    "dock": "left",
  },
  "collaboration_panel": {
    "dock": "left",
  },
  "git_panel": {
    "dock": "left",
  },
  "project_panel": {
    "dock": "left",
    // espaçamento vertical máximo entre as entradas (arquivos/pastas), não existe opção maior
    "entry_spacing": "comfortable",
    // indentação menor pros itens filhos (default do Zed é 20)
    "indent_size": 14,
    // com linha de guia da árvore
    "indent_guides": {
      "show": "always",
    },
  },

  // Aparência: tema, ícones e fontes
  "base_keymap": "JetBrains",
  "theme": {
    "mode": "system",
    "light": "Gruvbox Light Soft",
    "dark": "Vesper",
  },
  "icon_theme": "Catppuccin Mocha",
  "ui_font_family": "JetBrains Mono",
  "ui_font_size": 14,
  "buffer_font_family": "JetBrains Mono",
  "buffer_font_size": 14,
  "buffer_font_weight": 550,
  "buffer_line_height": {
    "custom": 2.2,
  },

  // Terminal integrado
  "terminal": {
    "minimum_contrast": 40.0,
    "cursor_shape": "block",
    "font_weight": 390.0,
    "button": false,
    "font_family": "JetBrains Mono",
    "line_height": {
      "custom": 3,
    },
    "font_size": 12.0,
  },

  // Git
  "git": {
    "inline_blame": {
      "enabled": false,
    },
  },

  // Toolbar do editor
  "toolbar": {
    "breadcrumbs": false,
    "quick_actions": false,
  },

  // Por linguagem: formata com Prettier + corrige ESLint ao salvar
  "languages": {
    "JavaScript": {
      "format_on_save": "on",
      "code_actions_on_format": {
        "source.fixAll.eslint": true,
      },
      "formatter": {
        "external": {
          "command": "prettier",
          "arguments": ["--stdin-filepath", "{buffer_path}"],
        },
      },
    },
    "TypeScript": {
      "format_on_save": "on",
      "code_actions_on_format": {
        "source.fixAll.eslint": true,
      },
      "formatter": {
        "external": {
          "command": "prettier",
          "arguments": ["--stdin-filepath", "{buffer_path}"],
        },
      },
    },
    "TSX": {
      "format_on_save": "on",
      "code_actions_on_format": {
        "source.fixAll.eslint": true,
      },
      "formatter": {
        "external": {
          "command": "prettier",
          "arguments": ["--stdin-filepath", "{buffer_path}"],
        },
      },
    },
  },
}
