---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 656e61e7f208367fc7fae28f73d1b6f289831d77
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427740"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="95e0a-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="95e0a-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="95e0a-104">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="95e0a-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="95e0a-105">General</span></span>
* <span data-ttu-id="95e0a-106">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="95e0a-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95e0a-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-107">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-108">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="95e0a-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="95e0a-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95e0a-109">Az.ApiManagement</span></span>
* <span data-ttu-id="95e0a-110">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="95e0a-111">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="95e0a-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-112">Az.Automation</span></span>
* <span data-ttu-id="95e0a-113">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="95e0a-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="95e0a-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95e0a-114">Az.Batch</span></span>
* <span data-ttu-id="95e0a-115">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-116">Az.Compute</span></span>
* <span data-ttu-id="95e0a-117">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="95e0a-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="95e0a-118">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="95e0a-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="95e0a-119">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="95e0a-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="95e0a-120">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="95e0a-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-121">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-122">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="95e0a-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="95e0a-123">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="95e0a-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="95e0a-124">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-126">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="95e0a-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="95e0a-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="95e0a-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="95e0a-128">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="95e0a-129">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="95e0a-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="95e0a-130">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="95e0a-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="95e0a-131">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="95e0a-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95e0a-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-132">Az.IotHub</span></span>
* <span data-ttu-id="95e0a-133">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="95e0a-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="95e0a-134">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95e0a-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-135">Az.Monitor</span></span>
* <span data-ttu-id="95e0a-136">Добавлены новые получатели групп действий для New-AzActionGroupReceiver: -ItsmReceiver, -VoiceReceiver,-ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="95e0a-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="95e0a-137">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="95e0a-138">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="95e0a-139">Веб-перехватчики теперь поддерживают аутентификацию на основе Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95e0a-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-140">Az.Network</span></span>
* <span data-ttu-id="95e0a-141">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="95e0a-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="95e0a-142">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="95e0a-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="95e0a-143">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="95e0a-143">New cmdlets added:</span></span>
        - <span data-ttu-id="95e0a-144">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="95e0a-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="95e0a-145">В следующие командлеты добавлен необязательный параметр -TrafficSelectorPolicies:</span><span class="sxs-lookup"><span data-stu-id="95e0a-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="95e0a-146">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="95e0a-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="95e0a-147">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="95e0a-148">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="95e0a-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="95e0a-149">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="95e0a-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="95e0a-150">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95e0a-151">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95e0a-152">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="95e0a-153">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="95e0a-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="95e0a-154">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="95e0a-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="95e0a-155">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="95e0a-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="95e0a-156">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="95e0a-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="95e0a-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="95e0a-157">Az.RedisCache</span></span>
* <span data-ttu-id="95e0a-158">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="95e0a-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-159">Az.Sql</span></span>
* <span data-ttu-id="95e0a-160">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="95e0a-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-161">Az.Storage</span></span>
* <span data-ttu-id="95e0a-162">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="95e0a-163">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="95e0a-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="95e0a-164">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95e0a-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="95e0a-165">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="95e0a-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="95e0a-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="95e0a-167">Az.StorageSync</span></span>
* <span data-ttu-id="95e0a-168">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="95e0a-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-169">Az.Websites</span></span>
* <span data-ttu-id="95e0a-170">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="95e0a-171">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="95e0a-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95e0a-172">Az.ApiManagement</span></span>
* <span data-ttu-id="95e0a-173">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="95e0a-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="95e0a-174">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="95e0a-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="95e0a-175">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="95e0a-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-176">Az.Automation</span></span>
* <span data-ttu-id="95e0a-177">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="95e0a-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="95e0a-178">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="95e0a-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="95e0a-179">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="95e0a-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-180">Az.Compute</span></span>
* <span data-ttu-id="95e0a-181">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="95e0a-182">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="95e0a-183">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="95e0a-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="95e0a-184">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="95e0a-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="95e0a-185">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="95e0a-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="95e0a-186">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="95e0a-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="95e0a-187">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="95e0a-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="95e0a-188">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="95e0a-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="95e0a-189">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-190">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-191">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="95e0a-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="95e0a-192">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="95e0a-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="95e0a-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95e0a-193">Az.HDInsight</span></span>
* <span data-ttu-id="95e0a-194">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95e0a-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-195">Az.IotHub</span></span>
* <span data-ttu-id="95e0a-196">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="95e0a-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="95e0a-197">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="95e0a-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="95e0a-198">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="95e0a-198">New cmdlets are:</span></span>
    - <span data-ttu-id="95e0a-199">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="95e0a-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="95e0a-200">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="95e0a-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="95e0a-201">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="95e0a-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="95e0a-202">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="95e0a-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95e0a-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-203">Az.Monitor</span></span>
* <span data-ttu-id="95e0a-204">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="95e0a-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="95e0a-205">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="95e0a-206">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="95e0a-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="95e0a-207">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="95e0a-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="95e0a-208">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="95e0a-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="95e0a-209">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="95e0a-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="95e0a-210">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="95e0a-211">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="95e0a-212">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="95e0a-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="95e0a-213">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="95e0a-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="95e0a-214">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="95e0a-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="95e0a-215">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="95e0a-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="95e0a-216">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="95e0a-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="95e0a-217">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="95e0a-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="95e0a-218">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="95e0a-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="95e0a-219">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="95e0a-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="95e0a-220">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="95e0a-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="95e0a-221">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="95e0a-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="95e0a-222">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="95e0a-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="95e0a-223">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="95e0a-223">Overall improved help files</span></span>
* <span data-ttu-id="95e0a-224">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="95e0a-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-225">Az.Network</span></span>
* <span data-ttu-id="95e0a-226">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="95e0a-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="95e0a-227">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="95e0a-228">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="95e0a-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="95e0a-229">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="95e0a-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="95e0a-230">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="95e0a-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="95e0a-231">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="95e0a-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="95e0a-232">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="95e0a-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="95e0a-233">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="95e0a-234">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="95e0a-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="95e0a-235">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="95e0a-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="95e0a-236">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="95e0a-237">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="95e0a-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="95e0a-238">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-238">New cmdlets</span></span>
        - <span data-ttu-id="95e0a-239">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="95e0a-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="95e0a-240">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="95e0a-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="95e0a-241">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="95e0a-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="95e0a-242">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="95e0a-242">New-VpnSite</span></span>
        - <span data-ttu-id="95e0a-243">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="95e0a-243">Update-VpnSite</span></span>
        - <span data-ttu-id="95e0a-244">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="95e0a-244">New-VpnConnection</span></span>
        - <span data-ttu-id="95e0a-245">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-245">Update-VpnConnection</span></span>
