<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <!-- Card de buscas -->
                <card-component title="Busca de marcas">

                    <template v-slot:content>
                        <div class="form-row">
                            <div class="col mb-3">
                                <input-component title="Código" id="inputId" id-help="idHelp" text-help="Opcional. Informe o codigo da marca">
                                    <input type="number" class="form-control" id="inputId" aria-describedby="idHelp" placeholder="Código">
                                </input-component>
                            </div>

                            <div class="col mb-3">
                                <input-component title="Nome da Marca" id="inputName" id-help="nameHelp" text-help="Opcional. Informe o nome da marca">
                                    <input type="text" class="form-control" id="inputName" aria-describedby="nameHelp" placeholder="Nome da marca">
                                </input-component>
                            </div>
                        </div>
                    </template>

                    <template v-slot:rodape>
                        <button type="submit" class="btn btn-primary btn-sm float-right">Pesquisar</button> 
                    </template>

                </card-component>

                <!-- Card de listagem de marcas -->
                <card-component title="Relação de marcas">
                    <template v-slot:content>
                        <table-component></table-component>
                    </template>

                    <template v-slot:rodape>
                        <button type="button" class="btn btn-primary btn-sm float-right" data-toggle="modal" data-target="#modalBrand">Adicionar</button> 
                    </template>
                </card-component>

            </div>
        </div>

        <modal-component id="modalBrand" title="Adicionar marca">
            <template v-slot:content>
                <div class="form-group">
                    <input-component title="Nome da Marca" id="newName" id-help="newNameHelp" text-help="Informe o nome da marca">
                        <input type="text" class="form-control" id="newName" aria-describedby="newNameHelp" placeholder="Nome da marca">
                    </input-component>
                </div>

                <div class="form-group">
                    <input-component title="Imagem" id="newImage" id-help="newImageHelp" text-help="Selecione uma imagem no formato PNG">
                        <input type="file" class="form-control-file" id="newImage" aria-describedby="newImageHelp" placeholder="Selecione uma imagem">
                    </input-component>
                </div>
            </template>

            <template v-slot:rodape>
                <button type="button" class="btn btn-secondary" data-dismiss="modal">Fechar</button>
                <button type="button" class="btn btn-primary">Salvar</button>
            </template>
        </modal-component>
    </div>
</template>

<script>

</script>