<script setup lang="ts" generic="T">
import BaseComponent from 'primevue/basecomponent';
import DataTableStyle from 'primevue/datatable/style';

defineOptions({
    name: 'BaseDataTable',
    extends: BaseComponent,
    // props: {
    //     value: {
    //         type: Array,
    //         default: null
    //     },
    //     dataKey: {
    //         type: [String, Function],
    //         default: null
    //     },
    //     rows: {
    //         type: Number,
    //         default: 0
    //     },
    //     first: {
    //         type: Number,
    //         default: 0
    //     },
    //     totalRecords: {
    //         type: Number,
    //         default: 0
    //     },
    //     paginator: {
    //         type: Boolean,
    //         default: false
    //     },
    //     paginatorPosition: {
    //         type: String,
    //         default: 'bottom'
    //     },
    //     alwaysShowPaginator: {
    //         type: Boolean,
    //         default: true
    //     },
    //     paginatorTemplate: {
    //         type: [Object, String],
    //         default: 'FirstPageLink PrevPageLink PageLinks NextPageLink LastPageLink RowsPerPageDropdown'
    //     },
    //     pageLinkSize: {
    //         type: Number,
    //         default: 5
    //     },
    //     rowsPerPageOptions: {
    //         type: Array,
    //         default: null
    //     },
    //     currentPageReportTemplate: {
    //         type: String,
    //         default: '({currentPage} of {totalPages})'
    //     },
    //     lazy: {
    //         type: Boolean,
    //         default: false
    //     },
    //     loading: {
    //         type: Boolean,
    //         default: false
    //     },
    //     loadingIcon: {
    //         type: String,
    //         default: undefined
    //     },
    //     sortField: {
    //         type: [String, Function],
    //         default: null
    //     },
    //     sortOrder: {
    //         type: Number,
    //         default: null
    //     },
    //     defaultSortOrder: {
    //         type: Number,
    //         default: 1
    //     },
    //     nullSortOrder: {
    //         type: Number,
    //         default: 1
    //     },
    //     multiSortMeta: {
    //         type: Array,
    //         default: null
    //     },
    //     sortMode: {
    //         type: String,
    //         default: 'single'
    //     },
    //     removableSort: {
    //         type: Boolean,
    //         default: false
    //     },
    //     filters: {
    //         type: Object,
    //         default: null
    //     },
    //     filterDisplay: {
    //         type: String,
    //         default: null
    //     },
    //     globalFilterFields: {
    //         type: Array,
    //         default: null
    //     },
    //     filterLocale: {
    //         type: String,
    //         default: undefined
    //     },
    //     selection: {
    //         type: [Array, Object],
    //         default: null
    //     },
    //     selectionMode: {
    //         type: String,
    //         default: null
    //     },
    //     compareSelectionBy: {
    //         type: String,
    //         default: 'deepEquals'
    //     },
    //     metaKeySelection: {
    //         type: Boolean,
    //         default: false
    //     },
    //     contextMenu: {
    //         type: Boolean,
    //         default: false
    //     },
    //     contextMenuSelection: {
    //         type: Object,
    //         default: null
    //     },
    //     selectAll: {
    //         type: Boolean,
    //         default: null
    //     },
    //     rowHover: {
    //         type: Boolean,
    //         default: false
    //     },
    //     csvSeparator: {
    //         type: String,
    //         default: ','
    //     },
    //     exportFilename: {
    //         type: String,
    //         default: 'download'
    //     },
    //     exportFunction: {
    //         type: Function,
    //         default: null
    //     },
    //     resizableColumns: {
    //         type: Boolean,
    //         default: false
    //     },
    //     columnResizeMode: {
    //         type: String,
    //         default: 'fit'
    //     },
    //     reorderableColumns: {
    //         type: Boolean,
    //         default: false
    //     },
    //     expandedRows: {
    //         type: [Array, Object],
    //         default: null
    //     },
    //     expandedRowIcon: {
    //         type: String,
    //         default: undefined
    //     },
    //     collapsedRowIcon: {
    //         type: String,
    //         default: undefined
    //     },
    //     rowGroupMode: {
    //         type: String,
    //         default: null
    //     },
    //     groupRowsBy: {
    //         type: [Array, String, Function],
    //         default: null
    //     },
    //     expandableRowGroups: {
    //         type: Boolean,
    //         default: false
    //     },
    //     expandedRowGroups: {
    //         type: Array,
    //         default: null
    //     },
    //     stateStorage: {
    //         type: String,
    //         default: 'session'
    //     },
    //     stateKey: {
    //         type: String,
    //         default: null
    //     },
    //     editMode: {
    //         type: String,
    //         default: null
    //     },
    //     editingRows: {
    //         type: Array,
    //         default: null
    //     },
    //     rowClass: {
    //         type: Function,
    //         default: null
    //     },
    //     rowStyle: {
    //         type: Function,
    //         default: null
    //     },
    //     scrollable: {
    //         type: Boolean,
    //         default: false
    //     },
    //     virtualScrollerOptions: {
    //         type: Object,
    //         default: null
    //     },
    //     scrollHeight: {
    //         type: String,
    //         default: null
    //     },
    //     frozenValue: {
    //         type: Array,
    //         default: null
    //     },
    //     responsiveLayout: {
    //         type: String,
    //         default: 'scroll'
    //     },
    //     breakpoint: {
    //         type: String,
    //         default: '960px'
    //     },
    //     showGridlines: {
    //         type: Boolean,
    //         default: false
    //     },
    //     stripedRows: {
    //         type: Boolean,
    //         default: false
    //     },
    //     highlightOnSelect: {
    //         type: Boolean,
    //         default: false
    //     },
    //     size: {
    //         type: String,
    //         default: null
    //     },
    //     tableStyle: {
    //         type: null,
    //         default: null
    //     },
    //     tableClass: {
    //         type: [String, Object],
    //         default: null
    //     },
    //     tableProps: {
    //         type: Object,
    //         default: null
    //     },
    //     filterInputProps: {
    //         type: null,
    //         default: null
    //     }
    // },
    style: DataTableStyle,
    provide() {
        return {
            $parentInstance: this
        };
    }
});