* <span data-ttu-id="95e0a-246">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-248">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="95e0a-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="95e0a-249">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-250">Az.Resources</span></span>
* <span data-ttu-id="95e0a-251">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="95e0a-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95e0a-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="95e0a-253">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="95e0a-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="95e0a-254">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="95e0a-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="95e0a-255">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="95e0a-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95e0a-256">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="95e0a-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="95e0a-257">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="95e0a-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="95e0a-258">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="95e0a-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="95e0a-259">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="95e0a-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95e0a-260">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="95e0a-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95e0a-261">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="95e0a-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="95e0a-262">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="95e0a-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="95e0a-263">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="95e0a-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="95e0a-264">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="95e0a-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95e0a-265">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="95e0a-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="95e0a-266">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="95e0a-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="95e0a-267">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="95e0a-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="95e0a-268">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="95e0a-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="95e0a-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="95e0a-269">Az.SignalR</span></span>
* <span data-ttu-id="95e0a-270">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="95e0a-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-271">Az.Sql</span></span>
* <span data-ttu-id="95e0a-272">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="95e0a-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="95e0a-273">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="95e0a-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="95e0a-274">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="95e0a-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="95e0a-275">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="95e0a-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="95e0a-276">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="95e0a-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-277">Az.Storage</span></span>
* <span data-ttu-id="95e0a-278">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="95e0a-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="95e0a-279">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="95e0a-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="95e0a-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="95e0a-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="95e0a-282">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="95e0a-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="95e0a-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="95e0a-284">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="95e0a-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="95e0a-285">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="95e0a-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="95e0a-286">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="95e0a-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="95e0a-287">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="95e0a-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="95e0a-288">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="95e0a-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-289">Az.Websites</span></span>
* <span data-ttu-id="95e0a-290">Исправлена проблема, из-за которой теги веб-приложений удалялись при переносе приложения на новый план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="95e0a-291">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="95e0a-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="95e0a-292">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="95e0a-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="95e0a-293">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="95e0a-294">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="95e0a-294">General</span></span>
* <span data-ttu-id="95e0a-295">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="95e0a-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95e0a-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-296">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-297">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="95e0a-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="95e0a-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="95e0a-298">Az.Aks</span></span>
* <span data-ttu-id="95e0a-299">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="95e0a-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="95e0a-300">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="95e0a-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="95e0a-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95e0a-301">Az.ApiManagement</span></span>
* <span data-ttu-id="95e0a-302">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="95e0a-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="95e0a-303">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="95e0a-304">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="95e0a-305">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="95e0a-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="95e0a-306">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="95e0a-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="95e0a-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95e0a-307">Az.Batch</span></span>
* <span data-ttu-id="95e0a-308">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95e0a-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95e0a-309">Az.Cdn</span></span>
* <span data-ttu-id="95e0a-310">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="95e0a-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-311">Az.Compute</span></span>
* <span data-ttu-id="95e0a-312">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="95e0a-313">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="95e0a-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="95e0a-314">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95e0a-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="95e0a-315">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="95e0a-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="95e0a-316">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="95e0a-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="95e0a-317">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="95e0a-318">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="95e0a-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="95e0a-319">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="95e0a-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-320">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-321">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="95e0a-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="95e0a-322">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="95e0a-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="95e0a-323">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="95e0a-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="95e0a-324">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="95e0a-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-326">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95e0a-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-327">Az.EventHub</span></span>
* <span data-ttu-id="95e0a-328">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="95e0a-329">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="95e0a-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="95e0a-330">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="95e0a-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="95e0a-331">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="95e0a-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="95e0a-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="95e0a-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="95e0a-333">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="95e0a-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95e0a-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-334">Az.Monitor</span></span>
* <span data-ttu-id="95e0a-335">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-336">Az.Network</span></span>
* <span data-ttu-id="95e0a-337">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="95e0a-338">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="95e0a-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="95e0a-339">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="95e0a-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="95e0a-340">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="95e0a-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="95e0a-341">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="95e0a-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="95e0a-342">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="95e0a-343">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="95e0a-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95e0a-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="95e0a-345">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="95e0a-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="95e0a-346">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="95e0a-346">Added example</span></span>
    - <span data-ttu-id="95e0a-347">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="95e0a-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="95e0a-348">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="95e0a-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="95e0a-349">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="95e0a-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-351">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-352">Az.Resources</span></span>
* <span data-ttu-id="95e0a-353">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="95e0a-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="95e0a-354">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="95e0a-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="95e0a-355">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="95e0a-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="95e0a-356">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95e0a-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95e0a-357">Az.ServiceBus</span></span>
* <span data-ttu-id="95e0a-358">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="95e0a-359">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="95e0a-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="95e0a-360">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="95e0a-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95e0a-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="95e0a-362">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="95e0a-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="95e0a-363">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="95e0a-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="95e0a-364">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="95e0a-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="95e0a-365">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="95e0a-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="95e0a-366">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="95e0a-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="95e0a-367">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="95e0a-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-368">Az.Sql</span></span>
* <span data-ttu-id="95e0a-369">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="95e0a-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-370">Az.Storage</span></span>
* <span data-ttu-id="95e0a-371">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="95e0a-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="95e0a-372">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="95e0a-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="95e0a-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="95e0a-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="95e0a-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="95e0a-375">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="95e0a-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="95e0a-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="95e0a-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-377">Az.Websites</span></span>
* <span data-ttu-id="95e0a-378">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="95e0a-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="95e0a-379">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-380">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-381">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="95e0a-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="95e0a-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="95e0a-383">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="95e0a-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-384">Az.Automation</span></span>
* <span data-ttu-id="95e0a-385">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="95e0a-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95e0a-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="95e0a-387">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-388">Az.Compute</span></span>
* <span data-ttu-id="95e0a-389">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95e0a-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="95e0a-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="95e0a-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="95e0a-391">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="95e0a-392">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="95e0a-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-393">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-394">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="95e0a-395">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="95e0a-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95e0a-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-396">Az.EventHub</span></span>
* <span data-ttu-id="95e0a-397">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="95e0a-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="95e0a-398">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="95e0a-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95e0a-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95e0a-399">Az.KeyVault</span></span>
* <span data-ttu-id="95e0a-400">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95e0a-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95e0a-401">Az.LogicApp</span></span>
* <span data-ttu-id="95e0a-402">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="95e0a-403">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="95e0a-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-404">Az.ManagedServices</span></span>
* <span data-ttu-id="95e0a-405">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="95e0a-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-406">Az.Network</span></span>
* <span data-ttu-id="95e0a-407">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="95e0a-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="95e0a-408">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-408">New cmdlets</span></span>
        - <span data-ttu-id="95e0a-409">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="95e0a-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95e0a-410">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="95e0a-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="95e0a-411">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95e0a-412">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95e0a-413">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95e0a-414">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95e0a-415">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="95e0a-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="95e0a-416">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="95e0a-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="95e0a-417">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="95e0a-418">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="95e0a-419">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="95e0a-420">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="95e0a-421">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="95e0a-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="95e0a-422">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="95e0a-423">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-423">Updated cmdlets</span></span>
        - <span data-ttu-id="95e0a-424">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95e0a-425">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95e0a-426">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="95e0a-427">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="95e0a-428">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="95e0a-429">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="95e0a-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="95e0a-430">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="95e0a-431">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="95e0a-432">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="95e0a-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="95e0a-433">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="95e0a-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="95e0a-434">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="95e0a-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="95e0a-435">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="95e0a-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95e0a-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="95e0a-437">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="95e0a-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="95e0a-438">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-440">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="95e0a-441">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="95e0a-442">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="95e0a-443">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="95e0a-444">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="95e0a-445">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="95e0a-446">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="95e0a-447">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="95e0a-448">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="95e0a-449">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="95e0a-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-450">Az.Resources</span></span>
