<template>
    <div class="mail container-fluid">
        <div class="row">
            <div class="col-xl-2 col-lg-3 col-md-3 col-sm-3 col-4">
                <ul class="list-group">
                    <li class="list-group-item header">
                        <img src="../../../public/images/design/receive.png" class="header-image" alt="..."> Received
                    </li>
                    <li class="list-group-item float-left">
                        <router-link class="sideRouter" to="/home">Done</router-link>
                        <span class="number float-right">150/71</span>
                    </li>

                    <li class="list-group-item active">Undone <span class="number float-right">150/71</span></li>


                    <li class="list-group-item header">
                        <img src="../../../public/images/design/send.png" class="header-image" alt="..."> Send
                    </li>
                    <li class="list-group-item float-left">
                        <router-link class="sideRouter" to="/home">Done</router-link>
                        <span class="number float-right">150/71</span>
                    </li>

                    <li class="list-group-item active">Undone <span class="number float-right">150/71</span></li>



                </ul>
            </div>
            <div class="col-xl-10 col-lg-9 col-md-9 col-sm-9 col-8">
                <div class="org-title"><h4>Filter</h4></div>
                <div class="filter">
                    <div class="row">
                        <div class="col-xl-8 col-lg-12 col-md-12 col-sm-12 col-12">
                            <div class="filter-row">
                                <button class="btn btn-default mail-button"><img src="../../../public/images/design/envelope.png" alt="">Message</button>
                                <button class="btn btn-default mail-button"><img src="../../../public/images/design/save.png" alt="">Save</button>
                            </div>
                            <div class="row filter-row">
                                <div class="col-xl-4 col-lg-4 col-md-6 col-sm-12 col-12">
                                    <div class="row">
                                        <div class="col-xl-3 col-lg-2 col-md-3 col-sm-3 col-4">
                                            <p class="date-header">From</p>
                                        </div>
                                        <div class="col-xl-9 col-lg-10 col-md-9 col-sm-8 col-8">
                                            <div class="input-group">
                                                <date-picker v-model="date" :config="options"></date-picker>
                                                <div class="input-group-prepend">
                                                    <div class="input-group-text" id="btnGroupAddon">
                                                        <img src="../../../public/images/design/date.png" alt="...">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="col-xl-4 col-lg-4 col-md-6 col-sm-12 col-12">
                                    <div class="row">
                                        <div class="col-xl-1 col-lg-2 col-md-3 col-sm-3 col-4">
                                            <p class="date-header">To</p>
                                        </div>
                                        <div class="col-xl-9 col-lg-10 col-md-9 col-sm-8 col-8">
                                            <div class="input-group">
                                                <date-picker v-model="date2" :config="options"></date-picker>
                                                <div class="input-group-prepend">
                                                    <div class="input-group-text">
                                                        <img src="../../../public/images/design/date.png" alt="...">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="col-xl-4 col-lg-4 col-md-6 col-sm-12 col-12">
                                    <div class="row">
                                        <div class="col-xl-5 col-lg-5 col-md-4 col-sm-3 col-4">
                                            <p class="date-header order-header">Order &#8470;</p>
                                        </div>
                                        <div class="col-xl-7 col-lg-7 col-md-8 col-sm-8 col-8">
                                            <input class="input-txt" type="text">
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xl-4 col-lg-4 col-md-6 col-sm-12 col-12">
                                    <div class="row">
                                        <div class="col-xl-3 col-lg-2 col-md-3 col-sm-3 col-4">
                                            <p class="date-header">Ex.fr</p>
                                        </div>
                                        <div class="col-xl-9 col-lg-10 col-md-9 col-sm-8 col-8">
                                            <div class="input-group">
                                                <date-picker v-model="date" :config="options"></date-picker>
                                                <div class="input-group-prepend">
                                                    <div class="input-group-text">
                                                        <img src="../../../public/images/design/date.png" alt="...">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="col-xl-4 col-lg-4 col-md-6 col-sm-12 col-12">
                                    <div class="row">
                                        <div class="col-xl-1 col-lg-2 col-md-3 col-sm-3 col-4">
                                            <p class="date-header">To</p>
                                        </div>
                                        <div class="col-xl-9 col-lg-10 col-md-9 col-sm-8 col-8">
                                            <div class="input-group">
                                                <date-picker v-model="date2" :config="options"></date-picker>
                                                <div class="input-group-prepend">
                                                    <div class="input-group-text">
                                                        <img src="../../../public/images/design/date.png" alt="...">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="col-xl-4 col-lg-4 col-md-6 col-sm-12 col-12">
                                    <div class="row">
                                        <div class="col-xl-5 col-lg-5 col-md-4 col-sm-3 col-4">
                                            <p class="date-header order-header">Doc type</p>
                                        </div>
                                        <div class="col-xl-7 col-lg-7 col-md-8 col-sm-8 col-8">
                                            <div class="dropdown">
                                                <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton"
                                                        data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                                    Personal doc
                                                </button>
                                                <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                                                    <a class="dropdown-item" href="#">Action</a>
                                                    <a class="dropdown-item" href="#">Another action</a>
                                                    <a class="dropdown-item" href="#">Something else here</a>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-xl-8 col-lg-10 col-md-11 col-sm-11 col-11">

                                    <div class="option-row float-left">
                                        <div class="row">
                                            <div class="col-xl-3 col-lg-4 col-md-3 col-sm-2 col-12">
                                                <div class="custom-control custom-radio custom-control-inline float-left">
                                                    <input type="radio" id="customRadioInline1" name="customRadioInline1" class="custom-control-input">
                                                    <label class="custom-control-label" for="customRadioInline1">All</label>
                                                </div>
                                            </div>
                                            <div class="col-xl-4 col-lg-4 col-md-4 col-sm-5 col-12">
                                                <div class="custom-control custom-radio custom-control-inline float-left">
                                                    <input type="radio" id="customRadioInline2" name="customRadioInline1" class="custom-control-input">
                                                    <label class="custom-control-label" for="customRadioInline2">On control</label>
                                                </div>
                                            </div>
                                            <div class="col-xl-5 col-lg-4 col-md-5 col-sm-5 col-12">
                                                <div class="custom-control custom-radio custom-control-inline float-left">
                                                    <input type="radio" id="customRadioInline3" name="customRadioInline1" class="custom-control-input">
                                                    <label class="custom-control-label" for="customRadioInline3">Out of control</label>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="row filter-row">

                        <div class="col-xl-4 col-lg-6 col-md-8 col-sm-12 col-12">
                            <div class="row">
                                <div class="col-xl-4 col-lg-4 col-md-4 col-sm-4 col-5">
                                    <p class="date-header order-header">Correspondent?</p>
                                </div>
                                <div class="col-xl-5 col-lg-5 col-md-5 col-sm-4 col-5">
                                    <div class="dropdown">
                                        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton"
                                                data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                            Personal doc
                                        </button>
                                        <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                                            <a class="dropdown-item" href="#">Action</a>
                                            <a class="dropdown-item" href="#">Another action</a>
                                            <a class="dropdown-item" href="#">Something else here</a>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xl-2 col-lg-1 col-md-1 col-sm-1 col-1">
                                    <button class="btn btn-add"><img src="../../../public/images/design/add.png"></button>
                                </div>

                            </div>
                        </div>
                        <div class="col-xl-4 col-lg-6 col-md-8 col-sm-12 col-12">
                            <div class="row">
                                <div class="col-xl-4 col-lg-4 col-md-4 col-sm-4 col-5">
                                    <p class="date-header order-header">Correspondent?</p>
                                </div>
                                <div class="col-xl-5 col-lg-5 col-md-5 col-sm-4 col-5">
                                    <div class="dropdown">
                                        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton"
                                                data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                            Personal doc
                                        </button>
                                        <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                                            <a class="dropdown-item" href="#">Action</a>
                                            <a class="dropdown-item" href="#">Another action</a>
                                            <a class="dropdown-item" href="#">Something else here</a>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xl-2 col-lg-1 col-md-1 col-sm-1 col-1">
                                    <button class="btn btn-add"><img src="../../../public/images/design/add.png"></button>
                                </div>

                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
            <div class="doc-container">
                <!--<div class="doc-container">-->
                    <div class="doc-title"><h4>Nazoratdagi hujjatlar</h4></div>

                        <!-- Main table element -->
                        <b-row>
                            <b-col md="6" class="my-1">
                                <b-pagination
                                        :total-rows="totalRows"
                                        :per-page="perPage"
                                        size="sm"
                                        v-model="currentPage"
                                        class="my-0"
                                />
                            </b-col>
                        </b-row>


                        <b-table bordered
                                show-empty
                                stacked="md"
                                :items="items"
                                :fields="fields"
                                :current-page="currentPage"
                                :per-page="perPage"
                                :filter="filter"
                                :sort-by.sync="sortBy"
                                :sort-desc.sync="sortDesc"
                                :sort-direction="sortDirection"
                                @filtered="onFiltered"
                        >

                        <template slot="resolution" slot-scope="row">
                            <tr class="b-custom-table-row">
                                {{ row.value.person1 }}
                            </tr>
                            <tr class="b-custom-table-row">
                                {{ row.value.person2 }}
                            </tr>
                        </template>
                        <template slot="ijroDate" slot-scope="row">
                            <tr class="b-custom-table-row">
                                {{ row.value.date1 }}
                            </tr>
                            <tr class="b-custom-table-row">
                                {{ row.value.date2 }}
                            </tr>
                        </template>

                        <template slot="row-details" slot-scope="row">
                            <b-card>
                                <ul>
                                    <li v-for="(value, key) in row.item" :key="key">{{ key }}: {{ value }}</li>
                                </ul>
                            </b-card>
                        </template>
                        </b-table>

                <!--</div>-->
            </div>


        <router-view/>
    </div>

