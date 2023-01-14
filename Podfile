# Uncomment the next line to define a global platform for your project
platform :ios, '9.0'

source 'https://github.com/CocoaPods/Specs.git'


plugin 'cocoapods-zjbinary'
 #静态库预编译编译
#use_frameworks! :linkage => :static
use_static_binary!
#set_default_desktop_cache_path!
set_local_binary_cache_path '/Users/zhouzj/Documents/binaryCache'

## 动态库预编译
#use_frameworks!
#use_dynamic_binary!
#
##remove_source_code_for_prebuilt_frameworks!

target 'BinaryDemo' do
  pod 'AFNetworking', '~> 4.0',:binary=>false
  pod 'SDWebImage'

end
  post_install do |installer|
    installer.pods_project.targets.each do |target|
      target.build_configurations.each do |config|
        config.build_settings['CODE_SIGN_IDENTITY'] = ''
      end
    end
  end

