---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035767"
---
## <a name="280---october-2019"></a><span data-ttu-id="2e225-103">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="2e225-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2e225-104">General</span></span>
* <span data-ttu-id="2e225-105">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2e225-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2e225-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-106">Az.Accounts</span></span>
* <span data-ttu-id="2e225-107">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="2e225-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2e225-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e225-108">Az.ApiManagement</span></span>
* <span data-ttu-id="2e225-109">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="2e225-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="2e225-110">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="2e225-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-111">Az.Automation</span></span>
* <span data-ttu-id="2e225-112">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="2e225-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="2e225-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2e225-113">Az.Batch</span></span>
* <span data-ttu-id="2e225-114">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-115">Az.Compute</span></span>
* <span data-ttu-id="2e225-116">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="2e225-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2e225-117">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="2e225-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="2e225-118">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="2e225-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="2e225-119">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="2e225-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-120">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-121">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="2e225-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="2e225-122">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="2e225-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="2e225-123">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-125">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="2e225-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2e225-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2e225-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="2e225-127">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="2e225-128">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="2e225-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="2e225-129">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="2e225-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="2e225-130">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="2e225-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2e225-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2e225-131">Az.IotHub</span></span>
* <span data-ttu-id="2e225-132">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="2e225-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="2e225-133">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="2e225-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="2e225-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-134">Az.Monitor</span></span>
* <span data-ttu-id="2e225-135">Добавлены новые получатели групп действий для New-AzActionGroupReceiver: -ItsmReceiver, -VoiceReceiver,-ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="2e225-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="2e225-136">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="2e225-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="2e225-137">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e225-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="2e225-138">Веб-перехватчики теперь поддерживают аутентификацию на основе Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e225-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-139">Az.Network</span></span>
* <span data-ttu-id="2e225-140">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="2e225-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="2e225-141">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="2e225-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="2e225-142">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2e225-142">New cmdlets added:</span></span>
        - <span data-ttu-id="2e225-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2e225-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="2e225-144">В следующие командлеты добавлен необязательный параметр -TrafficSelectorPolicies:</span><span class="sxs-lookup"><span data-stu-id="2e225-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="2e225-145">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="2e225-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="2e225-146">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="2e225-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2e225-147">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="2e225-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="2e225-148">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="2e225-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="2e225-149">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2e225-150">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2e225-151">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2e225-152">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="2e225-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="2e225-153">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2e225-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="2e225-154">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2e225-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="2e225-155">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="2e225-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2e225-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2e225-156">Az.RedisCache</span></span>
* <span data-ttu-id="2e225-157">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="2e225-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-158">Az.Sql</span></span>
* <span data-ttu-id="2e225-159">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="2e225-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-160">Az.Storage</span></span>
* <span data-ttu-id="2e225-161">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="2e225-162">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="2e225-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2e225-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2e225-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="2e225-164">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="2e225-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2e225-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2e225-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2e225-166">Az.StorageSync</span></span>
* <span data-ttu-id="2e225-167">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="2e225-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-168">Az.Websites</span></span>
* <span data-ttu-id="2e225-169">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="2e225-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="2e225-170">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2e225-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e225-171">Az.ApiManagement</span></span>
* <span data-ttu-id="2e225-172">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="2e225-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="2e225-173">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="2e225-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="2e225-174">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2e225-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-175">Az.Automation</span></span>
* <span data-ttu-id="2e225-176">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="2e225-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="2e225-177">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="2e225-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="2e225-178">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="2e225-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-179">Az.Compute</span></span>
* <span data-ttu-id="2e225-180">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="2e225-181">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2e225-182">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="2e225-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="2e225-183">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="2e225-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="2e225-184">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="2e225-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="2e225-185">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="2e225-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="2e225-186">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="2e225-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="2e225-187">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="2e225-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="2e225-188">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2e225-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-189">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-190">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="2e225-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="2e225-191">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="2e225-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2e225-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2e225-192">Az.HDInsight</span></span>
* <span data-ttu-id="2e225-193">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="2e225-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2e225-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2e225-194">Az.IotHub</span></span>
* <span data-ttu-id="2e225-195">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="2e225-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="2e225-196">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="2e225-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="2e225-197">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2e225-197">New cmdlets are:</span></span>
    - <span data-ttu-id="2e225-198">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="2e225-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2e225-199">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="2e225-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2e225-200">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="2e225-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2e225-201">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="2e225-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2e225-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-202">Az.Monitor</span></span>
* <span data-ttu-id="2e225-203">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="2e225-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="2e225-204">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="2e225-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="2e225-205">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="2e225-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="2e225-206">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="2e225-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="2e225-207">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="2e225-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="2e225-208">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="2e225-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="2e225-209">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="2e225-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="2e225-210">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="2e225-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="2e225-211">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="2e225-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2e225-212">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="2e225-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="2e225-213">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="2e225-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2e225-214">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="2e225-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="2e225-215">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="2e225-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="2e225-216">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="2e225-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="2e225-217">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="2e225-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="2e225-218">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="2e225-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="2e225-219">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="2e225-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="2e225-220">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="2e225-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="2e225-221">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="2e225-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="2e225-222">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="2e225-222">Overall improved help files</span></span>
* <span data-ttu-id="2e225-223">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="2e225-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-224">Az.Network</span></span>
* <span data-ttu-id="2e225-225">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="2e225-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="2e225-226">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="2e225-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="2e225-227">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="2e225-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="2e225-228">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="2e225-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="2e225-229">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="2e225-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="2e225-230">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="2e225-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="2e225-231">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2e225-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="2e225-232">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="2e225-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="2e225-233">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="2e225-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="2e225-234">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="2e225-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="2e225-235">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="2e225-236">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="2e225-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="2e225-237">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-237">New cmdlets</span></span>
        - <span data-ttu-id="2e225-238">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="2e225-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="2e225-239">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="2e225-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="2e225-240">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2e225-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="2e225-241">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="2e225-241">New-VpnSite</span></span>
        - <span data-ttu-id="2e225-242">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="2e225-242">Update-VpnSite</span></span>
        - <span data-ttu-id="2e225-243">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="2e225-243">New-VpnConnection</span></span>
        - <span data-ttu-id="2e225-244">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="2e225-244">Update-VpnConnection</span></span>