</template>
<script>
    import datePicker from 'vue-bootstrap-datetimepicker';
    import 'pc-bootstrap4-datetimepicker/build/css/bootstrap-datetimepicker.css';
    const items = [
            { number: 1, correspondent: 'Tashkent Region',typeOfDoc:'Bayon', regNumber:'25 exat',
                regDate: '12.02.2019', publishNumber: 'RK/12-15', publishDate:'10.02.2019', printedDate: '12.02.2019',
                content: 'Navroz celebration',
            resolution: {person1: 'Shokirov', person2: 'Soliev'},
                ijroDate: {date1: '12.03.2018', date2: '12.02.2019'},
            },
            { number: 2, correspondent: 'vazirlar Mahkamasi',typeOfDoc:'Bayon', regNumber:'25 exat',
                regDate: '12.02.2019', publishNumber: 'RK/12-15', publishDate:'10.02.2019', printedDate: '12.02.2019',
                content: 'Navroz celebration'},
            { number: 3, correspondent: 'Tashkent Region',typeOfDoc:'Bayon', regNumber:'25 exat',
                regDate: '12.02.2019', publishNumber: 'RK/12-15', publishDate:'10.02.2019', printedDate: '12.02.2019',
                content: 'Navroz celebration'},
            { number: 4, correspondent: 'Tashkent Region',typeOfDoc:'Bayon', regNumber:'25 exat',
                regDate: '12.02.2019', publishNumber: 'RK/12-15', publishDate:'10.02.2019', printedDate: '12.02.2019',
                content: 'Navroz celebration'},
            { number: 5, correspondent: 'vazirlar Mahkamasi',typeOfDoc:'Bayon', regNumber:'25 exat',
                regDate: '12.02.2019', publishNumber: 'RK/12-15', publishDate:'10.02.2019', printedDate: '12.02.2019',
                content: 'Navroz celebration'},
            { number: 6, correspondent: 'Tashkent Region',typeOfDoc:'Bayon', regNumber:'25 exat',
                regDate: '12.02.2019', publishNumber: 'RK/12-15', publishDate:'10.02.2019', printedDate: '12.02.2019',
                content: 'Navroz celebration'},



    ];

    export default {
        data () {
            return {
                date: new Date(''),
                date2: new Date(),
                options: {
                    format: 'DD.MM.YYYY',
                    useCurrent: false,
                },
                items: items,
                fields: [
                    { key: 'number', label: '№'},
                    { key: 'correspondent', label: 'Correspondent', sortable: true, class: 'text-center' },
                    { key: 'typeOfDoc', label: 'Type of docs' },
                    { key: 'regNumber', label: 'Registered Number' },
                    { key: 'regDate', label: 'Registered Date' },
                    { key: 'publishNumber', label: 'Published number' },
                    { key: 'publishDate', label: 'Published Date' },
                    { key: 'printedDate', label: 'Printed Date' },
                    { key: 'content', label: 'Content' },
                    { key: 'resolution', label: 'Rezolyutsiya' },
                    { key: 'ijroDate', label: 'Ijro muddati' }
                ],
                currentPage: 1,
                perPage: 5,
                totalRows: items.length,
                pageOptions: [5, 10, 15],
                sortBy: null,
                sortDesc: false,
                sortDirection: 'asc',
                filter: null,
                modalInfo: { title: '', content: '' }
            }

        },
        computed: {
            sortOptions() {
                // Create an options list from our fields
                return this.fields
                    .filter(f => f.sortable)
                    .map(f => {
                        return { text: f.label, value: f.key }
                    })
            }
        },
        methods: {
            info(item, index, button) {
                this.modalInfo.title = `Row index: ${index}`
                this.modalInfo.content = JSON.stringify(item, null, 2)
                this.$root.$emit('bv::show::modal', 'modalInfo', button)
            },
            resetModal() {
                this.modalInfo.title = '';
                this.modalInfo.content = ''
            },
            onFiltered(filteredItems) {
                // Trigger pagination to update the number of buttons/pages due to filtering
                this.totalRows = filteredItems.length
                this.currentPage = 1
            }
        },
        components: {
            datePicker

        }

    }



