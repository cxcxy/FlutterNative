platform :ios, '9.0'
install! 'cocoapods',:deterministic_uuids => false
flutter_application_path = '../flutter_module'
load File.join(flutter_application_path, '.ios', 'Flutter', 'podhelper.rb')
target 'flutter-demo' do
    inhibit_all_warnings!
	use_frameworks!
  install_all_flutter_pods(flutter_application_path)
#  pod 'flutter_ios_text_lib', :path => '../flutter_ios_text_lib'
  pod 'Moya'
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['ENABLE_BITCODE'] = 'NO'
        end
    end
end


