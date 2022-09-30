# data binding: đồng bộ dữ liệu giữa view và model

# scope: Đối tượng có khả năng truy cập giữa các model.

scope giúp controller và view có thể liên kết với nhau

# controller: những chức năng javascript được liên kết với một view cụ thể

# services: angularjs đi kèm với một số các service được xây dựng sẵn

ví dụ như $http: để thực hiện một XMLHttpRequests. Services là các singleton,
tạo một lần duy nhất, sử dụng ở mọi nơi.

# filers: filters giống như một bộ lọc, format lại dữ liệu gốc sau đó

hiển thị ra ngoài view cho người dùng

# directives: gắn lên tag html, cho phép tuỳ chỉnh lại các tính năng, phần tử,...như gắn lên input

# templates: các files html, nó được controller gọi và binding data từ model.

##### routing: angularJS có routing riêng và dùng chúng để trỏ tới module, module đã được mô tả controller, controller tạo model. sử dụng module và controller trong template. data binding giữa model và view

# denpendence injection (DJ): chúng ta sử dụng để có thể inject các service và sử dụng chúng

# chúng ta có thể inject service trong service, factory, controller,

# syntax: any.$inject = ['...',...]

# example:

# angular.module(AppConf.appModule).service('ReportRequest', ReportRequest);

ReportRequest.$inject = ['$http', 'Authentication', 'Utils'];
unction ReportRequest(http, authencitation, utils) {}

# angular.module(AppConf.appModule).factory('Authentication', userAuthentication);

userAuthentication.$inject = ['$localStorage', '$sessionStorage', 'UserData'];

# angular.module(AppConf.appModule).controller('materialImportController', materialImportController);

materialImportController.$inject = ['$scope', 'Utils', 'ExcelUtils', 'ApiRequest', 'ImportStoreData'];