- <span data-ttu-id="95e0a-451">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="95e0a-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="95e0a-452">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="95e0a-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95e0a-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95e0a-453">Az.ServiceBus</span></span>
* <span data-ttu-id="95e0a-454">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="95e0a-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="95e0a-455">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="95e0a-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-456">Az.Sql</span></span>
* <span data-ttu-id="95e0a-457">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="95e0a-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="95e0a-458">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="95e0a-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="95e0a-459">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-460">Az.Storage</span></span>
* <span data-ttu-id="95e0a-461">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="95e0a-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="95e0a-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="95e0a-462">Az.StorageSync</span></span>
* <span data-ttu-id="95e0a-463">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="95e0a-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="95e0a-464">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="95e0a-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-465">Az.Websites</span></span>
* <span data-ttu-id="95e0a-466">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="95e0a-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="95e0a-467">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="95e0a-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="95e0a-468">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="95e0a-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="95e0a-469">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-470">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-471">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="95e0a-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="95e0a-472">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="95e0a-473">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="95e0a-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="95e0a-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="95e0a-474">Az.Advisor</span></span>
* <span data-ttu-id="95e0a-475">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="95e0a-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="95e0a-476">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="95e0a-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95e0a-477">Az.ApiManagement</span></span>
* <span data-ttu-id="95e0a-478">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="95e0a-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="95e0a-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="95e0a-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="95e0a-480">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="95e0a-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="95e0a-481">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="95e0a-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="95e0a-482">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="95e0a-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="95e0a-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="95e0a-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="95e0a-484">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-485">Az.Automation</span></span>
* <span data-ttu-id="95e0a-486">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-487">Az.Compute</span></span>
* <span data-ttu-id="95e0a-488">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-489">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-490">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="95e0a-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95e0a-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95e0a-491">Az.EventGrid</span></span>
* <span data-ttu-id="95e0a-492">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="95e0a-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95e0a-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-493">Az.IotHub</span></span>
* <span data-ttu-id="95e0a-494">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-495">Az.Network</span></span>
* <span data-ttu-id="95e0a-496">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="95e0a-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="95e0a-497">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="95e0a-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95e0a-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="95e0a-499">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="95e0a-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="95e0a-500">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="95e0a-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95e0a-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="95e0a-502">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="95e0a-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-504">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="95e0a-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-505">Az.Resources</span></span>
    - <span data-ttu-id="95e0a-506">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="95e0a-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="95e0a-507">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="95e0a-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="95e0a-508">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="95e0a-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="95e0a-509">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="95e0a-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95e0a-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95e0a-510">Az.ServiceBus</span></span>
* <span data-ttu-id="95e0a-511">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="95e0a-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-512">Az.Sql</span></span>
* <span data-ttu-id="95e0a-513">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="95e0a-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="95e0a-514">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="95e0a-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="95e0a-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="95e0a-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="95e0a-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="95e0a-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="95e0a-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="95e0a-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="95e0a-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="95e0a-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="95e0a-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="95e0a-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="95e0a-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="95e0a-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="95e0a-521">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="95e0a-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-522">Az.Storage</span></span>
* <span data-ttu-id="95e0a-523">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="95e0a-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="95e0a-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="95e0a-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="95e0a-525">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="95e0a-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="95e0a-526">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="95e0a-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="95e0a-527">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="95e0a-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="95e0a-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="95e0a-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="95e0a-530">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="95e0a-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="95e0a-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="95e0a-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="95e0a-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="95e0a-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="95e0a-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="95e0a-533">Az.StorageSync</span></span>
* <span data-ttu-id="95e0a-534">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="95e0a-535">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-536">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-537">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="95e0a-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="95e0a-538">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="95e0a-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="95e0a-539">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="95e0a-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="95e0a-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="95e0a-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="95e0a-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="95e0a-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-542">Az.Compute</span></span>
* <span data-ttu-id="95e0a-543">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="95e0a-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="95e0a-544">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="95e0a-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="95e0a-545">Az.Dns</span></span>
* <span data-ttu-id="95e0a-546">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="95e0a-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95e0a-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95e0a-547">Az.EventGrid</span></span>
* <span data-ttu-id="95e0a-548">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="95e0a-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="95e0a-549">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="95e0a-549">New cmdlets:</span></span>
    - <span data-ttu-id="95e0a-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="95e0a-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="95e0a-551">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="95e0a-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="95e0a-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="95e0a-553">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="95e0a-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="95e0a-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="95e0a-555">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="95e0a-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="95e0a-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="95e0a-557">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="95e0a-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="95e0a-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="95e0a-559">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="95e0a-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="95e0a-560">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="95e0a-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="95e0a-561">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="95e0a-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="95e0a-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="95e0a-563">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="95e0a-564">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="95e0a-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="95e0a-565">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="95e0a-566">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="95e0a-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="95e0a-567">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="95e0a-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="95e0a-568">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="95e0a-569">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="95e0a-570">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="95e0a-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="95e0a-571">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="95e0a-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="95e0a-572">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="95e0a-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="95e0a-573">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="95e0a-574">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="95e0a-575">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="95e0a-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="95e0a-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="95e0a-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="95e0a-577">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="95e0a-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="95e0a-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="95e0a-579">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="95e0a-580">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="95e0a-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95e0a-581">Az.FrontDoor</span></span>
