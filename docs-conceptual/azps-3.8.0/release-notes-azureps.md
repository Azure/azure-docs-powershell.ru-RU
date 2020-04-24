---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740547"
---
## <a name="380---april-2020"></a><span data-ttu-id="733df-103">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="733df-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-104">Az.Accounts</span></span>
* <span data-ttu-id="733df-105">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="733df-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="733df-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-106">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-107">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="733df-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="733df-108">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="733df-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="733df-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-109">Az.Cdn</span></span>
* <span data-ttu-id="733df-110">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="733df-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-112">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="733df-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="733df-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-113">Az.Compute</span></span>
* <span data-ttu-id="733df-114">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="733df-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="733df-115">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="733df-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-116">Az.IotHub</span></span>
* <span data-ttu-id="733df-117">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="733df-118">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="733df-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="733df-119">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="733df-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="733df-120">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="733df-121">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="733df-122">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="733df-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="733df-123">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="733df-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="733df-124">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="733df-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="733df-125">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-125">New cmdlets are:</span></span>
    - <span data-ttu-id="733df-126">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="733df-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="733df-127">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="733df-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="733df-128">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="733df-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="733df-129">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="733df-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="733df-130">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-131">Az.KeyVault</span></span>
* <span data-ttu-id="733df-132">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="733df-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="733df-133">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="733df-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="733df-134">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="733df-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="733df-135">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="733df-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="733df-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="733df-136">Az.Maintenance</span></span>
* <span data-ttu-id="733df-137">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="733df-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-138">Az.Monitor</span></span>
* <span data-ttu-id="733df-139">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="733df-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="733df-140">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="733df-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="733df-141">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="733df-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="733df-142">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="733df-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="733df-143">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="733df-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="733df-144">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="733df-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="733df-145">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="733df-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="733df-146">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="733df-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-147">Az.Network</span></span>
* <span data-ttu-id="733df-148">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="733df-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="733df-149">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="733df-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="733df-150">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="733df-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="733df-151">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="733df-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="733df-152">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="733df-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="733df-153">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="733df-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="733df-154">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="733df-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="733df-155">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="733df-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="733df-156">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="733df-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="733df-157">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="733df-158">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="733df-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="733df-159">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="733df-160">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="733df-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="733df-161">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="733df-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="733df-162">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="733df-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="733df-163">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="733df-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="733df-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="733df-165">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="733df-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="733df-166">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="733df-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-168">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="733df-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-169">Az.Sql</span></span>
* <span data-ttu-id="733df-170">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="733df-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="733df-171">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="733df-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-172">Az.Storage</span></span>
* <span data-ttu-id="733df-173">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="733df-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="733df-174">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="733df-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="733df-175">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="733df-176">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="733df-177">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="733df-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="733df-178">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="733df-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="733df-179">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="733df-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="733df-180">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="733df-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="733df-181">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="733df-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="733df-182">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="733df-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="733df-183">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="733df-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="733df-184">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="733df-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="733df-185">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="733df-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="733df-186">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="733df-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="733df-187">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="733df-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-188">Az.Accounts</span></span>
* <span data-ttu-id="733df-189">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="733df-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-190">Az.Compute</span></span>
* <span data-ttu-id="733df-191">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="733df-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="733df-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="733df-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="733df-193">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="733df-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="733df-194">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="733df-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="733df-195">[11354]</span><span class="sxs-lookup"><span data-stu-id="733df-195">[#11354]</span></span>
* <span data-ttu-id="733df-196">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="733df-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="733df-197">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="733df-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="733df-198">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="733df-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="733df-199">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="733df-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="733df-200">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="733df-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="733df-201">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="733df-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="733df-202">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="733df-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="733df-203">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="733df-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="733df-204">[11257]</span><span class="sxs-lookup"><span data-stu-id="733df-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-205">Az.DataFactory</span></span>
* <span data-ttu-id="733df-206">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="733df-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="733df-207">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="733df-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-209">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="733df-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="733df-210">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="733df-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="733df-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="733df-211">Az.HDInsight</span></span>
* <span data-ttu-id="733df-212">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="733df-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-213">Az.IotHub</span></span>
* <span data-ttu-id="733df-214">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="733df-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="733df-215">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="733df-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="733df-216">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="733df-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="733df-217">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="733df-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-218">Az.KeyVault</span></span>
* <span data-ttu-id="733df-219">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="733df-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-220">Az.Monitor</span></span>
* <span data-ttu-id="733df-221">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="733df-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-222">Az.Network</span></span>
* <span data-ttu-id="733df-223">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="733df-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="733df-224">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="733df-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="733df-225">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="733df-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="733df-226">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="733df-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="733df-227">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="733df-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="733df-228">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="733df-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="733df-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="733df-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="733df-230">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="733df-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-232">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="733df-233">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="733df-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="733df-234">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="733df-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="733df-235">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="733df-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="733df-236">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="733df-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="733df-237">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="733df-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-238">Az.Resources</span></span>
* <span data-ttu-id="733df-239">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="733df-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="733df-240">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="733df-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="733df-241">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="733df-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="733df-242">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="733df-242">Added example.</span></span>
* <span data-ttu-id="733df-243">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="733df-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="733df-244">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="733df-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-245">Az.Sql</span></span>
* <span data-ttu-id="733df-246">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="733df-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="733df-247">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="733df-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="733df-248">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="733df-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="733df-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="733df-249">Az.Support</span></span>
* <span data-ttu-id="733df-250">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="733df-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-251">Az.Websites</span></span>
* <span data-ttu-id="733df-252">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="733df-253">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="733df-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="733df-254">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="733df-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="733df-255">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="733df-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="733df-256">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="733df-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="733df-257">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="733df-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-258">Az.Accounts</span></span>
* <span data-ttu-id="733df-259">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="733df-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="733df-260">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="733df-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="733df-261">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="733df-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="733df-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-262">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-263">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="733df-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="733df-264">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="733df-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="733df-265">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="733df-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="733df-266">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="733df-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-268">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="733df-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-269">Az.IotHub</span></span>
* <span data-ttu-id="733df-270">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="733df-271">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="733df-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="733df-272">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="733df-273">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="733df-274">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="733df-275">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="733df-276">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="733df-277">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="733df-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="733df-278">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="733df-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="733df-279">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="733df-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="733df-280">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="733df-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="733df-281">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="733df-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="733df-282">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="733df-283">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="733df-284">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="733df-285">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="733df-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="733df-286">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="733df-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="733df-287">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="733df-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="733df-288">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="733df-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-289">Az.Monitor</span></span>
* <span data-ttu-id="733df-290">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="733df-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-291">Az.Network</span></span>
* <span data-ttu-id="733df-292">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="733df-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="733df-293">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="733df-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="733df-294">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="733df-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="733df-295">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="733df-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-296">Az.Resources</span></span>
* <span data-ttu-id="733df-297">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="733df-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="733df-298">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="733df-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="733df-299">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="733df-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="733df-300">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="733df-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="733df-301">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="733df-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="733df-302">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="733df-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="733df-303">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="733df-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="733df-304">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="733df-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="733df-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="733df-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="733df-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="733df-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="733df-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="733df-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="733df-308">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="733df-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="733df-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="733df-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="733df-310">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="733df-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-311">Az.Sql</span></span>
* <span data-ttu-id="733df-312">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="733df-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="733df-313">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="733df-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="733df-314">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="733df-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="733df-315">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="733df-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="733df-316">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="733df-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="733df-317">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="733df-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="733df-318">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="733df-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="733df-319">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="733df-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="733df-320">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="733df-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-321">Az.Storage</span></span>
* <span data-ttu-id="733df-322">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="733df-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="733df-323">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="733df-324">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="733df-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="733df-325">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="733df-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="733df-326">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="733df-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-327">Az.Websites</span></span>
* <span data-ttu-id="733df-328">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="733df-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="733df-329">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="733df-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="733df-330">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="733df-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="733df-331">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="733df-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="733df-332">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="733df-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="733df-333">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="733df-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="733df-334">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="733df-334">Highlights since the last major release</span></span>
* <span data-ttu-id="733df-335">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="733df-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="733df-336">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="733df-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="733df-337">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="733df-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-338">Az.Accounts</span></span>
* <span data-ttu-id="733df-339">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="733df-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-340">Az.Automation</span></span>
* <span data-ttu-id="733df-341">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-343">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="733df-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="733df-344">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="733df-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-345">Az.Compute</span></span>
* <span data-ttu-id="733df-346">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="733df-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="733df-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="733df-347">Az.FrontDoor</span></span>
* <span data-ttu-id="733df-348">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="733df-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-349">Az.IotHub</span></span>
* <span data-ttu-id="733df-350">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="733df-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="733df-351">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="733df-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="733df-352">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="733df-353">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="733df-354">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="733df-355">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="733df-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-356">Az.KeyVault</span></span>
* <span data-ttu-id="733df-357">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="733df-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-358">Az.Monitor</span></span>
* <span data-ttu-id="733df-359">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="733df-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="733df-360">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="733df-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="733df-361">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="733df-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-362">Az.Network</span></span>
* <span data-ttu-id="733df-363">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="733df-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="733df-364">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="733df-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="733df-365">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="733df-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="733df-366">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="733df-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="733df-367">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="733df-367">No new cmdlets are added.</span></span> <span data-ttu-id="733df-368">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="733df-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-370">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="733df-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-371">Az.Resources</span></span>
* <span data-ttu-id="733df-372">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="733df-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="733df-373">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="733df-374">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="733df-375">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="733df-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="733df-376">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="733df-377">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="733df-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="733df-378">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="733df-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="733df-379">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="733df-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-380">Az.Sql</span></span>
* <span data-ttu-id="733df-381">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="733df-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="733df-382">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="733df-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="733df-383">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="733df-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="733df-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="733df-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="733df-385">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="733df-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="733df-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="733df-386">Az.StorageSync</span></span>
* <span data-ttu-id="733df-387">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="733df-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="733df-388">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="733df-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="733df-389">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="733df-389">Highlights since the last major release</span></span>
* <span data-ttu-id="733df-390">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="733df-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="733df-391">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="733df-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-392">Az.Accounts</span></span>
* <span data-ttu-id="733df-393">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="733df-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="733df-394">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="733df-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="733df-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-395">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-396">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="733df-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="733df-397">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="733df-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="733df-398">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="733df-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="733df-399">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="733df-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-400">Az.Compute</span></span>
* <span data-ttu-id="733df-401">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="733df-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="733df-402">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="733df-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="733df-403">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="733df-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="733df-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="733df-405">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-406">Az.DataFactory</span></span>
* <span data-ttu-id="733df-407">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="733df-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="733df-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="733df-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="733df-409">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="733df-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="733df-410">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="733df-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="733df-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="733df-411">Az.HDInsight</span></span>
* <span data-ttu-id="733df-412">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="733df-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-413">Az.KeyVault</span></span>
* <span data-ttu-id="733df-414">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="733df-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-415">Az.Network</span></span>
* <span data-ttu-id="733df-416">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="733df-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="733df-417">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="733df-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="733df-418">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="733df-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="733df-419">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="733df-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="733df-420">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="733df-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="733df-421">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="733df-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="733df-422">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="733df-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="733df-423">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="733df-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="733df-424">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-424">New cmdlets added:</span></span>
        - <span data-ttu-id="733df-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="733df-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="733df-426">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="733df-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="733df-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="733df-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="733df-428">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="733df-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="733df-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="733df-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="733df-430">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="733df-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="733df-431">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="733df-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="733df-432">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="733df-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="733df-433">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="733df-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-435">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="733df-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="733df-436">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="733df-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-437">Az.Resources</span></span>