* <span data-ttu-id="2e225-245">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="2e225-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-247">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="2e225-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="2e225-248">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2e225-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-249">Az.Resources</span></span>
* <span data-ttu-id="2e225-250">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="2e225-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2e225-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="2e225-252">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="2e225-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="2e225-253">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="2e225-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="2e225-254">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2e225-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2e225-255">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="2e225-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2e225-256">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="2e225-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2e225-257">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="2e225-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="2e225-258">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2e225-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2e225-259">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2e225-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2e225-260">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="2e225-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2e225-261">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="2e225-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2e225-262">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="2e225-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="2e225-263">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2e225-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2e225-264">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="2e225-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2e225-265">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="2e225-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2e225-266">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="2e225-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="2e225-267">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2e225-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2e225-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2e225-268">Az.SignalR</span></span>
* <span data-ttu-id="2e225-269">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="2e225-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-270">Az.Sql</span></span>
* <span data-ttu-id="2e225-271">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="2e225-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="2e225-272">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="2e225-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="2e225-273">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="2e225-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2e225-274">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="2e225-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="2e225-275">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="2e225-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-276">Az.Storage</span></span>
* <span data-ttu-id="2e225-277">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="2e225-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2e225-278">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="2e225-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="2e225-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2e225-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="2e225-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2e225-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="2e225-281">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="2e225-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="2e225-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2e225-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="2e225-283">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="2e225-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="2e225-284">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2e225-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2e225-285">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2e225-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2e225-286">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2e225-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2e225-287">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2e225-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-288">Az.Websites</span></span>
* <span data-ttu-id="2e225-289">Исправлена проблема, из-за которой теги веб-приложений удалялись при переносе приложения на новый план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="2e225-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="2e225-290">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="2e225-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="2e225-291">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="2e225-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="2e225-292">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="2e225-293">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2e225-293">General</span></span>
* <span data-ttu-id="2e225-294">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="2e225-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2e225-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-295">Az.Accounts</span></span>
* <span data-ttu-id="2e225-296">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="2e225-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2e225-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2e225-297">Az.Aks</span></span>
* <span data-ttu-id="2e225-298">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="2e225-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="2e225-299">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="2e225-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2e225-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e225-300">Az.ApiManagement</span></span>
* <span data-ttu-id="2e225-301">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="2e225-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="2e225-302">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="2e225-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="2e225-303">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="2e225-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="2e225-304">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="2e225-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="2e225-305">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="2e225-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2e225-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2e225-306">Az.Batch</span></span>
* <span data-ttu-id="2e225-307">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="2e225-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2e225-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2e225-308">Az.Cdn</span></span>
* <span data-ttu-id="2e225-309">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="2e225-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-310">Az.Compute</span></span>
* <span data-ttu-id="2e225-311">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="2e225-312">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2e225-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="2e225-313">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2e225-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="2e225-314">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="2e225-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="2e225-315">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2e225-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="2e225-316">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2e225-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="2e225-317">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="2e225-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="2e225-318">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="2e225-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-319">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-320">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="2e225-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="2e225-321">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="2e225-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="2e225-322">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="2e225-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="2e225-323">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="2e225-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-325">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="2e225-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2e225-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2e225-326">Az.EventHub</span></span>
* <span data-ttu-id="2e225-327">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="2e225-328">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="2e225-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="2e225-329">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="2e225-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="2e225-330">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="2e225-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="2e225-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2e225-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2e225-332">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="2e225-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2e225-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-333">Az.Monitor</span></span>
* <span data-ttu-id="2e225-334">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="2e225-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-335">Az.Network</span></span>
* <span data-ttu-id="2e225-336">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="2e225-337">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="2e225-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="2e225-338">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="2e225-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="2e225-339">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2e225-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="2e225-340">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="2e225-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="2e225-341">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="2e225-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="2e225-342">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="2e225-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2e225-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="2e225-344">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="2e225-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="2e225-345">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="2e225-345">Added example</span></span>
    - <span data-ttu-id="2e225-346">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="2e225-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="2e225-347">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2e225-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="2e225-348">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="2e225-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-350">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-351">Az.Resources</span></span>
* <span data-ttu-id="2e225-352">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="2e225-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="2e225-353">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="2e225-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="2e225-354">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="2e225-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="2e225-355">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="2e225-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2e225-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2e225-356">Az.ServiceBus</span></span>
* <span data-ttu-id="2e225-357">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="2e225-358">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="2e225-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="2e225-359">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="2e225-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="2e225-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="2e225-361">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="2e225-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="2e225-362">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2e225-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="2e225-363">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="2e225-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="2e225-364">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="2e225-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="2e225-365">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="2e225-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="2e225-366">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="2e225-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-367">Az.Sql</span></span>
* <span data-ttu-id="2e225-368">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="2e225-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-369">Az.Storage</span></span>
* <span data-ttu-id="2e225-370">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="2e225-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="2e225-371">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="2e225-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="2e225-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2e225-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="2e225-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2e225-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="2e225-374">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="2e225-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="2e225-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2e225-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-376">Az.Websites</span></span>
* <span data-ttu-id="2e225-377">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="2e225-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="2e225-378">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-379">Az.Accounts</span></span>
* <span data-ttu-id="2e225-380">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="2e225-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2e225-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2e225-382">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="2e225-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="2e225-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-383">Az.Automation</span></span>
* <span data-ttu-id="2e225-384">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e225-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="2e225-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2e225-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="2e225-386">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-387">Az.Compute</span></span>
* <span data-ttu-id="2e225-388">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2e225-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2e225-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2e225-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2e225-390">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="2e225-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="2e225-391">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="2e225-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-392">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-393">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="2e225-394">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="2e225-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2e225-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2e225-395">Az.EventHub</span></span>
* <span data-ttu-id="2e225-396">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="2e225-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2e225-397">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="2e225-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2e225-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2e225-398">Az.KeyVault</span></span>
* <span data-ttu-id="2e225-399">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2e225-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2e225-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2e225-400">Az.LogicApp</span></span>
* <span data-ttu-id="2e225-401">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="2e225-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="2e225-402">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="2e225-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2e225-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2e225-403">Az.ManagedServices</span></span>
* <span data-ttu-id="2e225-404">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="2e225-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-405">Az.Network</span></span>
* <span data-ttu-id="2e225-406">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="2e225-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="2e225-407">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-407">New cmdlets</span></span>
        - <span data-ttu-id="2e225-408">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2e225-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2e225-409">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2e225-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2e225-410">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2e225-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2e225-411">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2e225-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2e225-412">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2e225-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2e225-413">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2e225-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2e225-414">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="2e225-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="2e225-415">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2e225-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="2e225-416">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2e225-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="2e225-417">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="2e225-418">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="2e225-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="2e225-419">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="2e225-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="2e225-420">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="2e225-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="2e225-421">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="2e225-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="2e225-422">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-422">Updated cmdlets</span></span>
        - <span data-ttu-id="2e225-423">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2e225-424">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2e225-425">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2e225-426">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="2e225-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2e225-427">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="2e225-428">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2e225-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="2e225-429">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2e225-430">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2e225-431">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2e225-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="2e225-432">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="2e225-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="2e225-433">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="2e225-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="2e225-434">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="2e225-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2e225-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="2e225-436">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="2e225-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="2e225-437">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="2e225-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-439">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2e225-440">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="2e225-441">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="2e225-442">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2e225-443">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="2e225-444">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2e225-445">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="2e225-446">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2e225-447">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="2e225-448">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="2e225-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-449">Az.Resources</span></span>
