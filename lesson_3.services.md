##### routing: angularJS có routing riêng và dùng chúng để trỏ tới module, module đã được mô tả controller, controller tạo model thông qua $scope. sử dụng module và controller trong template. data binding giữa view và model đã được định nghĩa qua $scope

# danh sách services trong angular

###### http:

# $http.get() Perform Http GET request.

# $http.head() Perform Http HEAD request.

# $http.post() Perform Http POST request.

# $http.put() Perform Http PUT request.

# $http.delete() Perform Http DELETE request.

# $http.jsonp() Perform Http JSONP request.

# $http.patch() Perform Http PATCH request

# $inject $http trong function controller

## $http.get > HttpPromise $http.get(url)

var onSuccess = function (data, status, headers, config) {
$scope.data = data
}

var onError = function (data, status, headers, config) {
$scope.error = status;
}

# var promise = $http.get("/demo/getdata").success(onSuccess).error(onError);

## $http.post > HttpPromise $http.post(url, dataToSubmit)

# var promise = $http.post('/demo/submitData', { myData: 'Hello World!' }).success(onSuccess).error(onError);

## $http()

var getReq = {
method: 'GET',
url: '/demo/getdata'
};

# $http(getReq).success(onSuccess).error(onError);

var postReq = {
method: 'POST',
url: '/demo/submitData',
data: { myData: 'test data' }
};

# $http(postReq).success(onSuccess).error(onError);

##### interval

## $interval(fn, delay, [count], [invokeApply], [Pass])

# $scope.counter = 0;

var increaseCounter = function () {

# $scope.counter = $scope.counter + 1;

}
#$interval(increaseCounter, 1000, 10);

#

$anchorScroll
$exceptionHandler
$interval
$rootScope
$animate
$filter
$locale
$sceDelegate
$cacheFactory
$httpParamSerializer
$location
$sce
$templateCache
$httpParamSerializerJQLike
$log
$templateRequest
$compile
$http
$parse
$timeout
$controller
$httpBackend
$q
$window
$document
$interpolate
$rootElement
