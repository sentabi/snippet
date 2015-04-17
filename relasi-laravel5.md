daripada latih erban masing-masing variabel bagi 
```
$componentmodel = ComponentModel::with('relasiManufacture','relasiComponenttype')->get();
return view('componentmodel.index', compact('componentmodel'));
```
padin i tulis 
``
$componentmodelproductmap = ComponentModelProductMap::all();
return view('componentmodelproductmap.index', compact('componentmodelproductmap'));
``
la latih erbansa sada-sada janah lebih gendek scriptna, tading nambah relasina saja tapi bas controller-ta la man gantin kai pe. Bas viewna saja ganti contoh
```
{{ $data->component_model_id }}
```
ku
```
{{ $data->relasiComponentModel->component_model }}
```