* <span data-ttu-id="733df-438">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="733df-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="733df-439">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="733df-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-440">Az.Sql</span></span>
<span data-ttu-id="733df-441">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="733df-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-442">Az.Storage</span></span>
* <span data-ttu-id="733df-443">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="733df-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="733df-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="733df-445">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="733df-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="733df-446">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="733df-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-447">Az.Websites</span></span>
* <span data-ttu-id="733df-448">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="733df-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="733df-449">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="733df-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="733df-450">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="733df-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-451">Az.Accounts</span></span>
* <span data-ttu-id="733df-452">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="733df-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="733df-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-453">Az.Cdn</span></span>
* <span data-ttu-id="733df-454">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="733df-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-455">Az.Compute</span></span>
* <span data-ttu-id="733df-456">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="733df-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="733df-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="733df-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="733df-458">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="733df-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="733df-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="733df-460">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="733df-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="733df-461">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="733df-462">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="733df-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="733df-463">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="733df-464">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="733df-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="733df-465">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="733df-466">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="733df-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="733df-467">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="733df-468">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="733df-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="733df-469">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="733df-470">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="733df-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="733df-471">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="733df-472">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="733df-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="733df-473">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="733df-474">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="733df-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="733df-475">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="733df-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="733df-476">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="733df-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="733df-477">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="733df-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-478">Az.DataFactory</span></span>
* <span data-ttu-id="733df-479">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="733df-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="733df-480">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="733df-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="733df-481">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="733df-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="733df-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="733df-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="733df-483">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="733df-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="733df-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="733df-484">Az.EventHub</span></span>
* <span data-ttu-id="733df-485">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="733df-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="733df-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="733df-486">Az.HDInsight</span></span>
* <span data-ttu-id="733df-487">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="733df-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="733df-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="733df-488">Az.MachineLearning</span></span>
* <span data-ttu-id="733df-489">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="733df-490">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="733df-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="733df-491">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="733df-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="733df-492">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="733df-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="733df-493">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="733df-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="733df-494">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="733df-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="733df-495">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="733df-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="733df-496">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="733df-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-497">Az.Network</span></span>
* <span data-ttu-id="733df-498">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="733df-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-500">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="733df-501">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="733df-502">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="733df-503">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-504">Az.Resources</span></span>
* <span data-ttu-id="733df-505">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="733df-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-506">Az.Sql</span></span>
* <span data-ttu-id="733df-507">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="733df-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="733df-508">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="733df-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="733df-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="733df-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="733df-510">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="733df-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-511">Az.Storage</span></span>
* <span data-ttu-id="733df-512">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="733df-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="733df-513">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="733df-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="733df-514">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="733df-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="733df-515">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="733df-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="733df-516">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="733df-517">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="733df-517">General</span></span>
* <span data-ttu-id="733df-518">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="733df-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-519">Az.Accounts</span></span>
* <span data-ttu-id="733df-520">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="733df-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="733df-521">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="733df-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="733df-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="733df-522">Az.Batch</span></span>
* <span data-ttu-id="733df-523">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="733df-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-524">Az.DataFactory</span></span>
* <span data-ttu-id="733df-525">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="733df-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="733df-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="733df-526">Az.FrontDoor</span></span>
* <span data-ttu-id="733df-527">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="733df-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="733df-528">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="733df-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="733df-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="733df-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="733df-530">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="733df-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-531">Az.KeyVault</span></span>
* <span data-ttu-id="733df-532">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="733df-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="733df-533">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="733df-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="733df-534">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="733df-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-535">Az.Monitor</span></span>
* <span data-ttu-id="733df-536">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="733df-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="733df-537">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="733df-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="733df-538">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="733df-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-539">Az.Network</span></span>
* <span data-ttu-id="733df-540">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="733df-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-541">Az.Resources</span></span>
* <span data-ttu-id="733df-542">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="733df-543">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="733df-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-544">Az.Sql</span></span>
* <span data-ttu-id="733df-545">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="733df-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-546">Az.Storage</span></span>
* <span data-ttu-id="733df-547">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="733df-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="733df-548">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="733df-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="733df-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="733df-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="733df-550">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="733df-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="733df-551">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="733df-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="733df-552">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="733df-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="733df-553">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="733df-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="733df-554">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="733df-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="733df-555">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="733df-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="733df-556">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="733df-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="733df-557">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="733df-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="733df-558">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="733df-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="733df-559">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="733df-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="733df-560">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="733df-561">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="733df-561">Highlights since the last major release</span></span>
* <span data-ttu-id="733df-562">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="733df-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="733df-563">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="733df-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-564">Az.Compute</span></span>
* <span data-ttu-id="733df-565">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="733df-565">VM Reapply feature</span></span>
    - <span data-ttu-id="733df-566">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="733df-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="733df-567">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="733df-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="733df-568">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="733df-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="733df-569">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="733df-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="733df-570">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="733df-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="733df-571">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="733df-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="733df-572">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="733df-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="733df-573">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="733df-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="733df-574">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="733df-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="733df-575">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="733df-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="733df-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="733df-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="733df-577">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="733df-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="733df-578">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="733df-578">Get the Order</span></span>
* <span data-ttu-id="733df-579">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="733df-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="733df-580">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="733df-580">Create new Order</span></span>
* <span data-ttu-id="733df-581">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="733df-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="733df-582">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="733df-582">Remove the Order</span></span>
* <span data-ttu-id="733df-583">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="733df-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="733df-584">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="733df-584">Now creates Local Share</span></span>
* <span data-ttu-id="733df-585">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="733df-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="733df-586">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="733df-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="733df-587">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="733df-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="733df-588">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="733df-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="733df-589">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="733df-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="733df-590">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="733df-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="733df-591">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="733df-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="733df-592">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="733df-592">Create new Triggers</span></span>
* <span data-ttu-id="733df-593">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="733df-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="733df-594">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="733df-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-595">Az.DataFactory</span></span>
* <span data-ttu-id="733df-596">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="733df-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="733df-597">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="733df-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-599">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="733df-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="733df-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="733df-600">Az.EventHub</span></span>
* <span data-ttu-id="733df-601">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="733df-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="733df-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="733df-602">Az.FrontDoor</span></span>
* <span data-ttu-id="733df-603">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="733df-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="733df-604">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="733df-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="733df-605">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="733df-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="733df-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="733df-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-607">Az.Network</span></span>
* <span data-ttu-id="733df-608">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="733df-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="733df-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="733df-609">Az.PrivateDns</span></span>
* <span data-ttu-id="733df-610">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="733df-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-612">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="733df-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="733df-613">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="733df-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="733df-614">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="733df-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="733df-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="733df-615">Az.RedisCache</span></span>
* <span data-ttu-id="733df-616">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="733df-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="733df-617">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="733df-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="733df-618">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="733df-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-619">Az.Resources</span></span>
- <span data-ttu-id="733df-620">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="733df-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="733df-621">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="733df-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="733df-622">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="733df-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="733df-623">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="733df-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="733df-624">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="733df-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-625">Az.Sql</span></span>
* <span data-ttu-id="733df-626">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="733df-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="733df-627">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="733df-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="733df-628">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="733df-629">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="733df-629">General</span></span>
* <span data-ttu-id="733df-630">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="733df-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-631">Az.Accounts</span></span>
* <span data-ttu-id="733df-632">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="733df-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="733df-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="733df-633">Az.Advisor</span></span>
* <span data-ttu-id="733df-634">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="733df-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="733df-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="733df-635">Az.Batch</span></span>
* <span data-ttu-id="733df-636">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="733df-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="733df-637">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="733df-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="733df-638">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="733df-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="733df-639">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="733df-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="733df-640">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="733df-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="733df-641">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="733df-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="733df-642">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="733df-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="733df-643">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="733df-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="733df-644">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="733df-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="733df-645">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="733df-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="733df-646">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="733df-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="733df-647">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="733df-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="733df-648">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="733df-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="733df-649">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="733df-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="733df-650">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="733df-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="733df-651">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="733df-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="733df-652">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="733df-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="733df-653">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="733df-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="733df-654">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="733df-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="733df-655">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="733df-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="733df-656">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="733df-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="733df-657">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="733df-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="733df-658">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="733df-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="733df-659">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="733df-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="733df-660">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="733df-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="733df-661">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="733df-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="733df-662">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="733df-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="733df-663">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="733df-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="733df-664">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="733df-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="733df-665">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="733df-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="733df-666">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="733df-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="733df-667">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="733df-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="733df-668">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="733df-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="733df-669">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="733df-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="733df-670">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="733df-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="733df-671">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="733df-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="733df-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-672">Az.Cdn</span></span>
* <span data-ttu-id="733df-673">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="733df-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="733df-674">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="733df-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-675">Az.Compute</span></span>
* <span data-ttu-id="733df-676">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="733df-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="733df-677">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="733df-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="733df-678">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="733df-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="733df-679">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="733df-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="733df-680">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="733df-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="733df-681">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="733df-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="733df-682">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="733df-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="733df-683">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="733df-683">Breaking changes</span></span>
    - <span data-ttu-id="733df-684">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="733df-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="733df-685">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="733df-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-686">Az.DataFactory</span></span>
