##### routing: angularJS có routing riêng và dùng chúng để trỏ tới module, module đã được mô tả controller, controller tạo model. sử dụng module và controller trong template. data binding giữa model và view

# modules & controller

# module:

module là một container, nó có thể chứa mọi thứ để tạo một application như services, controllers,
filters, directives,... hoặc chỉ chứ một trong số chúng

# tạo một mođule:

var [name] = angular.module('[module_name]', [(1)])
(1): một array khai báo các dependence mà module này phụ thuộc.

# controller:

controller là một hàm js, vai trò dựng lên model và thông view sẽ lấy ra để hiển thị.
controller mở rộng mô tả của mộ module

# tạo một controller:

[module_name].controller([controller_name], [function_controller_name])

[function_controller_name].$inject = [(2)]

function function_controller_name(services) {}

(2) là một mảng các services có thể của angular hoặc do mình tự định nghĩa.
các service này sẽ được đưa vào làm tham số của [function_controller_name]