- <span data-ttu-id="2e225-450">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2e225-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="2e225-451">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2e225-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2e225-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2e225-452">Az.ServiceBus</span></span>
* <span data-ttu-id="2e225-453">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="2e225-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2e225-454">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="2e225-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-455">Az.Sql</span></span>
* <span data-ttu-id="2e225-456">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="2e225-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="2e225-457">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2e225-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="2e225-458">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="2e225-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-459">Az.Storage</span></span>
* <span data-ttu-id="2e225-460">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="2e225-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2e225-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2e225-461">Az.StorageSync</span></span>
* <span data-ttu-id="2e225-462">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="2e225-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="2e225-463">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="2e225-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-464">Az.Websites</span></span>
* <span data-ttu-id="2e225-465">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="2e225-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="2e225-466">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="2e225-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="2e225-467">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="2e225-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="2e225-468">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-469">Az.Accounts</span></span>
* <span data-ttu-id="2e225-470">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="2e225-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2e225-471">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="2e225-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2e225-472">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2e225-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2e225-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2e225-473">Az.Advisor</span></span>
* <span data-ttu-id="2e225-474">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="2e225-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2e225-475">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="2e225-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2e225-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e225-476">Az.ApiManagement</span></span>
* <span data-ttu-id="2e225-477">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="2e225-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2e225-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2e225-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2e225-479">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="2e225-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2e225-480">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="2e225-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2e225-481">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="2e225-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2e225-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2e225-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2e225-483">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2e225-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-484">Az.Automation</span></span>
* <span data-ttu-id="2e225-485">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="2e225-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-486">Az.Compute</span></span>
* <span data-ttu-id="2e225-487">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="2e225-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-488">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-489">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="2e225-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2e225-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2e225-490">Az.EventGrid</span></span>
* <span data-ttu-id="2e225-491">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2e225-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2e225-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2e225-492">Az.IotHub</span></span>
* <span data-ttu-id="2e225-493">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="2e225-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-494">Az.Network</span></span>
* <span data-ttu-id="2e225-495">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="2e225-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2e225-496">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="2e225-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2e225-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="2e225-498">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2e225-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2e225-499">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="2e225-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2e225-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="2e225-501">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="2e225-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-503">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="2e225-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-504">Az.Resources</span></span>
    - <span data-ttu-id="2e225-505">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="2e225-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2e225-506">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="2e225-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2e225-507">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="2e225-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2e225-508">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="2e225-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2e225-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2e225-509">Az.ServiceBus</span></span>
* <span data-ttu-id="2e225-510">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="2e225-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-511">Az.Sql</span></span>
* <span data-ttu-id="2e225-512">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2e225-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2e225-513">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="2e225-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2e225-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2e225-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2e225-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2e225-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2e225-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2e225-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2e225-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2e225-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2e225-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2e225-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2e225-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2e225-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2e225-520">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2e225-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-521">Az.Storage</span></span>
* <span data-ttu-id="2e225-522">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="2e225-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2e225-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2e225-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2e225-524">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="2e225-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2e225-525">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2e225-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2e225-526">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="2e225-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2e225-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2e225-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2e225-529">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="2e225-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2e225-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2e225-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2e225-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2e225-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2e225-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2e225-532">Az.StorageSync</span></span>
* <span data-ttu-id="2e225-533">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="2e225-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2e225-534">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-535">Az.Accounts</span></span>
* <span data-ttu-id="2e225-536">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="2e225-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2e225-537">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="2e225-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2e225-538">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="2e225-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2e225-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2e225-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2e225-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="2e225-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-541">Az.Compute</span></span>
* <span data-ttu-id="2e225-542">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2e225-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2e225-543">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2e225-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2e225-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2e225-544">Az.Dns</span></span>
* <span data-ttu-id="2e225-545">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="2e225-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2e225-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2e225-546">Az.EventGrid</span></span>
* <span data-ttu-id="2e225-547">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2e225-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2e225-548">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2e225-548">New cmdlets:</span></span>
    - <span data-ttu-id="2e225-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2e225-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2e225-550">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2e225-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2e225-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2e225-552">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2e225-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2e225-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2e225-554">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2e225-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2e225-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2e225-556">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2e225-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2e225-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2e225-558">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="2e225-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2e225-559">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2e225-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2e225-560">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2e225-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2e225-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2e225-562">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="2e225-563">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2e225-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2e225-564">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2e225-565">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="2e225-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="2e225-566">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2e225-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2e225-567">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2e225-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2e225-568">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2e225-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2e225-569">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="2e225-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2e225-570">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="2e225-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2e225-571">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="2e225-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2e225-572">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="2e225-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2e225-573">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="2e225-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2e225-574">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="2e225-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="2e225-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2e225-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2e225-576">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="2e225-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2e225-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2e225-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2e225-578">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2e225-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2e225-579">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2e225-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2e225-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2e225-580">Az.FrontDoor</span></span>
* <span data-ttu-id="2e225-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2e225-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2e225-582">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="2e225-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2e225-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2e225-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2e225-584">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="2e225-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-585">Az.Network</span></span>
* <span data-ttu-id="2e225-586">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2e225-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2e225-587">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-587">New cmdlets</span></span>
        - <span data-ttu-id="2e225-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2e225-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2e225-589">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="2e225-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2e225-590">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-590">New cmdlets</span></span> 
        - <span data-ttu-id="2e225-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2e225-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2e225-592">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2e225-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2e225-593">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-593">New cmdlets</span></span> 
        - <span data-ttu-id="2e225-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2e225-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="2e225-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2e225-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2e225-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2e225-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2e225-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2e225-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2e225-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e225-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2e225-599">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2e225-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2e225-600">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-600">New cmdlets</span></span>
        - <span data-ttu-id="2e225-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e225-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2e225-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e225-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2e225-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e225-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2e225-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2e225-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2e225-605">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="2e225-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2e225-606">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="2e225-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2e225-607">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="2e225-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2e225-608">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="2e225-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2e225-609">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="2e225-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2e225-610">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="2e225-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2e225-611">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2e225-612">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="2e225-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2e225-613">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2e225-614">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="2e225-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2e225-615">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2e225-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2e225-616">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="2e225-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2e225-617">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="2e225-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2e225-618">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2e225-619">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2e225-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2e225-620">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2e225-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2e225-621">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2e225-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2e225-622">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="2e225-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2e225-623">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="2e225-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="2e225-624">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2e225-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="2e225-625">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="2e225-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2e225-626">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="2e225-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2e225-627">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="2e225-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2e225-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="2e225-629">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2e225-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-630">Az.Resources</span></span>