* <span data-ttu-id="733df-687">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="733df-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-689">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="733df-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="733df-690">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="733df-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="733df-691">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="733df-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="733df-692">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="733df-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="733df-693">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="733df-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="733df-694">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="733df-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="733df-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="733df-695">Az.FrontDoor</span></span>
* <span data-ttu-id="733df-696">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="733df-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="733df-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="733df-697">Az.HDInsight</span></span>
* <span data-ttu-id="733df-698">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="733df-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="733df-699">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="733df-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="733df-700">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="733df-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="733df-701">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="733df-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="733df-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="733df-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="733df-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="733df-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="733df-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="733df-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="733df-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="733df-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="733df-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="733df-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="733df-707">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="733df-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="733df-708">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="733df-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="733df-709">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="733df-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="733df-710">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="733df-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="733df-711">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="733df-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="733df-712">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="733df-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="733df-713">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="733df-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="733df-714">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="733df-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="733df-715">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="733df-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="733df-716">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="733df-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="733df-717">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="733df-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="733df-718">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="733df-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="733df-719">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="733df-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-720">Az.IotHub</span></span>
* <span data-ttu-id="733df-721">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="733df-721">Breaking changes:</span></span>
    - <span data-ttu-id="733df-722">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="733df-723">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="733df-724">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="733df-725">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="733df-726">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="733df-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="733df-727">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="733df-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="733df-728">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="733df-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="733df-729">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="733df-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="733df-730">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="733df-731">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="733df-732">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="733df-733">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="733df-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-735">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="733df-736">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="733df-737">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="733df-738">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="733df-739">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="733df-740">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="733df-741">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="733df-742">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="733df-743">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="733df-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-744">Az.Resources</span></span>
* <span data-ttu-id="733df-745">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="733df-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-746">Az.Network</span></span>
* <span data-ttu-id="733df-747">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="733df-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="733df-748">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="733df-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="733df-749">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-750">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-751">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-752">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="733df-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="733df-754">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="733df-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="733df-755">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="733df-755">New cmdlet:</span></span>
        - <span data-ttu-id="733df-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="733df-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="733df-757">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="733df-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="733df-758">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="733df-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="733df-759">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="733df-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="733df-760">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="733df-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="733df-761">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="733df-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="733df-762">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="733df-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="733df-763">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="733df-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="733df-764">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-764">New cmdlets added:</span></span>
        - <span data-ttu-id="733df-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="733df-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="733df-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="733df-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="733df-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="733df-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="733df-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="733df-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="733df-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="733df-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="733df-770">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="733df-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="733df-771">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="733df-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="733df-772">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="733df-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="733df-773">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="733df-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="733df-774">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="733df-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="733df-775">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="733df-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="733df-776">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="733df-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="733df-777">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-777">New cmdlets added:</span></span>
        - <span data-ttu-id="733df-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="733df-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="733df-779">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="733df-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="733df-780">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="733df-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="733df-781">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="733df-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="733df-782">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="733df-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="733df-783">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="733df-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="733df-784">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="733df-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="733df-785">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="733df-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="733df-786">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-786">New cmdlets added:</span></span>
        - <span data-ttu-id="733df-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="733df-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="733df-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="733df-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="733df-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="733df-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="733df-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="733df-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="733df-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="733df-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="733df-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="733df-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="733df-793">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="733df-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="733df-794">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="733df-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="733df-795">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="733df-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="733df-796">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="733df-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="733df-797">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="733df-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="733df-798">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="733df-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="733df-799">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="733df-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="733df-800">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="733df-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="733df-801">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="733df-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="733df-802">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="733df-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="733df-803">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="733df-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="733df-804">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-804">New cmdlets added:</span></span>
        - <span data-ttu-id="733df-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="733df-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="733df-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="733df-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="733df-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="733df-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="733df-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="733df-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-810">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="733df-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-811">Az.Sql</span></span>
* <span data-ttu-id="733df-812">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="733df-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="733df-813">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="733df-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="733df-814">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="733df-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="733df-815">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="733df-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="733df-816">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="733df-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="733df-817">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="733df-818">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="733df-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="733df-819">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="733df-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="733df-820">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="733df-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-821">Az.Storage</span></span>
* <span data-ttu-id="733df-822">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="733df-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="733df-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="733df-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="733df-825">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="733df-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="733df-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="733df-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="733df-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="733df-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="733df-828">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="733df-829">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="733df-829">General</span></span>
* <span data-ttu-id="733df-830">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="733df-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-831">Az.Accounts</span></span>
* <span data-ttu-id="733df-832">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="733df-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="733df-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-833">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-834">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="733df-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="733df-835">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="733df-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-836">Az.Automation</span></span>
* <span data-ttu-id="733df-837">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="733df-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="733df-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="733df-838">Az.Batch</span></span>
* <span data-ttu-id="733df-839">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="733df-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-840">Az.Compute</span></span>
* <span data-ttu-id="733df-841">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="733df-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="733df-842">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="733df-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="733df-843">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="733df-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="733df-844">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="733df-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-845">Az.DataFactory</span></span>
* <span data-ttu-id="733df-846">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="733df-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="733df-847">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="733df-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="733df-848">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="733df-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-850">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="733df-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="733df-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="733df-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="733df-852">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="733df-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="733df-853">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="733df-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="733df-854">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="733df-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="733df-855">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="733df-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-856">Az.IotHub</span></span>
* <span data-ttu-id="733df-857">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="733df-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="733df-858">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="733df-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-859">Az.Monitor</span></span>
* <span data-ttu-id="733df-860">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="733df-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="733df-861">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="733df-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="733df-862">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="733df-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="733df-863">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="733df-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-864">Az.Network</span></span>
* <span data-ttu-id="733df-865">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="733df-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="733df-866">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="733df-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="733df-867">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-867">New cmdlets added:</span></span>
        - <span data-ttu-id="733df-868">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="733df-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="733df-869">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="733df-870">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="733df-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="733df-871">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="733df-872">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="733df-873">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="733df-874">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="733df-875">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="733df-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="733df-876">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="733df-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="733df-877">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="733df-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="733df-878">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="733df-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="733df-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="733df-879">Az.RedisCache</span></span>
* <span data-ttu-id="733df-880">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="733df-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-881">Az.Sql</span></span>
* <span data-ttu-id="733df-882">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="733df-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-883">Az.Storage</span></span>
* <span data-ttu-id="733df-884">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="733df-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="733df-885">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="733df-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="733df-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="733df-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="733df-887">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="733df-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="733df-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="733df-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="733df-889">Az.StorageSync</span></span>
* <span data-ttu-id="733df-890">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="733df-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-891">Az.Websites</span></span>
* <span data-ttu-id="733df-892">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="733df-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="733df-893">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="733df-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-894">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-895">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="733df-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="733df-896">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="733df-897">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="733df-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-898">Az.Automation</span></span>
* <span data-ttu-id="733df-899">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="733df-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="733df-900">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="733df-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="733df-901">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="733df-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-902">Az.Compute</span></span>
* <span data-ttu-id="733df-903">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="733df-904">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="733df-905">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="733df-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="733df-906">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="733df-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="733df-907">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="733df-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="733df-908">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="733df-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="733df-909">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="733df-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="733df-910">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="733df-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="733df-911">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="733df-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-912">Az.DataFactory</span></span>
* <span data-ttu-id="733df-913">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="733df-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="733df-914">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="733df-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="733df-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="733df-915">Az.HDInsight</span></span>
* <span data-ttu-id="733df-916">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="733df-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-917">Az.IotHub</span></span>
* <span data-ttu-id="733df-918">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="733df-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="733df-919">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="733df-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="733df-920">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-920">New cmdlets are:</span></span>
    - <span data-ttu-id="733df-921">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="733df-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="733df-922">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="733df-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="733df-923">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="733df-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="733df-924">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="733df-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-925">Az.Monitor</span></span>
