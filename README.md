<div class="container">
    <h1>Guia do Desenvolvedor: Clonar & Migrar</h1>
    <div class="subhead">
        📘 Baixe este projeto e configure no <strong>seu próprio GitHub</strong> de forma rápida, segura e sem erros.
    </div>

   <!-- PASSO 1 -->
  <h2>📥 Passo 1: Baixar o código original</h2>
    <p>Abra o terminal na pasta desejada e execute os comandos abaixo para clonar o repositório e entrar no diretório:</p>
    <div class="code-block">
        <div class="terminal">
            <code>git clone https://github.com/Luann8/LACIA-16-04.git</code><br>
            <code>cd LACIA-16-04</code>
        </div>
        <button class="copy-btn" data-cmd="git clone https://github.com/Luann8/LACIA-16-04.git&#10;cd LACIA-16-04">📋 Copiar</button>
    </div>
    <p><span class="inline-code">💡 Dica:</span> Certifique-se de ter o Git instalado. Para verificar: <span class="inline-code">git --version</span></p>

    <!-- PASSO 2 -->
   <h2>🔗 Passo 2: Desvincular do dono atual</h2>
    <p>Remova a conexão com o repositório original (origin) para que você possa vincular ao seu próprio repositório remoto:</p>
    <div class="code-block">
        <div class="terminal">
            <code>git remote remove origin</code>
        </div>
        <button class="copy-btn" data-cmd="git remote remove origin">📋 Copiar</button>
    </div>
    <div class="important">
        ⚠️ <strong>Importante:</strong> Após esse comando, o repositório local fica completamente independente. Você pode confirmar com <span class="inline-code">git remote -v</span> — nenhum remote deve aparecer.
    </div>

    <!-- PASSO 3 -->
  <h2>🌐 Passo 3: Conectar ao SEU repositório</h2>
    <p>No GitHub, <strong>crie um novo repositório vazio</strong> (sem README, .gitignore ou licença). Copie a URL HTTPS ou SSH do seu repositório e então execute:</p>
    <div class="code-block">
        <div class="terminal">
            <code>git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git</code>
        </div>
        <button class="copy-btn" data-cmd="git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git">📋 Copiar template</button>
    </div>
    <p>🔁 Substitua <span class="inline-code">SEU_USUARIO</span> e <span class="inline-code">SEU_REPOSITORIO</span> pelo seu nome de usuário e nome do repositório criado.</p>

    <!-- PASSO 4 -->
  <h2>🚀 Passo 4: Padronizar e Enviar (Main)</h2>
    <p>Renomeie a branch atual para <span class="inline-code">main</span> (evitando conflitos com 'master') e faça o primeiro push vinculando a upstream:</p>
    <div class="code-block">
        <div class="terminal">
            <code>git branch -M main</code><br>
            <code>git push -u origin main</code>
        </div>
        <button class="copy-btn" data-cmd="git branch -M main&#10;git push -u origin main">📋 Copiar comandos</button>
    </div>
    
    <!-- Aviso Vim -->
    <div class="important">
        <strong>⌨️ Atenção Vim / Editor inesperado:</strong> Se o terminal "travar" em uma tela de texto (editor padrão, ex: commit message ou merge), pressione <kbd>Esc</kbd>, digite <code>:q!</code> e aperte <code>Enter</code> para sair sem salvar. Se for um editor nano, use <code>Ctrl+X</code>.
    </div>

    <!-- Dicas de uso diário -->
   <h2>📌 Dicas de Uso Diário (Fluxo Git essencial)</h2>
    <div class="tips-grid">
        <p>✅ Salvar alterações localmente (stage + commit):</p>
        <div class="code-block" style="margin-bottom: 1rem;">
            <div class="terminal" style="margin-top: 0.2rem;">
                <code>git add .</code><br>
                <code>git commit -m "mensagem descritiva"</code>
            </div>
            <button class="copy-btn" data-cmd="git add .&#10;git commit -m \"mensagem descritiva\"">📋 Copiar</button>
        </div>
        <p>📤 Enviar para o GitHub (após commit):</p>
        <div class="code-block">
            <div class="terminal" style="margin-top: 0.2rem;">
                <code>git push</code>
            </div>
            <button class="copy-btn" data-cmd="git push">📋 Copiar</button>
        </div>
        <p>📜 Sair do log (visualização de histórico de commits):</p>
        <div class="terminal" style="margin-top: 0.5rem;">
            <code>git log</code>
        </div>
        <p>Para sair da lista, pressione a tecla <kbd>q</kbd> (quit). Use <span class="inline-code">git log --oneline</span> para uma visão compacta.</p>
        <p>🔍 Verificar status e remotos:</p>
        <div class="terminal">
            <code>git status</code><br>
            <code>git remote -v</code>
        </div>
    </div>

    <!-- BÔNUS: Fluxo completo + explicação extra -->
    <hr>
  <h2>🧠 Fluxo Completo (resumo visual)</h2>
    <div style="background: #eef2f5; border-radius: 1rem; padding: 1.2rem; margin: 0.5rem 0;">
        <p><strong>1️⃣ Clone → 2️⃣ Remove origin → 3️⃣ Adiciona novo remote → 4️⃣ Push -u main</strong><br>
        Após isso, seu fork pessoal está configurado. Toda vez que fizer alterações: <span class="inline-code">git add .</span>, <span class="inline-code">git commit -m "msg"</span> e <span class="inline-code">git push</span>.</p>
        <p>💡 Para baixar atualizações de outro repositório (caso queira sincronizar com o original depois), você pode adicionar um remote "upstream", mas o guia foca em migração total.</p>
    </div>

  <div class="important" style="background:#e7f0fa; border-left-color:#2c7da0;">
        🎯 <strong>Objetivo alcançado:</strong> Agora o projeto está 100% vinculado ao SEU GitHub! Você pode compartilhar, colaborar ou continuar desenvolvendo.
    </div>

    <!-- FAQ rápido sobre problemas comuns -->
  <h2>🛠️ Solução de problemas comuns</h2>
    <ul>
        <li><strong>Erro "fatal: remote origin already exists"</strong> → Execute <span class="inline-code">git remote remove origin</span> novamente ou <span class="inline-code">git remote set-url origin NOVA_URL</span>.</li>
        <li><strong>Push rejeitado (fetch first)</strong> → Use <span class="inline-code">git pull origin main --allow-unrelated-histories</span> (cuidado, somente se houver commits no GitHub vazio). Normalmente repositório vazio não causa isso.</li>
        <li><strong>Não consigo sair do Vim/Nano?</strong> → Vim: <kbd>Esc</kbd> + <code>:q!</code> + Enter. Nano: <kbd>Ctrl</kbd>+<kbd>X</kbd>.</li>
        <li><strong>Esqueci de mudar a branch para main?</strong> → Use <span class="inline-code">git branch -M main</span> antes do push.</li>
        <li><strong>Quero ver meu histórico de commits:</strong> <span class="inline-code">git log --oneline --graph</span> → saia com <kbd>q</kbd>.</li>
    </ul>

  <div class="footer-note">
        ⚡ Guia prático para devs — construído com HTML/CSS puro e funcionalidade de copiar comandos.<br>
        Repositório original: <strong>Luann8/LACIA-16-04</strong> • Transforme e publique no seu GitHub agora.
    </div>
</div>