* <span data-ttu-id="2e225-631">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="2e225-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2e225-632">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="2e225-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2e225-633">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="2e225-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2e225-634">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e225-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2e225-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="2e225-636">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2e225-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-637">Az.Sql</span></span>
* <span data-ttu-id="2e225-638">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="2e225-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2e225-639">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="2e225-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2e225-640">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="2e225-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2e225-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e225-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2e225-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e225-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2e225-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e225-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2e225-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2e225-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2e225-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2e225-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-646">Az.Storage</span></span>
* <span data-ttu-id="2e225-647">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2e225-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2e225-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="2e225-649">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="2e225-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2e225-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2e225-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-651">Az.Websites</span></span>
* <span data-ttu-id="2e225-652">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="2e225-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2e225-653">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="2e225-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2e225-654">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2e225-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2e225-655">Az.Cdn</span></span>
* <span data-ttu-id="2e225-656">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="2e225-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-657">Az.Compute</span></span>
* <span data-ttu-id="2e225-658">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="2e225-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2e225-659">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2e225-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2e225-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2e225-660">Az.EventHub</span></span>
* <span data-ttu-id="2e225-661">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="2e225-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2e225-662">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2e225-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-663">Az.Network</span></span>
* <span data-ttu-id="2e225-664">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="2e225-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2e225-665">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="2e225-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2e225-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="2e225-667">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="2e225-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-669">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="2e225-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2e225-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2e225-670">Az.ServiceBus</span></span>
* <span data-ttu-id="2e225-671">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2e225-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2e225-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="2e225-673">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="2e225-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2e225-674">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2e225-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-675">Az.Sql</span></span>
* <span data-ttu-id="2e225-676">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2e225-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2e225-677">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="2e225-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2e225-678">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="2e225-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2e225-679">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="2e225-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-680">Az.Websites</span></span>
* <span data-ttu-id="2e225-681">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="2e225-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2e225-682">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2e225-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e225-683">Az.ApiManagement</span></span>
* <span data-ttu-id="2e225-684">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="2e225-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2e225-685">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="2e225-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2e225-686">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="2e225-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2e225-687">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="2e225-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2e225-688">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="2e225-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2e225-689">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="2e225-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2e225-690">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="2e225-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2e225-691">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="2e225-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2e225-692">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2e225-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2e225-693">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="2e225-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2e225-694">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2e225-695">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="2e225-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2e225-696">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="2e225-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2e225-697">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="2e225-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2e225-698">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="2e225-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2e225-699">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="2e225-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2e225-700">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="2e225-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2e225-701">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="2e225-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2e225-702">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="2e225-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="2e225-703">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="2e225-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2e225-704">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="2e225-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2e225-705">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="2e225-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2e225-706">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="2e225-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2e225-707">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2e225-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="2e225-708">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="2e225-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2e225-709">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="2e225-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2e225-710">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="2e225-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2e225-711">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2e225-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2e225-712">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2e225-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2e225-713">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="2e225-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2e225-714">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2e225-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="2e225-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2e225-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2e225-716">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2e225-717">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="2e225-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2e225-718">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2e225-719">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="2e225-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2e225-720">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="2e225-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2e225-721">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="2e225-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2e225-722">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="2e225-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2e225-723">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="2e225-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="2e225-724">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="2e225-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2e225-725">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2e225-726">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="2e225-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2e225-727">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="2e225-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2e225-728">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="2e225-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2e225-729">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="2e225-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2e225-730">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="2e225-731">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="2e225-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2e225-732">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="2e225-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2e225-733">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="2e225-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2e225-734">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="2e225-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2e225-735">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="2e225-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2e225-736">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="2e225-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2e225-737">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="2e225-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2e225-738">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="2e225-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2e225-739">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="2e225-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2e225-740">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="2e225-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2e225-741">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="2e225-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2e225-742">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="2e225-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2e225-743">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="2e225-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2e225-744">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="2e225-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2e225-745">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="2e225-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2e225-746">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="2e225-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2e225-747">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="2e225-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2e225-748">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="2e225-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2e225-749">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2e225-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2e225-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2e225-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2e225-751">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="2e225-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2e225-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2e225-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2e225-753">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2e225-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2e225-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2e225-755">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="2e225-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2e225-756">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="2e225-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2e225-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2e225-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2e225-758">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="2e225-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="2e225-759">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2e225-760">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="2e225-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-761">Az.Automation</span></span>
* <span data-ttu-id="2e225-762">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="2e225-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2e225-763">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="2e225-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2e225-764">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="2e225-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2e225-765">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="2e225-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2e225-766">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="2e225-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2e225-767">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="2e225-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2e225-768">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="2e225-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-769">Az.Compute</span></span>
* <span data-ttu-id="2e225-770">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2e225-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2e225-771">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2e225-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-773">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="2e225-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2e225-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-774">Az.Monitor</span></span>
* <span data-ttu-id="2e225-775">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="2e225-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-776">Az.Network</span></span>
* <span data-ttu-id="2e225-777">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2e225-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2e225-778">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2e225-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="2e225-779">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="2e225-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2e225-780">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="2e225-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-781">Az.Resources</span></span>
* <span data-ttu-id="2e225-782">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="2e225-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-783">Az.Sql</span></span>
* <span data-ttu-id="2e225-784">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2e225-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2e225-785">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-786">Az.Accounts</span></span>
* <span data-ttu-id="2e225-787">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="2e225-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2e225-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2e225-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="2e225-789">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="2e225-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2e225-790">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2e225-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-791">Az.Compute</span></span>
* <span data-ttu-id="2e225-792">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="2e225-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2e225-793">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2e225-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2e225-794">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2e225-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2e225-795">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2e225-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2e225-796">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2e225-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2e225-797">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2e225-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="2e225-798">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="2e225-798">Breaking changes</span></span>
    - <span data-ttu-id="2e225-799">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2e225-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2e225-800">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="2e225-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2e225-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2e225-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="2e225-802">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="2e225-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2e225-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2e225-803">Az.Dns</span></span>