* <span data-ttu-id="95e0a-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="95e0a-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="95e0a-583">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="95e0a-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="95e0a-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="95e0a-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="95e0a-585">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-586">Az.Network</span></span>
* <span data-ttu-id="95e0a-587">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="95e0a-588">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-588">New cmdlets</span></span>
        - <span data-ttu-id="95e0a-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="95e0a-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="95e0a-590">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="95e0a-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="95e0a-591">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-591">New cmdlets</span></span>
        - <span data-ttu-id="95e0a-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="95e0a-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="95e0a-593">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="95e0a-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="95e0a-594">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-594">New cmdlets</span></span>
        - <span data-ttu-id="95e0a-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95e0a-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="95e0a-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95e0a-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="95e0a-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95e0a-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="95e0a-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="95e0a-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="95e0a-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95e0a-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="95e0a-600">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="95e0a-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="95e0a-601">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-601">New cmdlets</span></span>
        - <span data-ttu-id="95e0a-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95e0a-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95e0a-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95e0a-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95e0a-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95e0a-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95e0a-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="95e0a-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="95e0a-606">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="95e0a-607">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="95e0a-608">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="95e0a-609">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="95e0a-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="95e0a-610">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="95e0a-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="95e0a-611">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="95e0a-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="95e0a-612">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="95e0a-613">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="95e0a-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="95e0a-614">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="95e0a-615">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="95e0a-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="95e0a-616">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="95e0a-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="95e0a-617">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="95e0a-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="95e0a-618">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="95e0a-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="95e0a-619">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="95e0a-620">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="95e0a-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="95e0a-621">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="95e0a-622">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="95e0a-623">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="95e0a-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="95e0a-624">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="95e0a-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="95e0a-625">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="95e0a-626">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="95e0a-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="95e0a-627">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="95e0a-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="95e0a-628">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="95e0a-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95e0a-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="95e0a-630">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="95e0a-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-631">Az.Resources</span></span>
* <span data-ttu-id="95e0a-632">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="95e0a-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="95e0a-633">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="95e0a-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="95e0a-634">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="95e0a-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="95e0a-635">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95e0a-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="95e0a-637">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="95e0a-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-638">Az.Sql</span></span>
* <span data-ttu-id="95e0a-639">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="95e0a-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="95e0a-640">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="95e0a-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="95e0a-641">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="95e0a-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="95e0a-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="95e0a-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="95e0a-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="95e0a-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="95e0a-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="95e0a-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="95e0a-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="95e0a-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="95e0a-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="95e0a-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-647">Az.Storage</span></span>
* <span data-ttu-id="95e0a-648">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="95e0a-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="95e0a-650">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="95e0a-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="95e0a-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-652">Az.Websites</span></span>
* <span data-ttu-id="95e0a-653">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="95e0a-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="95e0a-654">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="95e0a-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="95e0a-655">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="95e0a-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95e0a-656">Az.Cdn</span></span>
* <span data-ttu-id="95e0a-657">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="95e0a-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-658">Az.Compute</span></span>
* <span data-ttu-id="95e0a-659">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="95e0a-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="95e0a-660">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95e0a-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-661">Az.EventHub</span></span>
* <span data-ttu-id="95e0a-662">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="95e0a-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="95e0a-663">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="95e0a-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-664">Az.Network</span></span>
* <span data-ttu-id="95e0a-665">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="95e0a-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="95e0a-666">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="95e0a-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95e0a-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="95e0a-668">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="95e0a-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-670">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="95e0a-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95e0a-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95e0a-671">Az.ServiceBus</span></span>
* <span data-ttu-id="95e0a-672">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="95e0a-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95e0a-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="95e0a-674">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="95e0a-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="95e0a-675">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="95e0a-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-676">Az.Sql</span></span>
* <span data-ttu-id="95e0a-677">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="95e0a-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="95e0a-678">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="95e0a-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="95e0a-679">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="95e0a-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="95e0a-680">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="95e0a-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-681">Az.Websites</span></span>
* <span data-ttu-id="95e0a-682">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="95e0a-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="95e0a-683">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="95e0a-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95e0a-684">Az.ApiManagement</span></span>
* <span data-ttu-id="95e0a-685">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="95e0a-686">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="95e0a-687">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="95e0a-688">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="95e0a-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="95e0a-689">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="95e0a-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="95e0a-690">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="95e0a-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="95e0a-691">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="95e0a-692">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="95e0a-693">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="95e0a-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="95e0a-694">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="95e0a-695">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="95e0a-696">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="95e0a-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="95e0a-697">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="95e0a-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="95e0a-698">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="95e0a-699">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="95e0a-700">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="95e0a-701">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="95e0a-702">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="95e0a-703">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="95e0a-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="95e0a-704">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="95e0a-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="95e0a-705">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="95e0a-706">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="95e0a-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="95e0a-707">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="95e0a-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="95e0a-708">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="95e0a-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="95e0a-709">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="95e0a-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="95e0a-710">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="95e0a-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="95e0a-711">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="95e0a-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="95e0a-712">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="95e0a-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="95e0a-713">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="95e0a-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="95e0a-714">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="95e0a-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="95e0a-715">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="95e0a-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="95e0a-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="95e0a-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="95e0a-717">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="95e0a-718">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="95e0a-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="95e0a-719">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="95e0a-720">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="95e0a-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="95e0a-721">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="95e0a-722">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="95e0a-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="95e0a-723">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="95e0a-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="95e0a-724">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="95e0a-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="95e0a-725">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="95e0a-726">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="95e0a-727">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="95e0a-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="95e0a-728">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="95e0a-729">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="95e0a-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="95e0a-730">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="95e0a-731">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="95e0a-732">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="95e0a-733">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="95e0a-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="95e0a-734">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="95e0a-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="95e0a-735">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="95e0a-736">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="95e0a-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="95e0a-737">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="95e0a-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="95e0a-738">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="95e0a-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="95e0a-739">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="95e0a-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="95e0a-740">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="95e0a-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="95e0a-741">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="95e0a-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="95e0a-742">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="95e0a-743">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="95e0a-744">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="95e0a-745">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="95e0a-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="95e0a-746">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="95e0a-747">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="95e0a-748">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="95e0a-749">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="95e0a-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="95e0a-750">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="95e0a-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="95e0a-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="95e0a-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="95e0a-752">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="95e0a-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="95e0a-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="95e0a-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="95e0a-754">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="95e0a-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="95e0a-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="95e0a-756">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="95e0a-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="95e0a-757">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="95e0a-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="95e0a-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="95e0a-759">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="95e0a-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="95e0a-760">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="95e0a-761">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="95e0a-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-762">Az.Automation</span></span>
* <span data-ttu-id="95e0a-763">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="95e0a-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="95e0a-764">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="95e0a-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="95e0a-765">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="95e0a-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="95e0a-766">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="95e0a-767">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="95e0a-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="95e0a-768">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="95e0a-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="95e0a-769">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="95e0a-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-770">Az.Compute</span></span>
* <span data-ttu-id="95e0a-771">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="95e0a-772">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95e0a-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-774">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="95e0a-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95e0a-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-775">Az.Monitor</span></span>
* <span data-ttu-id="95e0a-776">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-777">Az.Network</span></span>
* <span data-ttu-id="95e0a-778">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="95e0a-779">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="95e0a-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="95e0a-780">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="95e0a-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="95e0a-781">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="95e0a-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-782">Az.Resources</span></span>
* <span data-ttu-id="95e0a-783">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-784">Az.Sql</span></span>
* <span data-ttu-id="95e0a-785">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95e0a-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="95e0a-786">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-787">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-788">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="95e0a-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95e0a-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="95e0a-790">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="95e0a-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="95e0a-791">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="95e0a-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-792">Az.Compute</span></span>
* <span data-ttu-id="95e0a-793">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="95e0a-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="95e0a-794">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="95e0a-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="95e0a-795">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="95e0a-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="95e0a-796">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="95e0a-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="95e0a-797">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="95e0a-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="95e0a-798">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="95e0a-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="95e0a-799">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="95e0a-799">Breaking changes</span></span>
    - <span data-ttu-id="95e0a-800">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="95e0a-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="95e0a-801">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="95e0a-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="95e0a-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="95e0a-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="95e0a-803">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="95e0a-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="95e0a-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="95e0a-804">Az.Dns</span></span>