* <span data-ttu-id="733df-926">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="733df-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="733df-927">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="733df-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="733df-928">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="733df-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="733df-929">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="733df-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="733df-930">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="733df-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="733df-931">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="733df-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="733df-932">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="733df-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="733df-933">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="733df-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="733df-934">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="733df-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="733df-935">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="733df-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="733df-936">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="733df-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="733df-937">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="733df-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="733df-938">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="733df-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="733df-939">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="733df-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="733df-940">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="733df-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="733df-941">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="733df-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="733df-942">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="733df-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="733df-943">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="733df-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="733df-944">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="733df-945">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="733df-945">Overall improved help files</span></span>
* <span data-ttu-id="733df-946">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="733df-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-947">Az.Network</span></span>
* <span data-ttu-id="733df-948">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="733df-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="733df-949">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="733df-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="733df-950">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="733df-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="733df-951">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="733df-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="733df-952">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="733df-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="733df-953">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="733df-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="733df-954">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="733df-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="733df-955">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="733df-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="733df-956">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="733df-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="733df-957">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="733df-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="733df-958">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="733df-959">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="733df-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="733df-960">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-960">New cmdlets</span></span>
        - <span data-ttu-id="733df-961">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="733df-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="733df-962">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="733df-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="733df-963">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="733df-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="733df-964">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="733df-964">New-VpnSite</span></span>
        - <span data-ttu-id="733df-965">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="733df-965">Update-VpnSite</span></span>
        - <span data-ttu-id="733df-966">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="733df-966">New-VpnConnection</span></span>
        - <span data-ttu-id="733df-967">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-967">Update-VpnConnection</span></span>
* <span data-ttu-id="733df-968">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="733df-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-970">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="733df-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="733df-971">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="733df-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-972">Az.Resources</span></span>
* <span data-ttu-id="733df-973">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="733df-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-975">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="733df-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="733df-976">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="733df-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="733df-977">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="733df-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="733df-978">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="733df-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="733df-979">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="733df-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="733df-980">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="733df-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="733df-981">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="733df-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="733df-982">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="733df-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="733df-983">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="733df-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="733df-984">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="733df-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="733df-985">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="733df-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="733df-986">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="733df-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="733df-987">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="733df-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="733df-988">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="733df-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="733df-989">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="733df-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="733df-990">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="733df-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="733df-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="733df-991">Az.SignalR</span></span>
* <span data-ttu-id="733df-992">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="733df-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-993">Az.Sql</span></span>
* <span data-ttu-id="733df-994">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="733df-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="733df-995">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="733df-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="733df-996">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="733df-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="733df-997">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="733df-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="733df-998">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="733df-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-999">Az.Storage</span></span>
* <span data-ttu-id="733df-1000">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="733df-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="733df-1001">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="733df-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="733df-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="733df-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="733df-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="733df-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="733df-1004">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="733df-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="733df-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="733df-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="733df-1006">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="733df-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="733df-1007">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="733df-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="733df-1008">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="733df-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="733df-1009">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="733df-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="733df-1010">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="733df-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1011">Az.Websites</span></span>
* <span data-ttu-id="733df-1012">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="733df-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="733df-1013">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="733df-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="733df-1014">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="733df-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="733df-1015">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="733df-1016">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="733df-1016">General</span></span>
* <span data-ttu-id="733df-1017">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="733df-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1018">Az.Accounts</span></span>
* <span data-ttu-id="733df-1019">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="733df-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="733df-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="733df-1020">Az.Aks</span></span>
* <span data-ttu-id="733df-1021">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="733df-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="733df-1022">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="733df-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="733df-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-1024">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="733df-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="733df-1025">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="733df-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="733df-1026">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="733df-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="733df-1027">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="733df-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="733df-1028">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="733df-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="733df-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="733df-1029">Az.Batch</span></span>
* <span data-ttu-id="733df-1030">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="733df-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="733df-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-1031">Az.Cdn</span></span>
* <span data-ttu-id="733df-1032">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="733df-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1033">Az.Compute</span></span>
* <span data-ttu-id="733df-1034">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="733df-1035">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="733df-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="733df-1036">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="733df-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="733df-1037">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="733df-1038">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="733df-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="733df-1039">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="733df-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="733df-1040">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="733df-1041">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="733df-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-1042">Az.DataFactory</span></span>
* <span data-ttu-id="733df-1043">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="733df-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="733df-1044">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="733df-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="733df-1045">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="733df-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="733df-1046">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="733df-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-1048">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="733df-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="733df-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="733df-1049">Az.EventHub</span></span>
* <span data-ttu-id="733df-1050">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="733df-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="733df-1051">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="733df-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="733df-1052">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="733df-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="733df-1053">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="733df-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="733df-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="733df-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="733df-1055">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="733df-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-1056">Az.Monitor</span></span>
* <span data-ttu-id="733df-1057">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="733df-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1058">Az.Network</span></span>
* <span data-ttu-id="733df-1059">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="733df-1060">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="733df-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="733df-1061">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="733df-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="733df-1062">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="733df-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="733df-1063">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="733df-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="733df-1064">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="733df-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="733df-1065">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="733df-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="733df-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="733df-1067">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="733df-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="733df-1068">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="733df-1068">Added example</span></span>
    - <span data-ttu-id="733df-1069">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="733df-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="733df-1070">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="733df-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="733df-1071">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="733df-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1073">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1074">Az.Resources</span></span>
* <span data-ttu-id="733df-1075">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="733df-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="733df-1076">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="733df-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="733df-1077">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="733df-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="733df-1078">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="733df-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="733df-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="733df-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="733df-1080">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="733df-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="733df-1081">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="733df-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="733df-1082">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="733df-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-1084">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="733df-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="733df-1085">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="733df-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="733df-1086">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="733df-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="733df-1087">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="733df-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="733df-1088">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="733df-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="733df-1089">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="733df-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1090">Az.Sql</span></span>
* <span data-ttu-id="733df-1091">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="733df-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1092">Az.Storage</span></span>
* <span data-ttu-id="733df-1093">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="733df-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="733df-1094">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="733df-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="733df-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="733df-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="733df-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="733df-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="733df-1097">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="733df-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="733df-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="733df-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1099">Az.Websites</span></span>
* <span data-ttu-id="733df-1100">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="733df-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="733df-1101">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1102">Az.Accounts</span></span>
* <span data-ttu-id="733df-1103">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="733df-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="733df-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="733df-1105">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="733df-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1106">Az.Automation</span></span>
* <span data-ttu-id="733df-1107">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="733df-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-1109">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="733df-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1110">Az.Compute</span></span>
* <span data-ttu-id="733df-1111">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="733df-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="733df-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="733df-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="733df-1113">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="733df-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="733df-1114">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="733df-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-1115">Az.DataFactory</span></span>
* <span data-ttu-id="733df-1116">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="733df-1117">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="733df-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="733df-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="733df-1118">Az.EventHub</span></span>
* <span data-ttu-id="733df-1119">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="733df-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="733df-1120">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="733df-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-1121">Az.KeyVault</span></span>
* <span data-ttu-id="733df-1122">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="733df-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="733df-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="733df-1123">Az.LogicApp</span></span>
* <span data-ttu-id="733df-1124">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="733df-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="733df-1125">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="733df-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="733df-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="733df-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="733df-1127">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="733df-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1128">Az.Network</span></span>
* <span data-ttu-id="733df-1129">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="733df-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="733df-1130">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1130">New cmdlets</span></span>
        - <span data-ttu-id="733df-1131">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="733df-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="733df-1132">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="733df-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="733df-1133">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-1134">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-1135">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-1136">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="733df-1137">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="733df-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="733df-1138">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="733df-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="733df-1139">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="733df-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="733df-1140">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="733df-1141">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="733df-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="733df-1142">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="733df-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="733df-1143">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="733df-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="733df-1144">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="733df-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="733df-1145">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="733df-1146">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="733df-1147">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="733df-1148">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="733df-1149">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="733df-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="733df-1150">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="733df-1151">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="733df-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="733df-1152">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="733df-1153">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="733df-1154">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="733df-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="733df-1155">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="733df-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="733df-1156">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="733df-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="733df-1157">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="733df-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="733df-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="733df-1159">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="733df-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="733df-1160">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="733df-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1162">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="733df-1163">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="733df-1164">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="733df-1165">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="733df-1166">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="733df-1167">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="733df-1168">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="733df-1169">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="733df-1170">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="733df-1171">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="733df-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1172">Az.Resources</span></span>