* <span data-ttu-id="2e225-804">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="2e225-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2e225-805">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="2e225-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2e225-806">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="2e225-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2e225-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2e225-807">Az.FrontDoor</span></span>
* <span data-ttu-id="2e225-808">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="2e225-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2e225-809">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="2e225-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2e225-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2e225-810">Az.HDInsight</span></span>
* <span data-ttu-id="2e225-811">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="2e225-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2e225-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2e225-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2e225-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2e225-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2e225-814">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="2e225-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2e225-815">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="2e225-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2e225-816">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="2e225-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2e225-817">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="2e225-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2e225-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-818">Az.Monitor</span></span>
* <span data-ttu-id="2e225-819">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="2e225-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="2e225-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2e225-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2e225-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2e225-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2e225-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2e225-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2e225-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2e225-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2e225-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2e225-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2e225-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2e225-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2e225-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2e225-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2e225-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2e225-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2e225-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2e225-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2e225-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2e225-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2e225-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2e225-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2e225-831">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="2e225-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2e225-832">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="2e225-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-833">Az.Network</span></span>
* <span data-ttu-id="2e225-834">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="2e225-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2e225-835">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-835">New cmdlets</span></span>
        - <span data-ttu-id="2e225-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2e225-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="2e225-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2e225-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2e225-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2e225-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2e225-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2e225-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2e225-840">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="2e225-840">Updated cmdlets</span></span>
        - <span data-ttu-id="2e225-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2e225-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2e225-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2e225-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2e225-843">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="2e225-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2e225-844">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="2e225-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2e225-845">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="2e225-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2e225-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="2e225-847">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="2e225-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2e225-848">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2e225-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2e225-849">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="2e225-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-851">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2e225-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2e225-852">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2e225-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2e225-853">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2e225-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2e225-854">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="2e225-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2e225-855">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="2e225-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2e225-856">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="2e225-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2e225-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2e225-857">Az.Relay</span></span>
* <span data-ttu-id="2e225-858">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="2e225-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2e225-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2e225-859">Az.ServiceBus</span></span>
* <span data-ttu-id="2e225-860">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2e225-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-861">Az.Storage</span></span>
* <span data-ttu-id="2e225-862">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="2e225-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2e225-863">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="2e225-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2e225-864">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2e225-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2e225-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="2e225-866">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="2e225-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2e225-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2e225-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2e225-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-870">Az.Websites</span></span>
* <span data-ttu-id="2e225-871">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="2e225-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2e225-872">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="2e225-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2e225-873">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2e225-874">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2e225-874">Highlights since the last major release</span></span>
* <span data-ttu-id="2e225-875">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="2e225-875">General availability of `Az` module</span></span>
* <span data-ttu-id="2e225-876">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2e225-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2e225-877">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2e225-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2e225-878">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="2e225-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2e225-879">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2e225-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2e225-880">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="2e225-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2e225-881">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="2e225-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2e225-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-882">Az.Accounts</span></span>
* <span data-ttu-id="2e225-883">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="2e225-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2e225-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2e225-884">Az.Batch</span></span>
* <span data-ttu-id="2e225-885">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2e225-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2e225-886">Az.Cdn</span></span>
* <span data-ttu-id="2e225-887">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2e225-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2e225-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="2e225-889">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-890">Az.Compute</span></span>
* <span data-ttu-id="2e225-891">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="2e225-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2e225-892">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2e225-893">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2e225-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-894">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-895">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2e225-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-897">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2e225-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2e225-898">Az.EventGrid</span></span>
* <span data-ttu-id="2e225-899">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="2e225-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2e225-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2e225-900">Az.EventHub</span></span>
* <span data-ttu-id="2e225-901">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2e225-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="2e225-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2e225-902">Az.HDInsight</span></span>
* <span data-ttu-id="2e225-903">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2e225-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2e225-904">Az.IotHub</span></span>
* <span data-ttu-id="2e225-905">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2e225-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2e225-906">Az.KeyVault</span></span>
* <span data-ttu-id="2e225-907">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2e225-908">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2e225-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2e225-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2e225-909">Az.MachineLearning</span></span>
* <span data-ttu-id="2e225-910">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2e225-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2e225-911">Az.Media</span></span>
* <span data-ttu-id="2e225-912">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2e225-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-913">Az.Monitor</span></span>
  * <span data-ttu-id="2e225-914">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="2e225-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2e225-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2e225-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2e225-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2e225-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2e225-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2e225-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2e225-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2e225-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2e225-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2e225-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2e225-920">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-921">Az.Network</span></span>
* <span data-ttu-id="2e225-922">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2e225-923">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2e225-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2e225-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2e225-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="2e225-925">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2e225-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="2e225-927">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2e225-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2e225-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2e225-929">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-931">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2e225-932">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2e225-933">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2e225-934">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="2e225-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2e225-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2e225-935">Az.RedisCache</span></span>
* <span data-ttu-id="2e225-936">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-937">Az.Resources</span></span>
* <span data-ttu-id="2e225-938">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2e225-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-939">Az.Sql</span></span>
* <span data-ttu-id="2e225-940">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="2e225-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2e225-941">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2e225-942">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="2e225-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2e225-943">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="2e225-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2e225-944">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="2e225-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2e225-945">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2e225-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2e225-946">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2e225-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-947">Az.Websites</span></span>
* <span data-ttu-id="2e225-948">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="2e225-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2e225-949">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2e225-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2e225-950">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="2e225-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2e225-951">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2e225-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2e225-952">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2e225-953">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2e225-953">Highlights since the last major release</span></span>
* <span data-ttu-id="2e225-954">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="2e225-954">General availability of `Az` module</span></span>
* <span data-ttu-id="2e225-955">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2e225-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2e225-956">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2e225-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2e225-957">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="2e225-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2e225-958">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2e225-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2e225-959">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="2e225-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2e225-960">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="2e225-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2e225-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-961">Az.Accounts</span></span>
* <span data-ttu-id="2e225-962">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="2e225-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2e225-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2e225-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="2e225-964">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2e225-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2e225-965">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="2e225-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-966">Az.Automation</span></span>
* <span data-ttu-id="2e225-967">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="2e225-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2e225-968">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="2e225-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2e225-969">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-970">Az.Compute</span></span>
* <span data-ttu-id="2e225-971">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="2e225-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2e225-972">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="2e225-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="2e225-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2e225-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="2e225-974">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="2e225-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-975">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-976">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="2e225-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2e225-977">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-978">Az.Resources</span></span>
* <span data-ttu-id="2e225-979">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="2e225-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2e225-980">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2e225-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2e225-981">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="2e225-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2e225-982">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="2e225-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2e225-983">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="2e225-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2e225-984">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="2e225-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-985">Az.Sql</span></span>
* <span data-ttu-id="2e225-986">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="2e225-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-987">Az.Storage</span></span>
* <span data-ttu-id="2e225-988">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2e225-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e225-989">New-AzStorageContext</span></span>
* <span data-ttu-id="2e225-990">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="2e225-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2e225-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2e225-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2e225-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2e225-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2e225-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e225-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2e225-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e225-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2e225-995">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="2e225-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2e225-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2e225-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2e225-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2e225-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2e225-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2e225-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2e225-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2e225-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2e225-1000">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2e225-1001">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2e225-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="2e225-1002">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="2e225-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="2e225-1003">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2e225-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2e225-1004">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2e225-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2e225-1005">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="2e225-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2e225-1006">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2e225-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2e225-1007">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="2e225-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2e225-1008">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="2e225-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-1009">Az.Automation</span></span>
* <span data-ttu-id="2e225-1010">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="2e225-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2e225-1011">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="2e225-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="2e225-1012">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="2e225-1012">Pre-Post script</span></span>
    * <span data-ttu-id="2e225-1013">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1014">Az.Compute</span></span>