* <span data-ttu-id="95e0a-805">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="95e0a-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="95e0a-806">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="95e0a-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="95e0a-807">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="95e0a-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="95e0a-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95e0a-808">Az.FrontDoor</span></span>
* <span data-ttu-id="95e0a-809">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="95e0a-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="95e0a-810">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="95e0a-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="95e0a-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95e0a-811">Az.HDInsight</span></span>
* <span data-ttu-id="95e0a-812">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="95e0a-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="95e0a-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="95e0a-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="95e0a-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="95e0a-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="95e0a-815">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="95e0a-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="95e0a-816">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="95e0a-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="95e0a-817">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="95e0a-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="95e0a-818">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="95e0a-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95e0a-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-819">Az.Monitor</span></span>
* <span data-ttu-id="95e0a-820">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="95e0a-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="95e0a-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="95e0a-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="95e0a-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="95e0a-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="95e0a-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="95e0a-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="95e0a-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="95e0a-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="95e0a-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="95e0a-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="95e0a-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="95e0a-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="95e0a-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95e0a-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95e0a-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95e0a-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95e0a-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95e0a-832">См. подробнее об [API SQR](/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="95e0a-832">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="95e0a-833">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="95e0a-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-834">Az.Network</span></span>
* <span data-ttu-id="95e0a-835">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="95e0a-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="95e0a-836">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-836">New cmdlets</span></span>
        - <span data-ttu-id="95e0a-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95e0a-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="95e0a-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95e0a-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="95e0a-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95e0a-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="95e0a-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95e0a-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="95e0a-841">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="95e0a-841">Updated cmdlets</span></span>
        - <span data-ttu-id="95e0a-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="95e0a-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="95e0a-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="95e0a-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="95e0a-844">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="95e0a-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="95e0a-845">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="95e0a-846">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95e0a-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="95e0a-848">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="95e0a-849">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="95e0a-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="95e0a-850">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="95e0a-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-852">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95e0a-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="95e0a-853">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95e0a-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="95e0a-854">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95e0a-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="95e0a-855">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="95e0a-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="95e0a-856">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="95e0a-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="95e0a-857">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="95e0a-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="95e0a-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="95e0a-858">Az.Relay</span></span>
* <span data-ttu-id="95e0a-859">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95e0a-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95e0a-860">Az.ServiceBus</span></span>
* <span data-ttu-id="95e0a-861">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="95e0a-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-862">Az.Storage</span></span>
* <span data-ttu-id="95e0a-863">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="95e0a-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="95e0a-864">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="95e0a-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="95e0a-865">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="95e0a-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="95e0a-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="95e0a-867">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="95e0a-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="95e0a-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="95e0a-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="95e0a-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-871">Az.Websites</span></span>
* <span data-ttu-id="95e0a-872">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="95e0a-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="95e0a-873">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="95e0a-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="95e0a-874">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95e0a-875">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="95e0a-875">Highlights since the last major release</span></span>
* <span data-ttu-id="95e0a-876">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-876">General availability of `Az` module</span></span>
* <span data-ttu-id="95e0a-877">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="95e0a-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="95e0a-878">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="95e0a-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="95e0a-879">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="95e0a-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="95e0a-880">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="95e0a-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95e0a-881">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="95e0a-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="95e0a-882">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="95e0a-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95e0a-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-883">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-884">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="95e0a-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="95e0a-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95e0a-885">Az.Batch</span></span>
* <span data-ttu-id="95e0a-886">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95e0a-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95e0a-887">Az.Cdn</span></span>
* <span data-ttu-id="95e0a-888">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95e0a-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="95e0a-890">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-891">Az.Compute</span></span>
* <span data-ttu-id="95e0a-892">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="95e0a-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="95e0a-893">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95e0a-894">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="95e0a-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-895">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-896">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="95e0a-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-898">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95e0a-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95e0a-899">Az.EventGrid</span></span>
* <span data-ttu-id="95e0a-900">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="95e0a-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95e0a-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-901">Az.EventHub</span></span>
* <span data-ttu-id="95e0a-902">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="95e0a-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="95e0a-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95e0a-903">Az.HDInsight</span></span>
* <span data-ttu-id="95e0a-904">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95e0a-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-905">Az.IotHub</span></span>
* <span data-ttu-id="95e0a-906">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95e0a-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95e0a-907">Az.KeyVault</span></span>
* <span data-ttu-id="95e0a-908">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95e0a-909">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="95e0a-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="95e0a-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="95e0a-910">Az.MachineLearning</span></span>
* <span data-ttu-id="95e0a-911">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="95e0a-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="95e0a-912">Az.Media</span></span>
* <span data-ttu-id="95e0a-913">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95e0a-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-914">Az.Monitor</span></span>
  * <span data-ttu-id="95e0a-915">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="95e0a-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="95e0a-916">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="95e0a-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="95e0a-917">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="95e0a-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="95e0a-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="95e0a-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="95e0a-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="95e0a-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="95e0a-920">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="95e0a-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="95e0a-921">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-922">Az.Network</span></span>