- <span data-ttu-id="733df-1173">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="733df-1174">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="733df-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="733df-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="733df-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="733df-1176">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="733df-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="733df-1177">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="733df-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1178">Az.Sql</span></span>
* <span data-ttu-id="733df-1179">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="733df-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="733df-1180">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="733df-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="733df-1181">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="733df-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1182">Az.Storage</span></span>
* <span data-ttu-id="733df-1183">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="733df-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="733df-1184">Az.StorageSync</span></span>
* <span data-ttu-id="733df-1185">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="733df-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="733df-1186">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="733df-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1187">Az.Websites</span></span>
* <span data-ttu-id="733df-1188">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="733df-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="733df-1189">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="733df-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="733df-1190">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="733df-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="733df-1191">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1192">Az.Accounts</span></span>
* <span data-ttu-id="733df-1193">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="733df-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="733df-1194">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="733df-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="733df-1195">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="733df-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="733df-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="733df-1196">Az.Advisor</span></span>
* <span data-ttu-id="733df-1197">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="733df-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="733df-1198">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="733df-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="733df-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-1200">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="733df-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="733df-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="733df-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="733df-1202">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="733df-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="733df-1203">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="733df-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="733df-1204">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="733df-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="733df-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="733df-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="733df-1206">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="733df-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1207">Az.Automation</span></span>
* <span data-ttu-id="733df-1208">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="733df-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1209">Az.Compute</span></span>
* <span data-ttu-id="733df-1210">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="733df-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-1211">Az.DataFactory</span></span>
* <span data-ttu-id="733df-1212">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="733df-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="733df-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="733df-1213">Az.EventGrid</span></span>
* <span data-ttu-id="733df-1214">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="733df-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-1215">Az.IotHub</span></span>
* <span data-ttu-id="733df-1216">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="733df-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1217">Az.Network</span></span>
* <span data-ttu-id="733df-1218">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="733df-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="733df-1219">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="733df-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="733df-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="733df-1221">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="733df-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="733df-1222">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="733df-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="733df-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="733df-1224">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="733df-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1226">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="733df-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1227">Az.Resources</span></span>
    - <span data-ttu-id="733df-1228">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="733df-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="733df-1229">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="733df-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="733df-1230">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="733df-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="733df-1231">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="733df-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="733df-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="733df-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="733df-1233">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="733df-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1234">Az.Sql</span></span>
* <span data-ttu-id="733df-1235">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="733df-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="733df-1236">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="733df-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="733df-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="733df-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="733df-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="733df-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="733df-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="733df-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="733df-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="733df-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="733df-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="733df-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="733df-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="733df-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="733df-1243">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="733df-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1244">Az.Storage</span></span>
* <span data-ttu-id="733df-1245">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="733df-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="733df-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="733df-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="733df-1247">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="733df-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="733df-1248">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="733df-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="733df-1249">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="733df-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="733df-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="733df-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="733df-1252">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="733df-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="733df-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="733df-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="733df-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="733df-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="733df-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="733df-1255">Az.StorageSync</span></span>
* <span data-ttu-id="733df-1256">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="733df-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="733df-1257">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1258">Az.Accounts</span></span>
* <span data-ttu-id="733df-1259">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="733df-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="733df-1260">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="733df-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="733df-1261">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="733df-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="733df-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="733df-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="733df-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="733df-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1264">Az.Compute</span></span>
* <span data-ttu-id="733df-1265">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="733df-1266">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="733df-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="733df-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="733df-1267">Az.Dns</span></span>
* <span data-ttu-id="733df-1268">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="733df-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="733df-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="733df-1269">Az.EventGrid</span></span>
* <span data-ttu-id="733df-1270">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="733df-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="733df-1271">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-1271">New cmdlets:</span></span>
    - <span data-ttu-id="733df-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="733df-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="733df-1273">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="733df-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="733df-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="733df-1275">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="733df-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="733df-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="733df-1277">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="733df-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="733df-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="733df-1279">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="733df-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="733df-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="733df-1281">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="733df-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="733df-1282">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="733df-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="733df-1283">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="733df-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="733df-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="733df-1285">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="733df-1286">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="733df-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="733df-1287">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="733df-1288">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="733df-1289">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="733df-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="733df-1290">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="733df-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="733df-1291">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="733df-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="733df-1292">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="733df-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="733df-1293">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="733df-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="733df-1294">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="733df-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="733df-1295">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="733df-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="733df-1296">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="733df-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="733df-1297">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="733df-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="733df-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="733df-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="733df-1299">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="733df-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="733df-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="733df-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="733df-1301">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="733df-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="733df-1302">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="733df-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="733df-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="733df-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="733df-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="733df-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="733df-1305">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="733df-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="733df-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="733df-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="733df-1307">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="733df-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1308">Az.Network</span></span>
* <span data-ttu-id="733df-1309">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="733df-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="733df-1310">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1310">New cmdlets</span></span>
        - <span data-ttu-id="733df-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="733df-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="733df-1312">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="733df-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="733df-1313">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1313">New cmdlets</span></span>
        - <span data-ttu-id="733df-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="733df-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="733df-1315">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="733df-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="733df-1316">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1316">New cmdlets</span></span>
        - <span data-ttu-id="733df-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="733df-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="733df-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="733df-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="733df-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="733df-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="733df-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="733df-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="733df-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="733df-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="733df-1322">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="733df-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="733df-1323">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1323">New cmdlets</span></span>
        - <span data-ttu-id="733df-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="733df-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="733df-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="733df-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="733df-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="733df-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="733df-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="733df-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="733df-1328">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="733df-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="733df-1329">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="733df-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="733df-1330">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="733df-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="733df-1331">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="733df-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="733df-1332">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="733df-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="733df-1333">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="733df-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="733df-1334">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="733df-1335">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="733df-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="733df-1336">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="733df-1337">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="733df-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="733df-1338">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="733df-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="733df-1339">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="733df-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="733df-1340">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="733df-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="733df-1341">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="733df-1342">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="733df-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="733df-1343">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="733df-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="733df-1344">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="733df-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="733df-1345">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="733df-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="733df-1346">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="733df-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="733df-1347">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="733df-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="733df-1348">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="733df-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="733df-1349">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="733df-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="733df-1350">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="733df-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="733df-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="733df-1352">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="733df-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1353">Az.Resources</span></span>
* <span data-ttu-id="733df-1354">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="733df-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="733df-1355">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="733df-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="733df-1356">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="733df-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="733df-1357">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="733df-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-1359">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="733df-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1360">Az.Sql</span></span>
* <span data-ttu-id="733df-1361">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="733df-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="733df-1362">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="733df-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="733df-1363">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="733df-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="733df-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="733df-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="733df-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="733df-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="733df-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="733df-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="733df-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="733df-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="733df-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="733df-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1369">Az.Storage</span></span>
* <span data-ttu-id="733df-1370">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="733df-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="733df-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="733df-1372">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="733df-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="733df-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1374">Az.Websites</span></span>
* <span data-ttu-id="733df-1375">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="733df-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="733df-1376">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="733df-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="733df-1377">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="733df-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-1378">Az.Cdn</span></span>
* <span data-ttu-id="733df-1379">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="733df-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1380">Az.Compute</span></span>
* <span data-ttu-id="733df-1381">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="733df-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="733df-1382">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="733df-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="733df-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="733df-1383">Az.EventHub</span></span>
* <span data-ttu-id="733df-1384">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="733df-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="733df-1385">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="733df-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1386">Az.Network</span></span>
* <span data-ttu-id="733df-1387">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="733df-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="733df-1388">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="733df-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="733df-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="733df-1390">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="733df-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1392">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="733df-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="733df-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="733df-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="733df-1394">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="733df-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-1396">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="733df-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="733df-1397">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="733df-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1398">Az.Sql</span></span>
* <span data-ttu-id="733df-1399">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="733df-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="733df-1400">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="733df-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="733df-1401">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="733df-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="733df-1402">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="733df-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1403">Az.Websites</span></span>
* <span data-ttu-id="733df-1404">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="733df-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="733df-1405">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="733df-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-1407">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="733df-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="733df-1408">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="733df-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="733df-1409">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="733df-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="733df-1410">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="733df-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="733df-1411">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="733df-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="733df-1412">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="733df-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="733df-1413">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="733df-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="733df-1414">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="733df-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="733df-1415">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="733df-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="733df-1416">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="733df-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="733df-1417">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="733df-1418">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="733df-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="733df-1419">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="733df-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="733df-1420">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="733df-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="733df-1421">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="733df-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="733df-1422">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="733df-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="733df-1423">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="733df-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="733df-1424">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="733df-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="733df-1425">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="733df-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="733df-1426">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="733df-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="733df-1427">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="733df-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="733df-1428">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="733df-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="733df-1429">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="733df-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="733df-1430">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="733df-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="733df-1431">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="733df-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="733df-1432">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="733df-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="733df-1433">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="733df-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="733df-1434">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="733df-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="733df-1435">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="733df-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="733df-1436">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="733df-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="733df-1437">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="733df-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="733df-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="733df-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="733df-1439">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="733df-1440">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="733df-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="733df-1441">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="733df-1442">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="733df-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="733df-1443">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="733df-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="733df-1444">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="733df-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="733df-1445">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="733df-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="733df-1446">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="733df-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="733df-1447">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="733df-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="733df-1448">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="733df-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="733df-1449">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="733df-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="733df-1450">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="733df-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="733df-1451">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="733df-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="733df-1452">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="733df-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="733df-1453">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="733df-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="733df-1454">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="733df-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="733df-1455">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="733df-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="733df-1456">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="733df-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="733df-1457">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="733df-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="733df-1458">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="733df-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="733df-1459">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="733df-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="733df-1460">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="733df-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="733df-1461">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="733df-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="733df-1462">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="733df-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="733df-1463">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="733df-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="733df-1464">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="733df-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="733df-1465">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="733df-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="733df-1466">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="733df-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="733df-1467">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="733df-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="733df-1468">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="733df-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="733df-1469">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="733df-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="733df-1470">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="733df-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="733df-1471">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="733df-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="733df-1472">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="733df-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="733df-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="733df-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="733df-1474">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="733df-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="733df-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="733df-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="733df-1476">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="733df-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="733df-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="733df-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="733df-1478">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="733df-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="733df-1479">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="733df-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="733df-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="733df-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="733df-1481">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="733df-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="733df-1482">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="733df-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="733df-1483">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="733df-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1484">Az.Automation</span></span>
* <span data-ttu-id="733df-1485">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="733df-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="733df-1486">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="733df-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="733df-1487">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="733df-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="733df-1488">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="733df-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="733df-1489">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="733df-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="733df-1490">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="733df-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="733df-1491">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="733df-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1492">Az.Compute</span></span>
* <span data-ttu-id="733df-1493">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="733df-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="733df-1494">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="733df-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-1496">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="733df-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-1497">Az.Monitor</span></span>
* <span data-ttu-id="733df-1498">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="733df-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1499">Az.Network</span></span>
* <span data-ttu-id="733df-1500">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="733df-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="733df-1501">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="733df-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="733df-1502">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="733df-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="733df-1503">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="733df-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1504">Az.Resources</span></span>
* <span data-ttu-id="733df-1505">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="733df-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1506">Az.Sql</span></span>
* <span data-ttu-id="733df-1507">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="733df-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="733df-1508">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1509">Az.Accounts</span></span>
* <span data-ttu-id="733df-1510">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="733df-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-1512">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="733df-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="733df-1513">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="733df-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1514">Az.Compute</span></span>
* <span data-ttu-id="733df-1515">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="733df-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="733df-1516">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="733df-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="733df-1517">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="733df-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="733df-1518">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="733df-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="733df-1519">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="733df-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="733df-1520">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="733df-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="733df-1521">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="733df-1521">Breaking changes</span></span>
    - <span data-ttu-id="733df-1522">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="733df-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="733df-1523">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="733df-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="733df-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="733df-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="733df-1525">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="733df-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="733df-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="733df-1526">Az.Dns</span></span>