* <span data-ttu-id="2e225-1015">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="2e225-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2e225-1016">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2e225-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2e225-1017">Az.KeyVault</span></span>
* <span data-ttu-id="2e225-1018">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2e225-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1019">Az.Network</span></span>
* <span data-ttu-id="2e225-1020">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2e225-1021">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2e225-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-1023">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="2e225-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2e225-1024">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="2e225-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1025">Az.Resources</span></span>
* <span data-ttu-id="2e225-1026">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2e225-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2e225-1027">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="2e225-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1028">Az.Sql</span></span>
* <span data-ttu-id="2e225-1029">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="2e225-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-1030">Az.Storage</span></span>
* <span data-ttu-id="2e225-1031">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2e225-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2e225-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2e225-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2e225-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2e225-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2e225-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2e225-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2e225-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2e225-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2e225-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2e225-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2e225-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2e225-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-1038">Az.Websites</span></span>
* <span data-ttu-id="2e225-1039">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="2e225-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="2e225-1040">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-1041">Az.Accounts</span></span>
* <span data-ttu-id="2e225-1042">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="2e225-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2e225-1043">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="2e225-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-1044">Az.Automation</span></span>
* <span data-ttu-id="2e225-1045">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2e225-1046">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2e225-1047">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="2e225-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2e225-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2e225-1048">Az.Cdn</span></span>
* <span data-ttu-id="2e225-1049">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="2e225-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1050">Az.Compute</span></span>
* <span data-ttu-id="2e225-1051">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="2e225-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-1052">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-1053">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="2e225-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2e225-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2e225-1054">Az.LogicApp</span></span>
* <span data-ttu-id="2e225-1055">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="2e225-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1056">Az.Network</span></span>
* <span data-ttu-id="2e225-1057">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="2e225-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-1059">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2e225-1060">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="2e225-1060">SDK Update</span></span>
* <span data-ttu-id="2e225-1061">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="2e225-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2e225-1062">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="2e225-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1063">Az.Resources</span></span>
* <span data-ttu-id="2e225-1064">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="2e225-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2e225-1065">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="2e225-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2e225-1066">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="2e225-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2e225-1067">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="2e225-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2e225-1068">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="2e225-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2e225-1069">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="2e225-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1070">Az.Sql</span></span>
* <span data-ttu-id="2e225-1071">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="2e225-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2e225-1072">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="2e225-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-1073">Az.Storage</span></span>
* <span data-ttu-id="2e225-1074">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2e225-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2e225-1075">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2e225-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="2e225-1077">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="2e225-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-1078">Az.Automation</span></span>
* <span data-ttu-id="2e225-1079">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2e225-1080">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2e225-1081">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2e225-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="2e225-1083">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e225-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1084">Az.Compute</span></span>
* <span data-ttu-id="2e225-1085">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="2e225-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2e225-1086">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="2e225-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2e225-1087">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2e225-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2e225-1088">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2e225-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-1090">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="2e225-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2e225-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2e225-1091">Az.EventHub</span></span>
* <span data-ttu-id="2e225-1092">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="2e225-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="2e225-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2e225-1093">Az.KeyVault</span></span>
* <span data-ttu-id="2e225-1094">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="2e225-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2e225-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2e225-1095">Az.LogicApp</span></span>
* <span data-ttu-id="2e225-1096">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="2e225-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2e225-1097">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2e225-1098">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="2e225-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2e225-1099">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="2e225-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2e225-1100">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="2e225-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2e225-1101">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="2e225-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2e225-1102">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="2e225-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2e225-1103">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="2e225-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2e225-1104">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2e225-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2e225-1105">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2e225-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2e225-1106">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2e225-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2e225-1107">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e225-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2e225-1108">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2e225-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-1109">Az.Monitor</span></span>
* <span data-ttu-id="2e225-1110">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="2e225-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1111">Az.Network</span></span>
* <span data-ttu-id="2e225-1112">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="2e225-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2e225-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="2e225-1114">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2e225-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2e225-1115">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2e225-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="2e225-1116">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="2e225-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="2e225-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1117">Az.Resources</span></span>
* <span data-ttu-id="2e225-1118">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="2e225-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2e225-1119">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="2e225-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2e225-1120">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="2e225-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2e225-1121">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="2e225-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1122">Az.Sql</span></span>
* <span data-ttu-id="2e225-1123">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2e225-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2e225-1124">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="2e225-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-1125">Az.Websites</span></span>
* <span data-ttu-id="2e225-1126">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="2e225-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2e225-1127">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-1128">Az.Accounts</span></span>
* <span data-ttu-id="2e225-1129">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2e225-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2e225-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="2e225-1131">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="2e225-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1132">Az.Compute</span></span>
* <span data-ttu-id="2e225-1133">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="2e225-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2e225-1134">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="2e225-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2e225-1135">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="2e225-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="2e225-1137">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="2e225-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1138">Az.Resources</span></span>
* <span data-ttu-id="2e225-1139">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="2e225-1140">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="2e225-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2e225-1141">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="2e225-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="2e225-1142">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="2e225-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1143">Az.Sql</span></span>
* <span data-ttu-id="2e225-1144">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="2e225-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2e225-1145">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2e225-1146">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="2e225-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2e225-1147">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-1148">Az.Accounts</span></span>
* <span data-ttu-id="2e225-1149">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="2e225-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2e225-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="2e225-1151">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="2e225-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="2e225-1153">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="2e225-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2e225-1154">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-1155">Az.Accounts</span></span>
* <span data-ttu-id="2e225-1156">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2e225-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2e225-1157">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2e225-1158">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="2e225-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2e225-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2e225-1159">Az.Aks</span></span>
* <span data-ttu-id="2e225-1160">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2e225-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-1161">Az.Automation</span></span>
* <span data-ttu-id="2e225-1162">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="2e225-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2e225-1163">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2e225-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2e225-1164">Az.Cdn</span></span>
* <span data-ttu-id="2e225-1165">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1166">Az.Compute</span></span>
* <span data-ttu-id="2e225-1167">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="2e225-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2e225-1168">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2e225-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2e225-1169">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2e225-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2e225-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2e225-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2e225-1171">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2e225-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e225-1172">Az.DataFactory</span></span>
* <span data-ttu-id="2e225-1173">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-1175">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="2e225-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2e225-1176">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="2e225-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2e225-1177">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2e225-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2e225-1178">Az.IotHub</span></span>
* <span data-ttu-id="2e225-1179">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2e225-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2e225-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2e225-1180">Az.KeyVault</span></span>
* <span data-ttu-id="2e225-1181">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1182">Az.Network</span></span>
* <span data-ttu-id="2e225-1183">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1184">Az.Resources</span></span>
* <span data-ttu-id="2e225-1185">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="2e225-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2e225-1186">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2e225-1187">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2e225-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2e225-1188">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="2e225-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2e225-1189">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="2e225-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2e225-1190">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2e225-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2e225-1191">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="2e225-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2e225-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="2e225-1193">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="2e225-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2e225-1194">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2e225-1194">Fix some error messages.</span></span>
* <span data-ttu-id="2e225-1195">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="2e225-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2e225-1196">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="2e225-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2e225-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2e225-1197">Az.SignalR</span></span>
* <span data-ttu-id="2e225-1198">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1199">Az.Sql</span></span>
* <span data-ttu-id="2e225-1200">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2e225-1201">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="2e225-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2e225-1202">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="2e225-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2e225-1203">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="2e225-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-1204">Az.Storage</span></span>
* <span data-ttu-id="2e225-1205">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2e225-1206">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="2e225-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2e225-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2e225-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2e225-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2e225-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2e225-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2e225-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="2e225-1210">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-1211">Az.Websites</span></span>
* <span data-ttu-id="2e225-1212">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2e225-1213">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="2e225-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2e225-1214">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="2e225-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2e225-1215">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2e225-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-1216">Az.Accounts</span></span>
* <span data-ttu-id="2e225-1217">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="2e225-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1218">Az.Compute</span></span>
* <span data-ttu-id="2e225-1219">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="2e225-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2e225-1220">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="2e225-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2e225-1221">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2e225-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-1223">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="2e225-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2e225-1224">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2e225-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2e225-1225">Az.EventGrid</span></span>
* <span data-ttu-id="2e225-1226">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2e225-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2e225-1227">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2e225-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2e225-1228">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="2e225-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2e225-1229">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="2e225-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2e225-1230">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="2e225-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2e225-1231">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e225-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2e225-1232">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="2e225-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2e225-1233">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="2e225-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2e225-1234">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="2e225-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2e225-1235">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e225-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="2e225-1236">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2e225-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2e225-1237">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="2e225-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2e225-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2e225-1238">Az.IotHub</span></span>
* <span data-ttu-id="2e225-1239">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="2e225-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2e225-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2e225-1240">Az.LogicApp</span></span>
* <span data-ttu-id="2e225-1241">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="2e225-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1242">Az.Resources</span></span>
* <span data-ttu-id="2e225-1243">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="2e225-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2e225-1244">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="2e225-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2e225-1245">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2e225-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2e225-1246">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="2e225-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2e225-1247">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="2e225-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2e225-1248">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="2e225-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2e225-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2e225-1249">Az.SignalR</span></span>
* <span data-ttu-id="2e225-1250">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2e225-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1251">Az.Sql</span></span>
* <span data-ttu-id="2e225-1252">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="2e225-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2e225-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-1253">Az.Storage</span></span>
* <span data-ttu-id="2e225-1254">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="2e225-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2e225-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e225-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="2e225-1256">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2e225-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2e225-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2e225-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-1258">Az.Websites</span></span>
* <span data-ttu-id="2e225-1259">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="2e225-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2e225-1260">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2e225-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2e225-1261">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2e225-1262">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2e225-1262">General</span></span>