* <span data-ttu-id="95e0a-923">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95e0a-924">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="95e0a-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="95e0a-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="95e0a-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="95e0a-926">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95e0a-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="95e0a-928">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="95e0a-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="95e0a-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="95e0a-930">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-932">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95e0a-933">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="95e0a-934">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="95e0a-935">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="95e0a-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="95e0a-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="95e0a-936">Az.RedisCache</span></span>
* <span data-ttu-id="95e0a-937">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-938">Az.Resources</span></span>
* <span data-ttu-id="95e0a-939">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="95e0a-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-940">Az.Sql</span></span>
* <span data-ttu-id="95e0a-941">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="95e0a-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="95e0a-942">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95e0a-943">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="95e0a-944">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="95e0a-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="95e0a-945">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="95e0a-946">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="95e0a-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="95e0a-947">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="95e0a-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-948">Az.Websites</span></span>
* <span data-ttu-id="95e0a-949">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="95e0a-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="95e0a-950">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="95e0a-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95e0a-951">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="95e0a-952">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="95e0a-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="95e0a-953">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95e0a-954">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="95e0a-954">Highlights since the last major release</span></span>
* <span data-ttu-id="95e0a-955">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-955">General availability of `Az` module</span></span>
* <span data-ttu-id="95e0a-956">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="95e0a-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="95e0a-957">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="95e0a-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="95e0a-958">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="95e0a-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="95e0a-959">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="95e0a-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95e0a-960">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="95e0a-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="95e0a-961">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="95e0a-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95e0a-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-962">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-963">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="95e0a-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="95e0a-965">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="95e0a-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="95e0a-966">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-967">Az.Automation</span></span>
* <span data-ttu-id="95e0a-968">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="95e0a-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="95e0a-969">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="95e0a-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="95e0a-970">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-971">Az.Compute</span></span>
* <span data-ttu-id="95e0a-972">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="95e0a-973">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="95e0a-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="95e0a-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="95e0a-975">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="95e0a-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-976">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-977">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="95e0a-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="95e0a-978">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-979">Az.Resources</span></span>
* <span data-ttu-id="95e0a-980">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="95e0a-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="95e0a-981">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="95e0a-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="95e0a-982">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="95e0a-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="95e0a-983">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="95e0a-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="95e0a-984">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="95e0a-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="95e0a-985">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="95e0a-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-986">Az.Sql</span></span>
* <span data-ttu-id="95e0a-987">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="95e0a-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-988">Az.Storage</span></span>
* <span data-ttu-id="95e0a-989">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="95e0a-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="95e0a-990">New-AzStorageContext</span></span>
* <span data-ttu-id="95e0a-991">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="95e0a-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="95e0a-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="95e0a-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="95e0a-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="95e0a-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="95e0a-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="95e0a-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="95e0a-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="95e0a-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="95e0a-996">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="95e0a-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="95e0a-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="95e0a-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="95e0a-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95e0a-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="95e0a-1001">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95e0a-1002">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="95e0a-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="95e0a-1003">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="95e0a-1004">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="95e0a-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="95e0a-1005">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="95e0a-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="95e0a-1006">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="95e0a-1007">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95e0a-1008">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="95e0a-1009">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-1010">Az.Automation</span></span>
* <span data-ttu-id="95e0a-1011">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="95e0a-1012">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="95e0a-1013">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1013">Pre-Post script</span></span>
    * <span data-ttu-id="95e0a-1014">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1015">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1016">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="95e0a-1017">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95e0a-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95e0a-1018">Az.KeyVault</span></span>
* <span data-ttu-id="95e0a-1019">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1020">Az.Network</span></span>
* <span data-ttu-id="95e0a-1021">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="95e0a-1022">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-1024">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="95e0a-1025">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1026">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1027">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="95e0a-1028">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1029">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1030">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-1031">Az.Storage</span></span>
* <span data-ttu-id="95e0a-1032">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="95e0a-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95e0a-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="95e0a-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95e0a-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="95e0a-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95e0a-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="95e0a-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="95e0a-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="95e0a-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="95e0a-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="95e0a-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-1039">Az.Websites</span></span>
* <span data-ttu-id="95e0a-1040">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="95e0a-1041">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-1042">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-1043">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="95e0a-1044">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-1045">Az.Automation</span></span>
* <span data-ttu-id="95e0a-1046">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="95e0a-1047">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="95e0a-1048">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95e0a-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95e0a-1049">Az.Cdn</span></span>
* <span data-ttu-id="95e0a-1050">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1051">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1052">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-1053">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-1054">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95e0a-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95e0a-1055">Az.LogicApp</span></span>
* <span data-ttu-id="95e0a-1056">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1057">Az.Network</span></span>
* <span data-ttu-id="95e0a-1058">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-1060">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="95e0a-1061">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="95e0a-1061">SDK Update</span></span>
* <span data-ttu-id="95e0a-1062">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="95e0a-1063">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1064">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1065">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="95e0a-1066">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="95e0a-1067">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="95e0a-1068">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="95e0a-1069">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="95e0a-1070">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1071">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1072">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="95e0a-1073">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-1074">Az.Storage</span></span>
* <span data-ttu-id="95e0a-1075">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="95e0a-1076">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="95e0a-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="95e0a-1078">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-1079">Az.Automation</span></span>
* <span data-ttu-id="95e0a-1080">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="95e0a-1081">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="95e0a-1082">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95e0a-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="95e0a-1084">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1085">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1086">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="95e0a-1087">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="95e0a-1088">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="95e0a-1089">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-1091">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95e0a-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-1092">Az.EventHub</span></span>
* <span data-ttu-id="95e0a-1093">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95e0a-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95e0a-1094">Az.KeyVault</span></span>
* <span data-ttu-id="95e0a-1095">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95e0a-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95e0a-1096">Az.LogicApp</span></span>
* <span data-ttu-id="95e0a-1097">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="95e0a-1098">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="95e0a-1099">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="95e0a-1100">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="95e0a-1101">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="95e0a-1102">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="95e0a-1103">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="95e0a-1104">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="95e0a-1105">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="95e0a-1106">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="95e0a-1107">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="95e0a-1108">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="95e0a-1109">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95e0a-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-1110">Az.Monitor</span></span>
* <span data-ttu-id="95e0a-1111">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1112">Az.Network</span></span>
* <span data-ttu-id="95e0a-1113">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95e0a-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="95e0a-1115">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="95e0a-1116">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="95e0a-1117">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1118">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1119">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="95e0a-1120">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="95e0a-1121">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="95e0a-1122">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1123">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1124">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="95e0a-1125">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-1126">Az.Websites</span></span>
* <span data-ttu-id="95e0a-1127">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="95e0a-1128">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-1129">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-1130">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="95e0a-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="95e0a-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="95e0a-1132">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1133">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1134">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="95e0a-1135">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="95e0a-1136">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="95e0a-1138">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1139">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1140">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="95e0a-1141">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="95e0a-1142">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="95e0a-1143">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1144">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1145">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="95e0a-1146">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="95e0a-1147">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="95e0a-1148">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-1149">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-1150">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="95e0a-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="95e0a-1152">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="95e0a-1154">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="95e0a-1155">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-1156">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-1157">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95e0a-1158">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95e0a-1159">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="95e0a-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="95e0a-1160">Az.Aks</span></span>
* <span data-ttu-id="95e0a-1161">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95e0a-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-1162">Az.Automation</span></span>
* <span data-ttu-id="95e0a-1163">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="95e0a-1164">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95e0a-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95e0a-1165">Az.Cdn</span></span>
* <span data-ttu-id="95e0a-1166">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1167">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1168">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="95e0a-1169">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="95e0a-1170">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="95e0a-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="95e0a-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="95e0a-1172">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95e0a-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95e0a-1173">Az.DataFactory</span></span>
* <span data-ttu-id="95e0a-1174">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-1176">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="95e0a-1177">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="95e0a-1178">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95e0a-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-1179">Az.IotHub</span></span>
* <span data-ttu-id="95e0a-1180">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95e0a-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95e0a-1181">Az.KeyVault</span></span>
* <span data-ttu-id="95e0a-1182">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1183">Az.Network</span></span>
* <span data-ttu-id="95e0a-1184">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1185">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1186">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="95e0a-1187">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="95e0a-1188">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="95e0a-1189">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="95e0a-1190">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="95e0a-1191">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="95e0a-1192">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95e0a-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="95e0a-1194">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="95e0a-1195">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1195">Fix some error messages.</span></span>
* <span data-ttu-id="95e0a-1196">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="95e0a-1197">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="95e0a-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="95e0a-1198">Az.SignalR</span></span>
* <span data-ttu-id="95e0a-1199">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1200">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1201">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95e0a-1202">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="95e0a-1203">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="95e0a-1204">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-1205">Az.Storage</span></span>
* <span data-ttu-id="95e0a-1206">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95e0a-1207">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="95e0a-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="95e0a-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="95e0a-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="95e0a-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="95e0a-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="95e0a-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="95e0a-1211">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-1212">Az.Websites</span></span>
* <span data-ttu-id="95e0a-1213">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95e0a-1214">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="95e0a-1215">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="95e0a-1216">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95e0a-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-1217">Az.Accounts</span></span>
* <span data-ttu-id="95e0a-1218">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1219">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1220">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="95e0a-1221">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="95e0a-1222">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-1224">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="95e0a-1225">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95e0a-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95e0a-1226">Az.EventGrid</span></span>
* <span data-ttu-id="95e0a-1227">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="95e0a-1228">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="95e0a-1229">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="95e0a-1230">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="95e0a-1231">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="95e0a-1232">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="95e0a-1233">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="95e0a-1234">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="95e0a-1235">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="95e0a-1236">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="95e0a-1237">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="95e0a-1238">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95e0a-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95e0a-1239">Az.IotHub</span></span>
* <span data-ttu-id="95e0a-1240">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95e0a-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95e0a-1241">Az.LogicApp</span></span>
* <span data-ttu-id="95e0a-1242">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1243">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1244">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="95e0a-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="95e0a-1245">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="95e0a-1246">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="95e0a-1247">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="95e0a-1248">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="95e0a-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="95e0a-1249">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="95e0a-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="95e0a-1250">Az.SignalR</span></span>
* <span data-ttu-id="95e0a-1251">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1252">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1253">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95e0a-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-1254">Az.Storage</span></span>
* <span data-ttu-id="95e0a-1255">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="95e0a-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="95e0a-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="95e0a-1257">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="95e0a-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="95e0a-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-1259">Az.Websites</span></span>
* <span data-ttu-id="95e0a-1260">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="95e0a-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="95e0a-1261">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="95e0a-1262">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="95e0a-1263">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="95e0a-1263">General</span></span>