* <span data-ttu-id="733df-1527">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="733df-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="733df-1528">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="733df-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="733df-1529">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="733df-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="733df-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="733df-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="733df-1531">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="733df-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="733df-1532">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="733df-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="733df-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="733df-1533">Az.HDInsight</span></span>
* <span data-ttu-id="733df-1534">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="733df-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="733df-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="733df-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="733df-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="733df-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="733df-1537">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="733df-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="733df-1538">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="733df-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="733df-1539">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="733df-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="733df-1540">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="733df-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-1541">Az.Monitor</span></span>
* <span data-ttu-id="733df-1542">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="733df-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="733df-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="733df-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="733df-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="733df-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="733df-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="733df-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="733df-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="733df-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="733df-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="733df-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="733df-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="733df-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="733df-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="733df-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="733df-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="733df-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="733df-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="733df-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="733df-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="733df-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="733df-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="733df-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="733df-1554">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="733df-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="733df-1555">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="733df-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1556">Az.Network</span></span>
* <span data-ttu-id="733df-1557">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="733df-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="733df-1558">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1558">New cmdlets</span></span>
        - <span data-ttu-id="733df-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="733df-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="733df-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="733df-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="733df-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="733df-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="733df-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="733df-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="733df-1563">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="733df-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="733df-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="733df-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="733df-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="733df-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="733df-1566">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="733df-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="733df-1567">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="733df-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="733df-1568">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="733df-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="733df-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="733df-1570">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="733df-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="733df-1571">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="733df-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="733df-1572">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="733df-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1574">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="733df-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="733df-1575">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="733df-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="733df-1576">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="733df-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="733df-1577">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="733df-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="733df-1578">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="733df-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="733df-1579">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="733df-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="733df-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="733df-1580">Az.Relay</span></span>
* <span data-ttu-id="733df-1581">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="733df-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="733df-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="733df-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="733df-1583">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="733df-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1584">Az.Storage</span></span>
* <span data-ttu-id="733df-1585">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="733df-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="733df-1586">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="733df-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="733df-1587">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="733df-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="733df-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="733df-1589">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="733df-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="733df-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="733df-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="733df-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1593">Az.Websites</span></span>
* <span data-ttu-id="733df-1594">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="733df-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="733df-1595">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="733df-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="733df-1596">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="733df-1597">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="733df-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="733df-1598">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="733df-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="733df-1599">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="733df-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="733df-1600">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="733df-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="733df-1601">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="733df-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="733df-1602">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="733df-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="733df-1603">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="733df-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="733df-1604">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="733df-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1605">Az.Accounts</span></span>
* <span data-ttu-id="733df-1606">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="733df-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="733df-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="733df-1607">Az.Batch</span></span>
* <span data-ttu-id="733df-1608">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="733df-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-1609">Az.Cdn</span></span>
* <span data-ttu-id="733df-1610">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-1612">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1613">Az.Compute</span></span>
* <span data-ttu-id="733df-1614">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="733df-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="733df-1615">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="733df-1616">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="733df-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-1617">Az.DataFactory</span></span>
* <span data-ttu-id="733df-1618">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="733df-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-1620">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="733df-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="733df-1621">Az.EventGrid</span></span>
* <span data-ttu-id="733df-1622">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="733df-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="733df-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="733df-1623">Az.EventHub</span></span>
* <span data-ttu-id="733df-1624">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="733df-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="733df-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="733df-1625">Az.HDInsight</span></span>
* <span data-ttu-id="733df-1626">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-1627">Az.IotHub</span></span>
* <span data-ttu-id="733df-1628">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-1629">Az.KeyVault</span></span>
* <span data-ttu-id="733df-1630">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="733df-1631">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="733df-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="733df-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="733df-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="733df-1633">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="733df-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="733df-1634">Az.Media</span></span>
* <span data-ttu-id="733df-1635">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-1636">Az.Monitor</span></span>
  * <span data-ttu-id="733df-1637">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="733df-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="733df-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="733df-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="733df-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="733df-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="733df-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="733df-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="733df-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="733df-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="733df-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="733df-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="733df-1643">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1644">Az.Network</span></span>
* <span data-ttu-id="733df-1645">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="733df-1646">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="733df-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="733df-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="733df-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="733df-1648">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="733df-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="733df-1650">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="733df-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="733df-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="733df-1652">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1654">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="733df-1655">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="733df-1656">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="733df-1657">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="733df-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="733df-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="733df-1658">Az.RedisCache</span></span>
* <span data-ttu-id="733df-1659">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1660">Az.Resources</span></span>
* <span data-ttu-id="733df-1661">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="733df-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1662">Az.Sql</span></span>
* <span data-ttu-id="733df-1663">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="733df-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="733df-1664">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="733df-1665">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="733df-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="733df-1666">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="733df-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="733df-1667">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="733df-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="733df-1668">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="733df-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="733df-1669">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="733df-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1670">Az.Websites</span></span>
* <span data-ttu-id="733df-1671">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="733df-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="733df-1672">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="733df-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="733df-1673">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="733df-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="733df-1674">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="733df-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="733df-1675">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="733df-1676">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="733df-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="733df-1677">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="733df-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="733df-1678">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="733df-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="733df-1679">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="733df-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="733df-1680">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="733df-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="733df-1681">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="733df-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="733df-1682">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="733df-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="733df-1683">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="733df-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="733df-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1684">Az.Accounts</span></span>
* <span data-ttu-id="733df-1685">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="733df-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="733df-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="733df-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="733df-1687">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="733df-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="733df-1688">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="733df-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1689">Az.Automation</span></span>
* <span data-ttu-id="733df-1690">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="733df-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="733df-1691">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="733df-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="733df-1692">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1693">Az.Compute</span></span>
* <span data-ttu-id="733df-1694">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="733df-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="733df-1695">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="733df-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="733df-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="733df-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="733df-1697">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="733df-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-1698">Az.DataFactory</span></span>
* <span data-ttu-id="733df-1699">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="733df-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="733df-1700">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1701">Az.Resources</span></span>
* <span data-ttu-id="733df-1702">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="733df-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="733df-1703">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="733df-1704">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="733df-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="733df-1705">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="733df-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="733df-1706">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="733df-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="733df-1707">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="733df-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1708">Az.Sql</span></span>
* <span data-ttu-id="733df-1709">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="733df-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1710">Az.Storage</span></span>
* <span data-ttu-id="733df-1711">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="733df-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="733df-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="733df-1713">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="733df-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="733df-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="733df-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="733df-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="733df-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="733df-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="733df-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="733df-1718">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="733df-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="733df-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="733df-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="733df-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="733df-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="733df-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="733df-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="733df-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="733df-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="733df-1723">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="733df-1724">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="733df-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="733df-1725">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="733df-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="733df-1726">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="733df-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="733df-1727">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="733df-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="733df-1728">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="733df-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="733df-1729">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="733df-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="733df-1730">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="733df-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="733df-1731">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="733df-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1732">Az.Automation</span></span>
* <span data-ttu-id="733df-1733">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="733df-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="733df-1734">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="733df-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="733df-1735">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="733df-1735">Pre-Post script</span></span>
    * <span data-ttu-id="733df-1736">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="733df-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1737">Az.Compute</span></span>