- <span data-ttu-id="2e225-1263">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="2e225-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="2e225-1264">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="2e225-1264">Online help for each module</span></span>
- <span data-ttu-id="2e225-1265">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="2e225-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2e225-1266">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2e225-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e225-1267">Az.Accounts</span></span>
- <span data-ttu-id="2e225-1268">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="2e225-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="2e225-1269">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="2e225-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2e225-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e225-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="2e225-1271">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="2e225-1271">Fixes for #7002</span></span>
- <span data-ttu-id="2e225-1272">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2e225-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2e225-1273">Az.Batch</span></span>
- <span data-ttu-id="2e225-1274">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2e225-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2e225-1275">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="2e225-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2e225-1276">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2e225-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2e225-1277">Az.Billing</span></span>
- <span data-ttu-id="2e225-1278">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="2e225-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2e225-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="2e225-1280">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="2e225-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2e225-1281">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2e225-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2e225-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2e225-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="2e225-1283">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="2e225-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2e225-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2e225-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2e225-1285">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2e225-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="2e225-1287">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2e225-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2e225-1288">Az.Monitor</span></span>
- <span data-ttu-id="2e225-1289">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2e225-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2e225-1290">Az.KeyVault</span></span>
- <span data-ttu-id="2e225-1291">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="2e225-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2e225-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2e225-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="2e225-1293">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2e225-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2e225-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2e225-1294">Az.Media</span></span>
- <span data-ttu-id="2e225-1295">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2e225-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2e225-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1296">Az.Network</span></span>
<span data-ttu-id="2e225-1297">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="2e225-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2e225-1298">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2e225-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="2e225-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e225-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2e225-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e225-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2e225-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e225-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2e225-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e225-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2e225-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e225-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2e225-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2e225-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2e225-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2e225-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2e225-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e225-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2e225-1307">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e225-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2e225-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e225-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2e225-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2e225-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2e225-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2e225-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2e225-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2e225-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2e225-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2e225-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2e225-1313">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2e225-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2e225-1314">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2e225-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2e225-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2e225-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2e225-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2e225-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2e225-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2e225-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2e225-1318">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2e225-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2e225-1319">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2e225-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="2e225-1321">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2e225-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2e225-1322">Az.Profile</span></span>
- <span data-ttu-id="2e225-1323">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2e225-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="2e225-1325">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2e225-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1326">Az.Resources</span></span>
- <span data-ttu-id="2e225-1327">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2e225-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="2e225-1329">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="2e225-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2e225-1330">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2e225-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2e225-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="2e225-1332">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2e225-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2e225-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1333">Az.Sql</span></span>
- <span data-ttu-id="2e225-1334">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="2e225-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2e225-1335">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2e225-1336">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2e225-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-1337">Az.Storage</span></span>
- <span data-ttu-id="2e225-1338">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2e225-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-1339">Az.Websites</span></span>
- <span data-ttu-id="2e225-1340">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2e225-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2e225-1341">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2e225-1342">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2e225-1342">General</span></span>

* <span data-ttu-id="2e225-1343">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="2e225-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2e225-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1344">Az.Compute</span></span>

* <span data-ttu-id="2e225-1345">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="2e225-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2e225-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="2e225-1347">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="2e225-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2e225-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2e225-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="2e225-1349">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="2e225-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="2e225-1350">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2e225-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2e225-1351">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2e225-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2e225-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="2e225-1353">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2e225-1354">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="2e225-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2e225-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1355">Az.Resources</span></span>