- <span data-ttu-id="95e0a-1264">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="95e0a-1265">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1265">Online help for each module</span></span>
- <span data-ttu-id="95e0a-1266">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="95e0a-1267">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="95e0a-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95e0a-1268">Az.Accounts</span></span>
- <span data-ttu-id="95e0a-1269">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="95e0a-1270">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="95e0a-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95e0a-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="95e0a-1272">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1272">Fixes for #7002</span></span>
- <span data-ttu-id="95e0a-1273">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="95e0a-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95e0a-1274">Az.Batch</span></span>
- <span data-ttu-id="95e0a-1275">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="95e0a-1276">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="95e0a-1277">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="95e0a-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="95e0a-1278">Az.Billing</span></span>
- <span data-ttu-id="95e0a-1279">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="95e0a-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="95e0a-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="95e0a-1281">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="95e0a-1282">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="95e0a-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="95e0a-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="95e0a-1284">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="95e0a-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="95e0a-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="95e0a-1286">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="95e0a-1288">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="95e0a-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95e0a-1289">Az.Monitor</span></span>
- <span data-ttu-id="95e0a-1290">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="95e0a-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95e0a-1291">Az.KeyVault</span></span>
- <span data-ttu-id="95e0a-1292">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="95e0a-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="95e0a-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="95e0a-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="95e0a-1294">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="95e0a-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="95e0a-1295">Az.Media</span></span>
- <span data-ttu-id="95e0a-1296">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="95e0a-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="95e0a-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1297">Az.Network</span></span>
<span data-ttu-id="95e0a-1298">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="95e0a-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="95e0a-1299">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="95e0a-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95e0a-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95e0a-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95e0a-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95e0a-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95e0a-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95e0a-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95e0a-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95e0a-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95e0a-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95e0a-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="95e0a-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="95e0a-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="95e0a-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="95e0a-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="95e0a-1308">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95e0a-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="95e0a-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95e0a-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="95e0a-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="95e0a-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="95e0a-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="95e0a-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95e0a-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="95e0a-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="95e0a-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="95e0a-1314">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="95e0a-1315">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="95e0a-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="95e0a-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="95e0a-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="95e0a-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="95e0a-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="95e0a-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="95e0a-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="95e0a-1319">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="95e0a-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="95e0a-1320">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="95e0a-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="95e0a-1322">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="95e0a-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="95e0a-1323">Az.Profile</span></span>
- <span data-ttu-id="95e0a-1324">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="95e0a-1326">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="95e0a-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1327">Az.Resources</span></span>
- <span data-ttu-id="95e0a-1328">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="95e0a-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="95e0a-1330">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="95e0a-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="95e0a-1331">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="95e0a-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="95e0a-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="95e0a-1333">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="95e0a-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="95e0a-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1334">Az.Sql</span></span>
- <span data-ttu-id="95e0a-1335">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="95e0a-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="95e0a-1336">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="95e0a-1337">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="95e0a-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-1338">Az.Storage</span></span>
- <span data-ttu-id="95e0a-1339">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="95e0a-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-1340">Az.Websites</span></span>
- <span data-ttu-id="95e0a-1341">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="95e0a-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="95e0a-1342">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="95e0a-1343">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="95e0a-1343">General</span></span>

