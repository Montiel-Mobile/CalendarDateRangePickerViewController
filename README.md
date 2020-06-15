# CalendarDateRangePickerViewController

## Usage

It's as simple as:

```swift
let dateRangePickerViewController = CalendarDateRangePickerViewController()
dateRangePickerViewController.delegate = self
let navigationController = UINavigationController(rootViewController: dateRangePickerViewController)
self.navigationController?.present(navigationController, animated: true, completion: nil)
```

Just implement the delegate methods:

```swift
protocol CalendarDateRangePickerViewControllerDelegate {
    func didCancelPickingDateRange()
    func didPickDateRange(startDate: Date, endDate: Date)
}
```

You can also set additional options to override the defaults:

```swift
dateRangePickerViewController.minimumDate = Date()
dateRangePickerViewController.maximumDate = Calendar.current.date(byAdding: .year, value: 2, to: Date())
dateRangePickerViewController.selectedStartDate = Date()
dateRangePickerViewController.selectedEndDate = Calendar.current.date(byAdding: .day, value: 10, to: Date())
dateRangePickerViewController.selectedColor = UIColor.red
dateRangePickerViewController.navBarBarTintColor = UIColor.blue
dateRangePickerViewController.navBarTintColor = UIColor.white
dateRangePickerViewController.navBarTitleTextAttributes = [NSAttributedString.Key.foregroundColor: UIColor.black, NSAttributedString.Key.font: UIFont.system as Any]
dateRangePickerViewController.titleText = "Select Date Range"
```

## Author

miraan, miraan@triprapp.com

## License

CalendarDateRangePickerViewController is available under the MIT license. See the LICENSE file for more info.
