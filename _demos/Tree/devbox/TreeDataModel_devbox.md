TreeView는 일반적인 트리 UI와 동일하게 부모 자식 관계를 갖는 데이터셋을 표시하고 관리하는 툴입니다. 다만, 리얼그리드의 TreeView는 GridView와 같이 컬럼셋을 지정할 수 있고, TreeView의 각 행(노드)은 컬럼셋에 해당하는 속성들을 갖게 됩니다. 각 컬럼은 TreeView에 연결된 데이터 제공자의 데이터필드에 연결됩니다.
TreeView의 데이터 제공자인 TreeDataProvider의 데이터셋은 Json, Xml, Csv 등 다양한 소스로 부터 구성될 수 있습니다. TreeDataProvider에 추가된 데이터행들은 부모/자식 관계를 갖는 구조로 재구성되며 원본 데이터셋 내에서의 위치 정보는 유지하지 않습니다. 하지만, 원본의 각 행이 TreeDataProvider의 데이터행으로 추가될 때 rowId 라는 유일한 키값이 행별로 지정되고, 이 후 Javascript 등에서는 이 값으로 TreeDataProvider의 데이터행을 추적할 수 있습니다. CellIndex의 dataRow나 함수, callback등에서 dataRow는 rowId를 의미합니다.
TreeView의 Item Model은 GridView와 동일하고, 각 item은 TreeDataProvider의 한 행을 표시합니다. GridView와 다르게 RowGrouping은 지원하지 않습니다. 또, Sorting이나 Filtering은 계층 구조 내에서 진행됩니다. 예를 들어, 부모 행이 Filtering에서 제외되면 자식 행들 역시 자동적으로 제외됩니다. 마찬가지로 Sorting이 계층 구조를 변경하지는 않고, 자식들을 정렬하게 됩니다.