* <span data-ttu-id="95e0a-1344">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="95e0a-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="95e0a-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1345">Az.Compute</span></span>

* <span data-ttu-id="95e0a-1346">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="95e0a-1348">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="95e0a-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="95e0a-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95e0a-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="95e0a-1350">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="95e0a-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="95e0a-1351">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="95e0a-1352">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="95e0a-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="95e0a-1354">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="95e0a-1355">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="95e0a-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1356">Az.Resources</span></span>

* <span data-ttu-id="95e0a-1357">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="95e0a-1358">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="95e0a-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1359">Az.Sql</span></span>

* <span data-ttu-id="95e0a-1360">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="95e0a-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="95e0a-1361">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="95e0a-1362">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="95e0a-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95e0a-1363">Az.Storage</span></span>

* <span data-ttu-id="95e0a-1364">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="95e0a-1365">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="95e0a-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="95e0a-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="95e0a-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="95e0a-1367">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="95e0a-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="95e0a-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="95e0a-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="95e0a-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="95e0a-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="95e0a-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-1370">Az.Websites</span></span>

* <span data-ttu-id="95e0a-1371">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95e0a-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="95e0a-1372">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="95e0a-1373">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="95e0a-1374">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="95e0a-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95e0a-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="95e0a-1376">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="95e0a-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95e0a-1377">Az.Automation</span></span>
* <span data-ttu-id="95e0a-1378">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="95e0a-1379">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="95e0a-1380">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="95e0a-1381">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="95e0a-1382">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="95e0a-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1383">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1384">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="95e0a-1385">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="95e0a-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="95e0a-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="95e0a-1387">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="95e0a-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="95e0a-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="95e0a-1389">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="95e0a-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1390">Az.Network</span></span>
* <span data-ttu-id="95e0a-1391">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="95e0a-1392">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="95e0a-1393">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="95e0a-1394">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="95e0a-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="95e0a-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="95e0a-1396">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="95e0a-1397">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="95e0a-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="95e0a-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="95e0a-1399">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="95e0a-1400">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="95e0a-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="95e0a-1401">Az.Relay</span></span>
* <span data-ttu-id="95e0a-1402">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="95e0a-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1403">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1404">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="95e0a-1405">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="95e0a-1406">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="95e0a-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="95e0a-1408">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="95e0a-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1409">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1410">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="95e0a-1411">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95e0a-1412">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95e0a-1413">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95e0a-1414">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95e0a-1415">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="95e0a-1416">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="95e0a-1417">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="95e0a-1418">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="95e0a-1419">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="95e0a-1420">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="95e0a-1421">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="95e0a-1422">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="95e0a-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="95e0a-1424">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="95e0a-1425">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="95e0a-1426">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="95e0a-1427">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="95e0a-1428">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="95e0a-1428">General</span></span>
* <span data-ttu-id="95e0a-1429">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="95e0a-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="95e0a-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="95e0a-1430">Az.Profile</span></span>
* <span data-ttu-id="95e0a-1431">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="95e0a-1432">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="95e0a-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="95e0a-1433">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="95e0a-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="95e0a-1434">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="95e0a-1435">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="95e0a-1436">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="95e0a-1437">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="95e0a-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="95e0a-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="95e0a-1439">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1440">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1441">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="95e0a-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="95e0a-1442">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="95e0a-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="95e0a-1443">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-1445">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="95e0a-1446">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="95e0a-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="95e0a-1447">Az.Insights</span></span>
* <span data-ttu-id="95e0a-1448">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="95e0a-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="95e0a-1449">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="95e0a-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="95e0a-1450">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="95e0a-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="95e0a-1451">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1452">Az.Network</span></span>
* <span data-ttu-id="95e0a-1453">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="95e0a-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="95e0a-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="95e0a-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="95e0a-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="95e0a-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="95e0a-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="95e0a-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="95e0a-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="95e0a-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="95e0a-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="95e0a-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="95e0a-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95e0a-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95e0a-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="95e0a-1461">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1462">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1463">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="95e0a-1464">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="95e0a-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95e0a-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95e0a-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="95e0a-1466">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95e0a-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95e0a-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="95e0a-1468">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="95e0a-1469">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="95e0a-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="95e0a-1470">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="95e0a-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="95e0a-1471">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="95e0a-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="95e0a-1472">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="95e0a-1473">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="95e0a-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="95e0a-1474">Az.Profile</span></span>
* <span data-ttu-id="95e0a-1475">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="95e0a-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="95e0a-1476">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1477">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1478">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="95e0a-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="95e0a-1479">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95e0a-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95e0a-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="95e0a-1481">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="95e0a-1482">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="95e0a-1483">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="95e0a-1484">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="95e0a-1485">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1486">Az.Network</span></span>
* <span data-ttu-id="95e0a-1487">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="95e0a-1488">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1489">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1490">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="95e0a-1491">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="95e0a-1492">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="95e0a-1493">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="95e0a-1493">Azure.Storage</span></span>
* <span data-ttu-id="95e0a-1494">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="95e0a-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="95e0a-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="95e0a-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="95e0a-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="95e0a-1497">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="95e0a-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="95e0a-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95e0a-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95e0a-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="95e0a-1500">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95e0a-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95e0a-1501">Az.Compute</span></span>
* <span data-ttu-id="95e0a-1502">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="95e0a-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="95e0a-1503">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="95e0a-1504">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="95e0a-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="95e0a-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="95e0a-1506">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95e0a-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95e0a-1507">Az.Network</span></span>
* <span data-ttu-id="95e0a-1508">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="95e0a-1509">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="95e0a-1509">new cmdlets added</span></span>
    - <span data-ttu-id="95e0a-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95e0a-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="95e0a-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95e0a-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="95e0a-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95e0a-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="95e0a-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95e0a-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="95e0a-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="95e0a-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="95e0a-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="95e0a-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="95e0a-1516">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="95e0a-1517">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="95e0a-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="95e0a-1518">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="95e0a-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="95e0a-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="95e0a-1519">Az.RedisCache</span></span>
* <span data-ttu-id="95e0a-1520">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="95e0a-1521">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="95e0a-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95e0a-1522">Az.Resources</span></span>
* <span data-ttu-id="95e0a-1523">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="95e0a-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="95e0a-1524">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="95e0a-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="95e0a-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95e0a-1525">Az.Sql</span></span>
* <span data-ttu-id="95e0a-1526">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95e0a-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95e0a-1527">Az.Websites</span></span>
* <span data-ttu-id="95e0a-1528">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="95e0a-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="95e0a-1529">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="95e0a-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="95e0a-1530">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="95e0a-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="95e0a-1531">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="95e0a-1531">Initial Release</span></span>