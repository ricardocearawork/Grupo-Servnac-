# Grupo-Servnac-
Solicitação de Uniforme 
function enviarWhatsApp(event) {
    event.preventDefault();

    // Obter valores do formulário
    const nome = document.querySelector('input[name="nome"]').value;
    const matricula = document.querySelector('input[name="matricula"]').value;
    const empresa = document.querySelector('select[name="empresa"]').value;
    const postoNome = document.querySelector('input[name="posto_nome"]').value;
    const postoCidade = document.querySelector('input[name="posto_cidade"]').value;
    const cadastroTipo = document.querySelector('select[name="cadastro_tipo"]').value;
    const turno = document.querySelector('select[name="turno"]').value;
    const camisa = document.querySelector('select[name="tamanho_camisa"]').value;
    const colete = document.querySelector('select[name="tamanho_colete"]').value;
    const calca = document.querySelector('select[name="tamanho_calca"]').value;
    const calcado = document.querySelector('select[name="tamanho_calcado"]').value;

    // Validar se todos os campos foram preenchidos
    if (!nome || !matricula || !empresa || !postoNome || !postoCidade || !cadastroTipo || !turno || !camisa || !colete || !calca || !calcado) {
        alert('⚠️ Por favor, preencha todos os campos antes de enviar!');
        return;
    }

    // Formatar mensagem
    const mensagem = `*SOLICITAÇÃO DE UNIFORME*%0A%0A` +
        `*DADOS DO COLABORADOR*%0A` +
        `Nome: ${nome}%0A` +
        `Matrícula: ${matricula}%0A` +
        `Empresa: ${empresa}%0A%0A` +
        `*INFORMAÇÕES DO POSTO*%0A` +
        `Posto: ${postoNome}%0A` +
        `Cidade: ${postoCidade}%0A` +
        `Status: ${cadastroTipo}%0A` +
        `Turno: ${turno}%0A%0A` +
        `*TAMANHOS*%0A` +
        `Camisa: ${camisa}%0A` +
        `Colete: ${colete}%0A` +
        `Calça: ${calca}%0A` +
        `Sapato/Coturno: ${calcado}%0A%0A` +
        `*IMPORTANTE*%0A` +
        `Enviar foto para crachá em anexo.`;

    // Número do WhatsApp (sem caracteres especiais)
    const numero = '5585992250785';

    // Link do WhatsApp
    const linkWhatsApp = `https://wa.me/${numero}?text=${mensagem}`;

    // Abrir WhatsApp
    window.open(linkWhatsApp, '_blank');
}