* <span data-ttu-id="733df-1738">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="733df-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="733df-1739">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-1740">Az.KeyVault</span></span>
* <span data-ttu-id="733df-1741">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="733df-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1742">Az.Network</span></span>
* <span data-ttu-id="733df-1743">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="733df-1744">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="733df-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1746">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="733df-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="733df-1747">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="733df-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1748">Az.Resources</span></span>
* <span data-ttu-id="733df-1749">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="733df-1750">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="733df-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1751">Az.Sql</span></span>
* <span data-ttu-id="733df-1752">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="733df-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1753">Az.Storage</span></span>
* <span data-ttu-id="733df-1754">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="733df-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="733df-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="733df-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="733df-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="733df-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="733df-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="733df-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="733df-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="733df-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="733df-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="733df-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1761">Az.Websites</span></span>
* <span data-ttu-id="733df-1762">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="733df-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="733df-1763">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1764">Az.Accounts</span></span>
* <span data-ttu-id="733df-1765">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="733df-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="733df-1766">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="733df-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1767">Az.Automation</span></span>
* <span data-ttu-id="733df-1768">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="733df-1769">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="733df-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="733df-1770">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="733df-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="733df-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-1771">Az.Cdn</span></span>
* <span data-ttu-id="733df-1772">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="733df-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1773">Az.Compute</span></span>
* <span data-ttu-id="733df-1774">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="733df-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-1775">Az.DataFactory</span></span>
* <span data-ttu-id="733df-1776">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="733df-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="733df-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="733df-1777">Az.LogicApp</span></span>
* <span data-ttu-id="733df-1778">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="733df-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1779">Az.Network</span></span>
* <span data-ttu-id="733df-1780">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="733df-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1782">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="733df-1783">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="733df-1783">SDK Update</span></span>
* <span data-ttu-id="733df-1784">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="733df-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="733df-1785">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="733df-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1786">Az.Resources</span></span>
* <span data-ttu-id="733df-1787">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="733df-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="733df-1788">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="733df-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="733df-1789">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="733df-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="733df-1790">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="733df-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="733df-1791">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="733df-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="733df-1792">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="733df-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1793">Az.Sql</span></span>
* <span data-ttu-id="733df-1794">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="733df-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="733df-1795">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="733df-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1796">Az.Storage</span></span>
* <span data-ttu-id="733df-1797">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="733df-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="733df-1798">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="733df-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="733df-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="733df-1800">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="733df-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1801">Az.Automation</span></span>
* <span data-ttu-id="733df-1802">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="733df-1803">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="733df-1804">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-1806">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="733df-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1807">Az.Compute</span></span>
* <span data-ttu-id="733df-1808">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="733df-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="733df-1809">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="733df-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="733df-1810">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="733df-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="733df-1811">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="733df-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-1813">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="733df-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="733df-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="733df-1814">Az.EventHub</span></span>
* <span data-ttu-id="733df-1815">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="733df-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-1816">Az.KeyVault</span></span>
* <span data-ttu-id="733df-1817">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="733df-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="733df-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="733df-1818">Az.LogicApp</span></span>
* <span data-ttu-id="733df-1819">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="733df-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="733df-1820">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="733df-1821">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="733df-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="733df-1822">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="733df-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="733df-1823">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="733df-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="733df-1824">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="733df-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="733df-1825">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="733df-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="733df-1826">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="733df-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="733df-1827">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="733df-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="733df-1828">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="733df-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="733df-1829">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="733df-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="733df-1830">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="733df-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="733df-1831">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="733df-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-1832">Az.Monitor</span></span>
* <span data-ttu-id="733df-1833">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="733df-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1834">Az.Network</span></span>
* <span data-ttu-id="733df-1835">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="733df-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="733df-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="733df-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="733df-1837">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="733df-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="733df-1838">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="733df-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="733df-1839">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="733df-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1840">Az.Resources</span></span>
* <span data-ttu-id="733df-1841">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="733df-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="733df-1842">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="733df-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="733df-1843">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="733df-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="733df-1844">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="733df-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1845">Az.Sql</span></span>
* <span data-ttu-id="733df-1846">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="733df-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="733df-1847">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="733df-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1848">Az.Websites</span></span>
* <span data-ttu-id="733df-1849">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="733df-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="733df-1850">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1851">Az.Accounts</span></span>
* <span data-ttu-id="733df-1852">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="733df-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="733df-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="733df-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="733df-1854">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="733df-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1855">Az.Compute</span></span>
* <span data-ttu-id="733df-1856">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="733df-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="733df-1857">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="733df-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="733df-1858">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="733df-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="733df-1860">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="733df-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1861">Az.Resources</span></span>
* <span data-ttu-id="733df-1862">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="733df-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="733df-1863">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="733df-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="733df-1864">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="733df-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="733df-1865">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="733df-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1866">Az.Sql</span></span>
* <span data-ttu-id="733df-1867">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="733df-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="733df-1868">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="733df-1869">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="733df-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="733df-1870">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1871">Az.Accounts</span></span>
* <span data-ttu-id="733df-1872">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="733df-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="733df-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="733df-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="733df-1874">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="733df-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="733df-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="733df-1876">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="733df-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="733df-1877">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1878">Az.Accounts</span></span>
* <span data-ttu-id="733df-1879">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="733df-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="733df-1880">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="733df-1881">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="733df-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="733df-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="733df-1882">Az.Aks</span></span>
* <span data-ttu-id="733df-1883">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="733df-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-1884">Az.Automation</span></span>
* <span data-ttu-id="733df-1885">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="733df-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="733df-1886">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="733df-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="733df-1887">Az.Cdn</span></span>
* <span data-ttu-id="733df-1888">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1889">Az.Compute</span></span>
* <span data-ttu-id="733df-1890">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="733df-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="733df-1891">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="733df-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="733df-1892">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="733df-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="733df-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="733df-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="733df-1894">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="733df-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="733df-1895">Az.DataFactory</span></span>
* <span data-ttu-id="733df-1896">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="733df-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-1898">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="733df-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="733df-1899">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="733df-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="733df-1900">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-1901">Az.IotHub</span></span>
* <span data-ttu-id="733df-1902">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="733df-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="733df-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-1903">Az.KeyVault</span></span>
* <span data-ttu-id="733df-1904">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-1905">Az.Network</span></span>
* <span data-ttu-id="733df-1906">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1907">Az.Resources</span></span>
* <span data-ttu-id="733df-1908">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="733df-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="733df-1909">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="733df-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="733df-1910">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="733df-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="733df-1911">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="733df-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="733df-1912">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="733df-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="733df-1913">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="733df-1914">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="733df-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-1916">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="733df-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="733df-1917">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="733df-1917">Fix some error messages.</span></span>
* <span data-ttu-id="733df-1918">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="733df-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="733df-1919">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="733df-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="733df-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="733df-1920">Az.SignalR</span></span>
* <span data-ttu-id="733df-1921">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1922">Az.Sql</span></span>
* <span data-ttu-id="733df-1923">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="733df-1924">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="733df-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="733df-1925">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="733df-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="733df-1926">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="733df-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1927">Az.Storage</span></span>
* <span data-ttu-id="733df-1928">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="733df-1929">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="733df-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="733df-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="733df-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="733df-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="733df-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="733df-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="733df-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="733df-1933">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1934">Az.Websites</span></span>
* <span data-ttu-id="733df-1935">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="733df-1936">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="733df-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="733df-1937">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="733df-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="733df-1938">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="733df-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1939">Az.Accounts</span></span>
* <span data-ttu-id="733df-1940">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="733df-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-1941">Az.Compute</span></span>
* <span data-ttu-id="733df-1942">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="733df-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="733df-1943">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="733df-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="733df-1944">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="733df-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-1946">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="733df-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="733df-1947">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="733df-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="733df-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="733df-1948">Az.EventGrid</span></span>
* <span data-ttu-id="733df-1949">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="733df-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="733df-1950">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="733df-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="733df-1951">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="733df-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="733df-1952">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="733df-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="733df-1953">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="733df-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="733df-1954">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="733df-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="733df-1955">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="733df-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="733df-1956">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="733df-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="733df-1957">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="733df-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="733df-1958">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="733df-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="733df-1959">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="733df-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="733df-1960">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="733df-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="733df-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="733df-1961">Az.IotHub</span></span>
* <span data-ttu-id="733df-1962">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="733df-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="733df-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="733df-1963">Az.LogicApp</span></span>
* <span data-ttu-id="733df-1964">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="733df-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-1965">Az.Resources</span></span>
* <span data-ttu-id="733df-1966">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="733df-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="733df-1967">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="733df-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="733df-1968">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="733df-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="733df-1969">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="733df-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="733df-1970">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="733df-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="733df-1971">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="733df-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="733df-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="733df-1972">Az.SignalR</span></span>
* <span data-ttu-id="733df-1973">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="733df-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-1974">Az.Sql</span></span>
* <span data-ttu-id="733df-1975">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="733df-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="733df-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-1976">Az.Storage</span></span>
* <span data-ttu-id="733df-1977">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="733df-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="733df-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="733df-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="733df-1979">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="733df-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="733df-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="733df-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-1981">Az.Websites</span></span>
* <span data-ttu-id="733df-1982">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="733df-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="733df-1983">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="733df-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="733df-1984">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="733df-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="733df-1985">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="733df-1985">General</span></span>

