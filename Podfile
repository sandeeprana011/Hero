

target 'HeroExamples' do
  platform :ios, '10.0'
  use_frameworks!
  pod 'CollectionKit', :inhibit_warnings => true

  target 'HeroTests' do
    inherit! :search_paths
  end
end

target 'HeroTvOSExamples' do
  platform :tvos, '10.0'
  use_frameworks!
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '15.0' #set your minimum version your all pods will set to mininum 13.1 version :-)
    end
  end
end