</script>
<style scoped>

    .b-custom-table-row{
        width: 100%;
        margin-top: 0;
        height: auto;
        display: block;
    }

    .b-custom-table-hr{
        margin-left: -15%;
        width: 130%;
    }
    .mail{
        margin-top: 10px;
    }

    .org-title{
        height: 49px;
        background: #F4F4F4;
        border: 1px solid #E7E7E7;
        box-sizing: border-box;
        padding-top: 1%;
    }
    .org-title h4{
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: bold;
        line-height: normal;
        font-size: 18px;
        text-align: center;
        color: #474747;
    }
    .doc-title{
        height: 49px;
        border-bottom: 1px solid #E7E7E7;
        box-sizing: border-box;
        padding: 1%;
    }
    .doc-title h4{
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: bold;
        line-height: normal;
        font-size: 18px;
        text-align: left;
        color: #474747;
    }
    .doc-container{
        margin-top: 1rem;
        border: 1px solid #E7E7E7;
        box-sizing: border-box;
        display: block;
        height: auto;
        padding: 0;
    }
    .sideRouter{
        color: inherit;
    }
    .sideRouter:hover{
        text-decoration: none;
    }
    .header-image{
        margin-right: 10px;
        margin-bottom: 4px;
    }
    .list-group{
        /*min-width: 150px;*/
    }
    .list-group .header{
        font-family: 'Lato', sans-serif;
        background: #008CBA;
        border: 1px solid #E7E7E7;
        box-sizing: border-box;
        border-radius: 3px 3px;
        font-style: normal;
        font-weight: bold;
        line-height: normal;
        font-size: 15px;
        padding: 10px;
        color: #FFFFFF;
    }

    .list-group .active{
        background: rgba(0, 0, 0, 0.05);
        border-right: #dfdfdf;
        border-left: #dfdfdf;
        border-top-color: #f2f2f2;
        border-bottom-color: #f2f2f2;

    }
    .list-group-item{
        border-radius: 0;
        padding: 10px;
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: normal;
        line-height: normal;
        font-size: 13px;
        text-align: left;

        color: #666666;


    }
    .number{
        text-align: right;
    }

    .filter{
        background: #FFFFFF;
        border: 1px solid #E7E7E7;
        box-sizing: border-box;
        border-radius: 0 0 3px 3px;

    }
    .filter-row .dropdown .btn{
        border: 1px solid #CCCCCC;
        box-sizing: border-box;
        border-radius: 3px;
        width: 100%;
        display: block;
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
        font-size: 11px;
        white-space: inherit;
        color: #727272;
    }
    .btn-add{
        border: 1px solid #CCCCCC;
        box-sizing: border-box;
        border-radius: 3px;
        display: block;
        padding: 0 4px;
        width: auto!important;
        position: absolute;
        left: -10px;
    }
    .filter-row{
        padding: 10px;
        text-align: left;
    }
    .filter-row .row{
        margin-bottom: 10px;
    }
    .mail-button{
        background: #F6F6F6;
        border: 1px solid #CCCCCC;
        box-sizing: border-box;
        border-radius: 3px;
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: normal;
        line-height: normal;
        font-size: 14px;
        color: #727272;
        height: 30px;
        margin-right: 10px;
    }
    h6{
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
        font-size: 15px;
        margin-bottom: 15px;
        color: #3F4756;


    }

    .mail-button img{
        margin-right: 6px;
        margin-bottom: 2px;
    }
    .date-header{
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
        font-size: 15px;
        color: #3F4756;
        display: table-cell;
        padding: 4px 2px;
    }
    .order-header{
        position: absolute;

    }
    .form-control{
        height: calc(1.2em + .75rem);
    }
    .form-control:focus{
        border-color: #e9ecef;
        box-shadow: 0 0 0 0.2rem rgba(233, 236, 239, 0.13);
    }
    .input-group>.input-group-prepend>.input-group-text{
        border-top-right-radius: .25rem;
        border-bottom-right-radius: .25rem;
    }
    .input-group>.form-control:not(:last-child) {
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
        font-size: 15px;
        color: #727272;
    }

    .input-txt{
        border: 1px solid #CCCCCC;
        box-sizing: border-box;
        border-radius: 3px;
        width: 100%;
        position: relative;

    }

    .option-row{
        border: 1px solid #CCCCCC;
        box-sizing: border-box;
        border-radius: 3px;
        margin: 10px;
        padding: 10px;
        width: 100%;
    }
    .page-link{
        border: none;
        font-family: 'Lato', sans-serif;
        font-style: normal;
        font-weight: normal;
        line-height: normal;
        font-size: 12px;
        letter-spacing: 0.4em;

        color: #474747;
        text-align: center;
        padding: 1px 2px;
        display: block;
    }
    .page-item.active .page-link {
        z-index: 1;
        color: #474747;
        background-color: transparent;

        border: 1.4px solid #474747;
        border-radius: 1px;
        text-align: center;
    }
</style>