- <span data-ttu-id="733df-1986">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="733df-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="733df-1987">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="733df-1987">Online help for each module</span></span>
- <span data-ttu-id="733df-1988">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="733df-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="733df-1989">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="733df-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="733df-1990">Az.Accounts</span></span>
- <span data-ttu-id="733df-1991">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="733df-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="733df-1992">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="733df-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="733df-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="733df-1994">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="733df-1994">Fixes for #7002</span></span>
- <span data-ttu-id="733df-1995">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="733df-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="733df-1996">Az.Batch</span></span>
- <span data-ttu-id="733df-1997">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="733df-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="733df-1998">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="733df-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="733df-1999">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="733df-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="733df-2000">Az.Billing</span></span>
- <span data-ttu-id="733df-2001">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="733df-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="733df-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="733df-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="733df-2003">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="733df-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="733df-2004">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="733df-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="733df-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="733df-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="733df-2006">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="733df-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="733df-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="733df-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="733df-2008">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="733df-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="733df-2010">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="733df-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="733df-2011">Az.Monitor</span></span>
- <span data-ttu-id="733df-2012">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="733df-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="733df-2013">Az.KeyVault</span></span>
- <span data-ttu-id="733df-2014">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="733df-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="733df-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="733df-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="733df-2016">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="733df-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="733df-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="733df-2017">Az.Media</span></span>
- <span data-ttu-id="733df-2018">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="733df-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="733df-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-2019">Az.Network</span></span>
<span data-ttu-id="733df-2020">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="733df-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="733df-2021">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="733df-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="733df-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="733df-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="733df-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="733df-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="733df-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="733df-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="733df-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="733df-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="733df-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="733df-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="733df-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="733df-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="733df-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="733df-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="733df-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="733df-2030">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="733df-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="733df-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="733df-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="733df-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="733df-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="733df-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="733df-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="733df-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="733df-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="733df-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="733df-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="733df-2036">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="733df-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="733df-2037">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="733df-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="733df-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="733df-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="733df-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="733df-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="733df-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="733df-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="733df-2041">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="733df-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="733df-2042">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="733df-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="733df-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="733df-2044">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="733df-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="733df-2045">Az.Profile</span></span>
- <span data-ttu-id="733df-2046">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="733df-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="733df-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="733df-2048">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="733df-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-2049">Az.Resources</span></span>
- <span data-ttu-id="733df-2050">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="733df-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="733df-2052">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="733df-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="733df-2053">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="733df-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="733df-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="733df-2055">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="733df-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="733df-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-2056">Az.Sql</span></span>
- <span data-ttu-id="733df-2057">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="733df-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="733df-2058">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="733df-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="733df-2059">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="733df-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-2060">Az.Storage</span></span>
- <span data-ttu-id="733df-2061">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="733df-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-2062">Az.Websites</span></span>
- <span data-ttu-id="733df-2063">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="733df-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="733df-2064">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="733df-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="733df-2065">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="733df-2065">General</span></span>

* <span data-ttu-id="733df-2066">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="733df-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="733df-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-2067">Az.Compute</span></span>

* <span data-ttu-id="733df-2068">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="733df-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="733df-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="733df-2070">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="733df-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="733df-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="733df-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="733df-2072">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="733df-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="733df-2073">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="733df-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="733df-2074">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="733df-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="733df-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="733df-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="733df-2076">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="733df-2077">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="733df-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="733df-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-2078">Az.Resources</span></span>

* <span data-ttu-id="733df-2079">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="733df-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="733df-2080">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="733df-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="733df-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-2081">Az.Sql</span></span>

* <span data-ttu-id="733df-2082">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="733df-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="733df-2083">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="733df-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="733df-2084">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="733df-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="733df-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="733df-2085">Az.Storage</span></span>

* <span data-ttu-id="733df-2086">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="733df-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="733df-2087">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="733df-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="733df-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="733df-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="733df-2089">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="733df-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="733df-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="733df-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="733df-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="733df-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="733df-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-2092">Az.Websites</span></span>

* <span data-ttu-id="733df-2093">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="733df-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="733df-2094">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="733df-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="733df-2095">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="733df-2096">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="733df-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="733df-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="733df-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="733df-2098">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="733df-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="733df-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="733df-2099">Az.Automation</span></span>
* <span data-ttu-id="733df-2100">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="733df-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="733df-2101">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="733df-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="733df-2102">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="733df-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="733df-2103">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="733df-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="733df-2104">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="733df-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="733df-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-2105">Az.Compute</span></span>
* <span data-ttu-id="733df-2106">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="733df-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="733df-2107">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="733df-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="733df-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="733df-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="733df-2109">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="733df-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="733df-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="733df-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="733df-2111">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="733df-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="733df-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-2112">Az.Network</span></span>
* <span data-ttu-id="733df-2113">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="733df-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="733df-2114">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="733df-2115">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="733df-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="733df-2116">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="733df-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="733df-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="733df-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="733df-2118">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="733df-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="733df-2119">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="733df-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="733df-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="733df-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="733df-2121">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="733df-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="733df-2122">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="733df-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="733df-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="733df-2123">Az.Relay</span></span>
* <span data-ttu-id="733df-2124">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="733df-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="733df-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-2125">Az.Resources</span></span>
* <span data-ttu-id="733df-2126">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="733df-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="733df-2127">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="733df-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="733df-2128">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="733df-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="733df-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-2130">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="733df-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="733df-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-2131">Az.Sql</span></span>
* <span data-ttu-id="733df-2132">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="733df-2133">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="733df-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="733df-2134">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="733df-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="733df-2135">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="733df-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="733df-2136">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="733df-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="733df-2137">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="733df-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="733df-2138">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="733df-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="733df-2139">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="733df-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="733df-2140">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="733df-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="733df-2141">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="733df-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="733df-2142">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="733df-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="733df-2143">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="733df-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="733df-2144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="733df-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="733df-2145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="733df-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="733df-2146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="733df-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="733df-2147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="733df-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="733df-2148">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="733df-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="733df-2149">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="733df-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="733df-2150">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="733df-2150">General</span></span>
* <span data-ttu-id="733df-2151">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="733df-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="733df-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="733df-2152">Az.Profile</span></span>
* <span data-ttu-id="733df-2153">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="733df-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="733df-2154">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="733df-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="733df-2155">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="733df-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="733df-2156">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="733df-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="733df-2157">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="733df-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="733df-2158">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="733df-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="733df-2159">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="733df-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-2161">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="733df-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-2162">Az.Compute</span></span>
* <span data-ttu-id="733df-2163">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="733df-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="733df-2164">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="733df-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="733df-2165">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="733df-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-2167">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="733df-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="733df-2168">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="733df-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="733df-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="733df-2169">Az.Insights</span></span>
* <span data-ttu-id="733df-2170">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="733df-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="733df-2171">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="733df-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="733df-2172">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="733df-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="733df-2173">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="733df-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-2174">Az.Network</span></span>
* <span data-ttu-id="733df-2175">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="733df-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="733df-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="733df-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="733df-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="733df-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="733df-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="733df-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="733df-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="733df-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="733df-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="733df-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="733df-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="733df-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="733df-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="733df-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="733df-2183">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="733df-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-2184">Az.Resources</span></span>
* <span data-ttu-id="733df-2185">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="733df-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="733df-2186">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="733df-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="733df-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="733df-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="733df-2188">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="733df-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="733df-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="733df-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="733df-2190">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="733df-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="733df-2191">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="733df-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="733df-2192">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="733df-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="733df-2193">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="733df-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="733df-2194">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="733df-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="733df-2195">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="733df-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="733df-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="733df-2196">Az.Profile</span></span>
* <span data-ttu-id="733df-2197">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="733df-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="733df-2198">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="733df-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-2199">Az.Compute</span></span>
* <span data-ttu-id="733df-2200">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="733df-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="733df-2201">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="733df-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="733df-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="733df-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="733df-2203">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="733df-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="733df-2204">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="733df-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="733df-2205">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="733df-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="733df-2206">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="733df-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="733df-2207">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="733df-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-2208">Az.Network</span></span>
* <span data-ttu-id="733df-2209">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="733df-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="733df-2210">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="733df-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-2211">Az.Resources</span></span>
* <span data-ttu-id="733df-2212">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="733df-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="733df-2213">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="733df-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="733df-2214">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="733df-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="733df-2215">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="733df-2215">Azure.Storage</span></span>
* <span data-ttu-id="733df-2216">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="733df-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="733df-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="733df-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="733df-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="733df-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="733df-2219">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="733df-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="733df-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="733df-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="733df-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="733df-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="733df-2222">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="733df-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="733df-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="733df-2223">Az.Compute</span></span>
* <span data-ttu-id="733df-2224">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="733df-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="733df-2225">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="733df-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="733df-2226">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="733df-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="733df-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="733df-2228">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="733df-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="733df-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="733df-2229">Az.Network</span></span>
* <span data-ttu-id="733df-2230">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="733df-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="733df-2231">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="733df-2231">new cmdlets added</span></span>
    - <span data-ttu-id="733df-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="733df-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="733df-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="733df-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="733df-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="733df-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="733df-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="733df-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="733df-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="733df-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="733df-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="733df-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="733df-2238">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="733df-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="733df-2239">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="733df-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="733df-2240">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="733df-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="733df-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="733df-2241">Az.RedisCache</span></span>
* <span data-ttu-id="733df-2242">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="733df-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="733df-2243">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="733df-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="733df-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="733df-2244">Az.Resources</span></span>
* <span data-ttu-id="733df-2245">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="733df-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="733df-2246">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="733df-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="733df-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="733df-2247">Az.Sql</span></span>
* <span data-ttu-id="733df-2248">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="733df-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="733df-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="733df-2249">Az.Websites</span></span>
* <span data-ttu-id="733df-2250">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="733df-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="733df-2251">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="733df-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="733df-2252">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="733df-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="733df-2253">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="733df-2253">Initial Release</span></span>