* <span data-ttu-id="2e225-1356">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="2e225-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2e225-1357">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2e225-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1358">Az.Sql</span></span>

* <span data-ttu-id="2e225-1359">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="2e225-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2e225-1360">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="2e225-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2e225-1361">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="2e225-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2e225-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2e225-1362">Az.Storage</span></span>

* <span data-ttu-id="2e225-1363">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2e225-1364">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="2e225-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2e225-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2e225-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2e225-1366">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="2e225-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="2e225-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2e225-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2e225-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2e225-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2e225-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-1369">Az.Websites</span></span>

* <span data-ttu-id="2e225-1370">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e225-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="2e225-1371">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="2e225-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2e225-1372">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2e225-1373">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2e225-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e225-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="2e225-1375">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2e225-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2e225-1376">Az.Automation</span></span>
* <span data-ttu-id="2e225-1377">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="2e225-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2e225-1378">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="2e225-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2e225-1379">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="2e225-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2e225-1380">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="2e225-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2e225-1381">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="2e225-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2e225-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1382">Az.Compute</span></span>
* <span data-ttu-id="2e225-1383">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="2e225-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2e225-1384">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2e225-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2e225-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="2e225-1386">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2e225-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2e225-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2e225-1388">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2e225-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2e225-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1389">Az.Network</span></span>
* <span data-ttu-id="2e225-1390">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="2e225-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2e225-1391">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2e225-1392">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="2e225-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="2e225-1393">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2e225-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2e225-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2e225-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2e225-1395">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2e225-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2e225-1396">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="2e225-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2e225-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2e225-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2e225-1398">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="2e225-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2e225-1399">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2e225-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2e225-1400">Az.Relay</span></span>
* <span data-ttu-id="2e225-1401">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="2e225-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2e225-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1402">Az.Resources</span></span>
* <span data-ttu-id="2e225-1403">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="2e225-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2e225-1404">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="2e225-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2e225-1405">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="2e225-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2e225-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="2e225-1407">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="2e225-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2e225-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1408">Az.Sql</span></span>
* <span data-ttu-id="2e225-1409">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2e225-1410">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2e225-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2e225-1411">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2e225-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2e225-1412">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2e225-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2e225-1413">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2e225-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2e225-1414">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2e225-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2e225-1415">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2e225-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2e225-1416">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2e225-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2e225-1417">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2e225-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2e225-1418">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="2e225-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2e225-1419">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="2e225-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2e225-1420">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2e225-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2e225-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2e225-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2e225-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2e225-1423">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2e225-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2e225-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2e225-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2e225-1425">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="2e225-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2e225-1426">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2e225-1427">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2e225-1427">General</span></span>
* <span data-ttu-id="2e225-1428">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="2e225-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2e225-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2e225-1429">Az.Profile</span></span>
* <span data-ttu-id="2e225-1430">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="2e225-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2e225-1431">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="2e225-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2e225-1432">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2e225-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2e225-1433">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="2e225-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2e225-1434">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="2e225-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2e225-1435">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="2e225-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2e225-1436">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="2e225-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2e225-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="2e225-1438">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2e225-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1439">Az.Compute</span></span>
* <span data-ttu-id="2e225-1440">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2e225-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2e225-1441">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2e225-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2e225-1442">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2e225-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-1444">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2e225-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2e225-1445">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="2e225-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2e225-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2e225-1446">Az.Insights</span></span>
* <span data-ttu-id="2e225-1447">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="2e225-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2e225-1448">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="2e225-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2e225-1449">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="2e225-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2e225-1450">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="2e225-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1451">Az.Network</span></span>
* <span data-ttu-id="2e225-1452">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="2e225-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2e225-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2e225-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2e225-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2e225-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2e225-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2e225-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2e225-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2e225-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2e225-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2e225-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2e225-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2e225-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2e225-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2e225-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="2e225-1460">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="2e225-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1461">Az.Resources</span></span>
* <span data-ttu-id="2e225-1462">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="2e225-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2e225-1463">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2e225-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2e225-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2e225-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="2e225-1465">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="2e225-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2e225-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2e225-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="2e225-1467">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="2e225-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2e225-1468">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2e225-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2e225-1469">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2e225-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2e225-1470">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2e225-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2e225-1471">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2e225-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2e225-1472">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2e225-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2e225-1473">Az.Profile</span></span>
* <span data-ttu-id="2e225-1474">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="2e225-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2e225-1475">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="2e225-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1476">Az.Compute</span></span>
* <span data-ttu-id="2e225-1477">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="2e225-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2e225-1478">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2e225-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2e225-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2e225-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="2e225-1480">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="2e225-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2e225-1481">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2e225-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2e225-1482">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2e225-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2e225-1483">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2e225-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2e225-1484">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2e225-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1485">Az.Network</span></span>
* <span data-ttu-id="2e225-1486">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="2e225-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2e225-1487">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2e225-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1488">Az.Resources</span></span>
* <span data-ttu-id="2e225-1489">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="2e225-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2e225-1490">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="2e225-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2e225-1491">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2e225-1492">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="2e225-1492">Azure.Storage</span></span>
* <span data-ttu-id="2e225-1493">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="2e225-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2e225-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2e225-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2e225-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2e225-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2e225-1496">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="2e225-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2e225-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2e225-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="2e225-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2e225-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="2e225-1499">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2e225-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2e225-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2e225-1500">Az.Compute</span></span>
* <span data-ttu-id="2e225-1501">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="2e225-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2e225-1502">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2e225-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2e225-1503">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2e225-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2e225-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2e225-1505">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="2e225-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2e225-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2e225-1506">Az.Network</span></span>
* <span data-ttu-id="2e225-1507">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="2e225-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2e225-1508">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2e225-1508">new cmdlets added</span></span>
    - <span data-ttu-id="2e225-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e225-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2e225-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e225-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2e225-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e225-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2e225-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e225-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2e225-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2e225-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2e225-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2e225-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2e225-1515">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="2e225-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2e225-1516">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e225-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2e225-1517">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2e225-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2e225-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2e225-1518">Az.RedisCache</span></span>
* <span data-ttu-id="2e225-1519">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="2e225-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2e225-1520">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="2e225-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2e225-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2e225-1521">Az.Resources</span></span>
* <span data-ttu-id="2e225-1522">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2e225-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2e225-1523">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="2e225-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2e225-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2e225-1524">Az.Sql</span></span>
* <span data-ttu-id="2e225-1525">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="2e225-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2e225-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2e225-1526">Az.Websites</span></span>
* <span data-ttu-id="2e225-1527">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="2e225-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2e225-1528">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="2e225-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2e225-1529">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2e225-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2e225-1530">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="2e225-1530">Initial Release</span></span>