type DataTableProps = Partial<{
    value: Array<T>;
    dataKey: string | (() => string);
    rows: number;
    first: number;
    totalRecord: number;
    paginator: boolean;
    paginatorPosition: string;
    alwaysShowPaginator: boolean;
    paginatorTemplate: object | string;
    pageLinkSize: number;
    rowsPerPageOptions: Array<number>;
    currentPageReportTemplate: string;
    lazy: boolean;
    loading: boolean;
    loadingIcon: string;
    sortField: string | (() => string);
    sortOrder: number;
    defaultSortOrder: number;
    nullSortOrder: number;
    multiSortMeta: Array<string>; // TODO
    sortMode: string;
    removableSort: boolean;
    filters: object; // todo
    filterDisplay: string;
    globalFilterFields: Array<string>;
    filterLocale: string;
    selection: Array<T> | T;
    selectionMode: string;
    compareSelectionBy: string;
    metaKeySelection: boolean;
    contextMenu: boolean;
    contextMenuSelection: T; // todo
    selectAll: boolean;
    rowHover: boolean;
    csvSeparator: string;
    exportFilename: string;
    exportFunction: () => string;
    resizableColumns: boolean;
    columnResizeMode: string;
    reorderableColumns: boolean;
    expandedRows: Array<T> | T;
    expandedRowIcon: string;
    collapsedRowIcon: string;
    rowGroupMode: string;
    groupRowsBy: Array<string> | string | (() => string); // todo
    expandableRowGroups: boolean;
    stateStorage: string;
    stateKey: string;
    editMode: string;
    editingRows: Array<T>;
    rowClass: () => string; // todo
    rowStyle: () => string; // todo
    scrollable: boolean;
    virtualScrollerOptions: object; // todo
    scrollHeight: string;
    frozenValue: Array<string>; // todo
    responsiveLayout: string;
    breakpoint: string;
    showGridLines: boolean;
    stripedRows: boolean;
    highlightOnSelect: boolean;
    size: string;
    tableStyle: string; // todo
    tableClass: string | object; // todo
    tableProps: object; // todo
    filterInputProps: object; // todo
}>

withDefaults(defineProps<DataTableProps>(), {
    value: null,
    dataKey: null,
    rows: 0,
    first: 0,
    totalRecord: 0,
    paginator: false,
    paginatorPosition: 'bottom',
    alwaysShowPaginator: true,
    paginatorTemplate: 'FirstPageLink PrevPageLink PageLinks NextPageLink LastPageLink RowsPerPageDropdown',
    pageLinkSize: 5,
    rowsPerPageOptions: null,
    currentPageReportTemplate: '({currentPage} of {totalPages})',
    lazy: false,
    loading: false,
    loadingIcon: undefined,
    sortField: null,
    sortOrder: null,
    defaultSortOrder: 1,
    nullSortOrder: 1,
    multiSortMeta: null,
    sortMode: 'single',
    removableSort: false,
    filters: null,
    filterDisplay: null,
    globalFilterFields: null,
    filterLocale: undefined,
    selection: null,
    selectionMode: null,
    compareSelectionBy: 'deepEquals',
    metaKeySelection: false,
    contextMenu: false,
    contextMenuSelection: null,
    selectAll: null,
    rowHover: false,
    csvSeparator: ',',
    exportFilename: 'download',
    exportFunction: null,
    resizableColumns: false,
    columnResizeMode: 'fit',
    reorderableColumns: false,
    expandedRows: null,
    expandedRowIcon: undefined,
    collapsedRowIcon: undefined,
    rowGroupMode: null,
    groupRowsBy: null,
    expandableRowGroups: false,
    stateStorage: 'session',
    stateKey: null,
    editMode: null,
    editingRows: null,
    rowClass: null,
    rowStyle: null,
    scrollable: false,
    virtualScrollerOptions: null,
    scrollHeight: null,
    frozenValue: null,
    responsiveLayout: 'scroll',
    breakpoint: '960px',
    showGridLines: false,
    stripedRows: false,
    highlightOnSelect: false,
    size: null,
    tableStyle: null,
    tableClass: null,
    tableProps: null,
    filterInputProps: null,
});
</script>
