---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9c5394a5fac8a8a3de96925b3563776783ea9fe
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "82080204"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f7644-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7644-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="f7644-104">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f7644-105">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="f7644-105">Highlights since the last release</span></span>
* <span data-ttu-id="f7644-106">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f7644-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-107">Az.Accounts</span></span>
* <span data-ttu-id="f7644-108">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="f7644-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f7644-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-109">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-110">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="f7644-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f7644-111">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="f7644-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7644-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-112">Az.Cdn</span></span>
* <span data-ttu-id="f7644-113">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="f7644-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-115">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="f7644-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-116">Az.Compute</span></span>
* <span data-ttu-id="f7644-117">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="f7644-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="f7644-118">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="f7644-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-119">Az.IotHub</span></span>
* <span data-ttu-id="f7644-120">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f7644-121">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f7644-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="f7644-122">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f7644-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="f7644-123">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="f7644-124">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f7644-125">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f7644-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="f7644-126">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f7644-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="f7644-127">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="f7644-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="f7644-128">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-128">New cmdlets are:</span></span>
    - <span data-ttu-id="f7644-129">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7644-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f7644-130">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7644-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f7644-131">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7644-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f7644-132">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7644-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="f7644-133">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-134">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-135">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="f7644-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="f7644-136">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="f7644-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="f7644-137">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="f7644-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="f7644-138">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f7644-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f7644-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f7644-139">Az.Maintenance</span></span>
* <span data-ttu-id="f7644-140">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="f7644-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-141">Az.Monitor</span></span>
* <span data-ttu-id="f7644-142">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="f7644-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="f7644-143">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f7644-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f7644-144">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f7644-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f7644-145">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f7644-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f7644-146">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f7644-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f7644-147">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f7644-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f7644-148">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f7644-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f7644-149">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f7644-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-150">Az.Network</span></span>
* <span data-ttu-id="f7644-151">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="f7644-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="f7644-152">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f7644-153">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f7644-154">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f7644-155">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f7644-156">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="f7644-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="f7644-157">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="f7644-158">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f7644-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="f7644-159">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="f7644-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="f7644-160">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f7644-161">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="f7644-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="f7644-162">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f7644-163">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="f7644-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="f7644-164">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f7644-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f7644-165">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="f7644-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="f7644-166">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7644-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7644-168">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="f7644-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="f7644-169">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f7644-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-171">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="f7644-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-172">Az.Sql</span></span>
* <span data-ttu-id="f7644-173">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="f7644-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="f7644-174">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-175">Az.Storage</span></span>
* <span data-ttu-id="f7644-176">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="f7644-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f7644-177">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7644-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="f7644-178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f7644-179">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f7644-180">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="f7644-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="f7644-181">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f7644-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f7644-182">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f7644-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f7644-183">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="f7644-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="f7644-184">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f7644-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f7644-185">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="f7644-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="f7644-186">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f7644-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f7644-187">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="f7644-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="f7644-188">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f7644-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="f7644-189">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="f7644-190">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-190">General</span></span>
* <span data-ttu-id="f7644-191">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="f7644-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="f7644-192">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="f7644-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="f7644-193">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="f7644-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="f7644-194">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="f7644-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="f7644-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f7644-195">Az.Billing</span></span>
  - <span data-ttu-id="f7644-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-196">Az.Compute</span></span>
  - <span data-ttu-id="f7644-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f7644-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="f7644-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-198">Az.EventHub</span></span>
  - <span data-ttu-id="f7644-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-199">Az.IotHub</span></span>
  - <span data-ttu-id="f7644-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-200">Az.KeyVault</span></span>
  - <span data-ttu-id="f7644-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-201">Az.Monitor</span></span>
  - <span data-ttu-id="f7644-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-202">Az.Network</span></span>
  - <span data-ttu-id="f7644-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-203">Az.Resources</span></span>
  - <span data-ttu-id="f7644-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-204">Az.Storage</span></span>
  - <span data-ttu-id="f7644-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-205">Az.Websites</span></span>
* <span data-ttu-id="f7644-206">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="f7644-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="f7644-207">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="f7644-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="f7644-208">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="f7644-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="f7644-209">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-210">Az.Accounts</span></span>
* <span data-ttu-id="f7644-211">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="f7644-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-212">Az.Compute</span></span>
* <span data-ttu-id="f7644-213">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="f7644-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="f7644-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f7644-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f7644-215">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f7644-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f7644-216">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="f7644-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f7644-217">[11354]</span><span class="sxs-lookup"><span data-stu-id="f7644-217">[#11354]</span></span>
* <span data-ttu-id="f7644-218">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="f7644-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f7644-219">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f7644-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f7644-220">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f7644-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f7644-221">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f7644-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f7644-222">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f7644-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f7644-223">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="f7644-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f7644-224">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7644-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f7644-225">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="f7644-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f7644-226">[11257]</span><span class="sxs-lookup"><span data-stu-id="f7644-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-227">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-228">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f7644-229">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="f7644-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-231">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="f7644-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f7644-232">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="f7644-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f7644-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7644-233">Az.HDInsight</span></span>
* <span data-ttu-id="f7644-234">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="f7644-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-235">Az.IotHub</span></span>
* <span data-ttu-id="f7644-236">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="f7644-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f7644-237">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="f7644-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="f7644-238">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="f7644-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f7644-239">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="f7644-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-240">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-241">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f7644-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-242">Az.Monitor</span></span>
* <span data-ttu-id="f7644-243">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="f7644-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-244">Az.Network</span></span>
* <span data-ttu-id="f7644-245">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="f7644-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f7644-246">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f7644-247">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f7644-248">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f7644-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f7644-249">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f7644-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f7644-250">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="f7644-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7644-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7644-252">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f7644-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-254">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f7644-255">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7644-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f7644-256">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="f7644-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f7644-257">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7644-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f7644-258">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="f7644-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f7644-259">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-260">Az.Resources</span></span>
* <span data-ttu-id="f7644-261">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="f7644-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f7644-262">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="f7644-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f7644-263">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="f7644-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f7644-264">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="f7644-264">Added example.</span></span>
* <span data-ttu-id="f7644-265">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="f7644-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f7644-266">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="f7644-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-267">Az.Sql</span></span>
* <span data-ttu-id="f7644-268">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="f7644-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f7644-269">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="f7644-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f7644-270">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f7644-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f7644-271">Az.Support</span></span>
* <span data-ttu-id="f7644-272">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="f7644-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-273">Az.Websites</span></span>
* <span data-ttu-id="f7644-274">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f7644-275">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f7644-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f7644-276">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f7644-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f7644-277">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f7644-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f7644-278">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f7644-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f7644-279">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-280">Az.Accounts</span></span>
* <span data-ttu-id="f7644-281">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="f7644-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f7644-282">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="f7644-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f7644-283">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="f7644-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f7644-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-284">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-285">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="f7644-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f7644-286">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="f7644-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f7644-287">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="f7644-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f7644-288">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="f7644-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-290">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="f7644-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-291">Az.IotHub</span></span>
* <span data-ttu-id="f7644-292">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f7644-293">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="f7644-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="f7644-294">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f7644-295">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f7644-296">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f7644-297">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f7644-298">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f7644-299">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="f7644-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="f7644-300">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f7644-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f7644-301">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f7644-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f7644-302">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f7644-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f7644-303">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f7644-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f7644-304">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f7644-305">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f7644-306">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f7644-307">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="f7644-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="f7644-308">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="f7644-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f7644-309">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="f7644-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f7644-310">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="f7644-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-311">Az.Monitor</span></span>
* <span data-ttu-id="f7644-312">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="f7644-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-313">Az.Network</span></span>
* <span data-ttu-id="f7644-314">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="f7644-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f7644-315">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="f7644-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f7644-316">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="f7644-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f7644-317">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="f7644-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-318">Az.Resources</span></span>
* <span data-ttu-id="f7644-319">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="f7644-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f7644-320">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="f7644-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f7644-321">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="f7644-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f7644-322">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="f7644-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f7644-323">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="f7644-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f7644-324">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="f7644-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f7644-325">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="f7644-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f7644-326">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7644-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f7644-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7644-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f7644-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7644-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f7644-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7644-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f7644-330">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="f7644-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f7644-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7644-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f7644-332">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-333">Az.Sql</span></span>
* <span data-ttu-id="f7644-334">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="f7644-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f7644-335">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f7644-336">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f7644-337">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="f7644-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f7644-338">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="f7644-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="f7644-339">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f7644-340">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="f7644-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f7644-341">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7644-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f7644-342">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f7644-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-343">Az.Storage</span></span>
* <span data-ttu-id="f7644-344">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7644-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f7644-345">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f7644-346">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="f7644-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f7644-347">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f7644-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f7644-348">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f7644-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-349">Az.Websites</span></span>
* <span data-ttu-id="f7644-350">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f7644-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f7644-351">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="f7644-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f7644-352">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="f7644-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f7644-353">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7644-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f7644-354">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="f7644-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f7644-355">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7644-356">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7644-356">Highlights since the last major release</span></span>
* <span data-ttu-id="f7644-357">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="f7644-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="f7644-358">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="f7644-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f7644-359">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="f7644-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-360">Az.Accounts</span></span>
* <span data-ttu-id="f7644-361">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f7644-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-362">Az.Automation</span></span>
* <span data-ttu-id="f7644-363">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-365">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f7644-366">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="f7644-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-367">Az.Compute</span></span>
* <span data-ttu-id="f7644-368">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="f7644-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f7644-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7644-369">Az.FrontDoor</span></span>
* <span data-ttu-id="f7644-370">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="f7644-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-371">Az.IotHub</span></span>
* <span data-ttu-id="f7644-372">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f7644-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f7644-373">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="f7644-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="f7644-374">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f7644-375">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f7644-376">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f7644-377">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f7644-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-378">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-379">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-380">Az.Monitor</span></span>
* <span data-ttu-id="f7644-381">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="f7644-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f7644-382">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="f7644-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f7644-383">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="f7644-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-384">Az.Network</span></span>
* <span data-ttu-id="f7644-385">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="f7644-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f7644-386">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f7644-387">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f7644-388">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f7644-389">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="f7644-389">No new cmdlets are added.</span></span> <span data-ttu-id="f7644-390">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f7644-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-392">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f7644-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-393">Az.Resources</span></span>
* <span data-ttu-id="f7644-394">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="f7644-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f7644-395">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f7644-396">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f7644-397">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="f7644-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f7644-398">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f7644-399">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="f7644-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f7644-400">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="f7644-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f7644-401">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-402">Az.Sql</span></span>
* <span data-ttu-id="f7644-403">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="f7644-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f7644-404">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="f7644-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f7644-405">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="f7644-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f7644-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f7644-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f7644-407">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="f7644-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f7644-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f7644-408">Az.StorageSync</span></span>
* <span data-ttu-id="f7644-409">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="f7644-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f7644-410">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7644-411">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7644-411">Highlights since the last major release</span></span>
* <span data-ttu-id="f7644-412">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f7644-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f7644-413">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="f7644-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-414">Az.Accounts</span></span>
* <span data-ttu-id="f7644-415">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="f7644-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f7644-416">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="f7644-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f7644-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-417">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-418">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f7644-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f7644-419">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="f7644-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="f7644-420">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="f7644-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f7644-421">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="f7644-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-422">Az.Compute</span></span>
* <span data-ttu-id="f7644-423">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7644-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f7644-424">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f7644-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f7644-425">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f7644-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f7644-427">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-428">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-429">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f7644-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f7644-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="f7644-431">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="f7644-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f7644-432">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="f7644-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f7644-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7644-433">Az.HDInsight</span></span>
* <span data-ttu-id="f7644-434">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="f7644-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-435">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-436">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f7644-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-437">Az.Network</span></span>
* <span data-ttu-id="f7644-438">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="f7644-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f7644-439">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="f7644-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f7644-440">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="f7644-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f7644-441">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="f7644-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f7644-442">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="f7644-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f7644-443">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f7644-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f7644-444">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7644-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f7644-445">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="f7644-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f7644-446">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-446">New cmdlets added:</span></span>
        - <span data-ttu-id="f7644-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7644-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f7644-448">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7644-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f7644-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f7644-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f7644-450">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="f7644-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7644-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7644-452">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="f7644-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f7644-453">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f7644-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f7644-454">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="f7644-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f7644-455">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="f7644-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-457">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="f7644-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f7644-458">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7644-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-459">Az.Resources</span></span>
* <span data-ttu-id="f7644-460">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="f7644-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f7644-461">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="f7644-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-462">Az.Sql</span></span>
<span data-ttu-id="f7644-463">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="f7644-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-464">Az.Storage</span></span>
* <span data-ttu-id="f7644-465">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f7644-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f7644-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="f7644-467">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="f7644-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f7644-468">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f7644-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-469">Az.Websites</span></span>
* <span data-ttu-id="f7644-470">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="f7644-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f7644-471">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f7644-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f7644-472">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-473">Az.Accounts</span></span>
* <span data-ttu-id="f7644-474">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="f7644-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7644-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-475">Az.Cdn</span></span>
* <span data-ttu-id="f7644-476">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f7644-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-477">Az.Compute</span></span>
* <span data-ttu-id="f7644-478">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="f7644-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f7644-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f7644-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="f7644-480">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f7644-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f7644-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f7644-482">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="f7644-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f7644-483">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f7644-484">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="f7644-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f7644-485">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f7644-486">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="f7644-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f7644-487">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f7644-488">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="f7644-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f7644-489">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f7644-490">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="f7644-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f7644-491">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f7644-492">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="f7644-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f7644-493">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f7644-494">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="f7644-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f7644-495">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f7644-496">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="f7644-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f7644-497">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="f7644-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f7644-498">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="f7644-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f7644-499">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="f7644-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-500">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-501">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f7644-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f7644-502">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f7644-503">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="f7644-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f7644-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f7644-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="f7644-505">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7644-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-506">Az.EventHub</span></span>
* <span data-ttu-id="f7644-507">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="f7644-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f7644-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7644-508">Az.HDInsight</span></span>
* <span data-ttu-id="f7644-509">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f7644-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f7644-510">Az.MachineLearning</span></span>
* <span data-ttu-id="f7644-511">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f7644-512">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="f7644-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f7644-513">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="f7644-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f7644-514">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="f7644-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f7644-515">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="f7644-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f7644-516">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="f7644-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f7644-517">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="f7644-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f7644-518">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="f7644-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-519">Az.Network</span></span>
* <span data-ttu-id="f7644-520">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="f7644-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-522">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f7644-523">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f7644-524">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f7644-525">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-526">Az.Resources</span></span>
* <span data-ttu-id="f7644-527">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="f7644-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-528">Az.Sql</span></span>
* <span data-ttu-id="f7644-529">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7644-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f7644-530">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="f7644-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f7644-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f7644-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f7644-532">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="f7644-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-533">Az.Storage</span></span>
* <span data-ttu-id="f7644-534">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="f7644-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f7644-535">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f7644-536">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="f7644-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f7644-537">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f7644-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f7644-538">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f7644-539">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-539">General</span></span>
* <span data-ttu-id="f7644-540">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="f7644-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-541">Az.Accounts</span></span>
* <span data-ttu-id="f7644-542">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="f7644-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f7644-543">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="f7644-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f7644-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7644-544">Az.Batch</span></span>
* <span data-ttu-id="f7644-545">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="f7644-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-546">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-547">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f7644-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7644-548">Az.FrontDoor</span></span>
* <span data-ttu-id="f7644-549">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="f7644-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f7644-550">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="f7644-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f7644-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f7644-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="f7644-552">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="f7644-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-553">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-554">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="f7644-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f7644-555">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="f7644-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f7644-556">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f7644-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-557">Az.Monitor</span></span>
* <span data-ttu-id="f7644-558">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="f7644-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f7644-559">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="f7644-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f7644-560">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="f7644-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-561">Az.Network</span></span>
* <span data-ttu-id="f7644-562">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="f7644-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-563">Az.Resources</span></span>
* <span data-ttu-id="f7644-564">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f7644-565">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="f7644-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-566">Az.Sql</span></span>
* <span data-ttu-id="f7644-567">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f7644-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-568">Az.Storage</span></span>
* <span data-ttu-id="f7644-569">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="f7644-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f7644-570">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="f7644-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f7644-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f7644-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f7644-572">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="f7644-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f7644-573">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="f7644-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f7644-574">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f7644-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f7644-575">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="f7644-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f7644-576">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="f7644-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f7644-577">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="f7644-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f7644-578">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="f7644-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f7644-579">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="f7644-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f7644-580">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="f7644-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f7644-581">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="f7644-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f7644-582">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7644-583">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7644-583">Highlights since the last major release</span></span>
* <span data-ttu-id="f7644-584">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f7644-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f7644-585">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f7644-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-586">Az.Compute</span></span>
* <span data-ttu-id="f7644-587">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f7644-587">VM Reapply feature</span></span>
    - <span data-ttu-id="f7644-588">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f7644-589">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="f7644-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f7644-590">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f7644-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f7644-591">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f7644-592">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7644-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f7644-593">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="f7644-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f7644-594">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="f7644-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f7644-595">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f7644-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f7644-596">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="f7644-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f7644-597">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7644-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f7644-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f7644-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f7644-599">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="f7644-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f7644-600">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="f7644-600">Get the Order</span></span>
* <span data-ttu-id="f7644-601">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="f7644-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f7644-602">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="f7644-602">Create new Order</span></span>
* <span data-ttu-id="f7644-603">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="f7644-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f7644-604">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="f7644-604">Remove the Order</span></span>
* <span data-ttu-id="f7644-605">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="f7644-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f7644-606">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="f7644-606">Now creates Local Share</span></span>
* <span data-ttu-id="f7644-607">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="f7644-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f7644-608">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="f7644-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f7644-609">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="f7644-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f7644-610">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f7644-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f7644-611">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="f7644-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f7644-612">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="f7644-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="f7644-613">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="f7644-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f7644-614">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="f7644-614">Create new Triggers</span></span>
* <span data-ttu-id="f7644-615">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="f7644-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f7644-616">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="f7644-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-617">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-618">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f7644-619">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="f7644-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-621">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="f7644-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7644-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-622">Az.EventHub</span></span>
* <span data-ttu-id="f7644-623">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="f7644-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f7644-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7644-624">Az.FrontDoor</span></span>
* <span data-ttu-id="f7644-625">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="f7644-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f7644-626">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f7644-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f7644-627">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="f7644-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f7644-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f7644-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-629">Az.Network</span></span>
* <span data-ttu-id="f7644-630">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f7644-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f7644-631">Az.PrivateDns</span></span>
* <span data-ttu-id="f7644-632">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f7644-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-634">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="f7644-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f7644-635">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7644-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f7644-636">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="f7644-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f7644-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f7644-637">Az.RedisCache</span></span>
* <span data-ttu-id="f7644-638">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="f7644-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f7644-639">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="f7644-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f7644-640">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="f7644-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-641">Az.Resources</span></span>
- <span data-ttu-id="f7644-642">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="f7644-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f7644-643">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="f7644-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="f7644-644">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="f7644-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f7644-645">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="f7644-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f7644-646">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="f7644-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-647">Az.Sql</span></span>
* <span data-ttu-id="f7644-648">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f7644-649">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="f7644-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f7644-650">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f7644-651">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-651">General</span></span>
* <span data-ttu-id="f7644-652">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f7644-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-653">Az.Accounts</span></span>
* <span data-ttu-id="f7644-654">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="f7644-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f7644-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f7644-655">Az.Advisor</span></span>
* <span data-ttu-id="f7644-656">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="f7644-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f7644-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7644-657">Az.Batch</span></span>
* <span data-ttu-id="f7644-658">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f7644-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f7644-659">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f7644-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f7644-660">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="f7644-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f7644-661">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="f7644-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f7644-662">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="f7644-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f7644-663">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="f7644-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f7644-664">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="f7644-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f7644-665">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="f7644-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f7644-666">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="f7644-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f7644-667">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f7644-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f7644-668">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="f7644-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f7644-669">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="f7644-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f7644-670">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f7644-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f7644-671">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="f7644-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f7644-672">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="f7644-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f7644-673">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="f7644-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f7644-674">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="f7644-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f7644-675">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f7644-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f7644-676">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="f7644-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f7644-677">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f7644-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="f7644-678">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f7644-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f7644-679">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f7644-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f7644-680">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="f7644-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f7644-681">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="f7644-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f7644-682">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="f7644-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f7644-683">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="f7644-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="f7644-684">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="f7644-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f7644-685">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="f7644-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f7644-686">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="f7644-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f7644-687">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="f7644-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f7644-688">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="f7644-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f7644-689">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="f7644-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f7644-690">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="f7644-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f7644-691">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="f7644-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f7644-692">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="f7644-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f7644-693">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="f7644-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7644-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-694">Az.Cdn</span></span>
* <span data-ttu-id="f7644-695">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="f7644-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f7644-696">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="f7644-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-697">Az.Compute</span></span>
* <span data-ttu-id="f7644-698">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="f7644-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f7644-699">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f7644-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f7644-700">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f7644-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f7644-701">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f7644-702">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f7644-703">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="f7644-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f7644-704">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f7644-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f7644-705">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="f7644-705">Breaking changes</span></span>
    - <span data-ttu-id="f7644-706">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="f7644-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f7644-707">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f7644-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-708">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-709">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-711">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="f7644-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f7644-712">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="f7644-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f7644-713">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="f7644-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f7644-714">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="f7644-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f7644-715">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="f7644-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f7644-716">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="f7644-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f7644-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7644-717">Az.FrontDoor</span></span>
* <span data-ttu-id="f7644-718">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="f7644-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f7644-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7644-719">Az.HDInsight</span></span>
* <span data-ttu-id="f7644-720">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="f7644-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f7644-721">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="f7644-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f7644-722">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="f7644-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f7644-723">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="f7644-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f7644-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f7644-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f7644-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f7644-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f7644-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f7644-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f7644-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f7644-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f7644-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f7644-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f7644-729">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="f7644-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="f7644-730">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f7644-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f7644-731">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f7644-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f7644-732">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f7644-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f7644-733">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="f7644-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f7644-734">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="f7644-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f7644-735">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="f7644-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f7644-736">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="f7644-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f7644-737">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f7644-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f7644-738">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="f7644-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f7644-739">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="f7644-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f7644-740">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="f7644-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="f7644-741">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="f7644-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-742">Az.IotHub</span></span>
* <span data-ttu-id="f7644-743">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="f7644-743">Breaking changes:</span></span>
    - <span data-ttu-id="f7644-744">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f7644-745">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f7644-746">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f7644-747">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f7644-748">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="f7644-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f7644-749">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="f7644-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f7644-750">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="f7644-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f7644-751">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="f7644-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f7644-752">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f7644-753">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f7644-754">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f7644-755">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="f7644-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-757">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f7644-758">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f7644-759">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f7644-760">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f7644-761">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f7644-762">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f7644-763">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f7644-764">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f7644-765">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="f7644-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-766">Az.Resources</span></span>
* <span data-ttu-id="f7644-767">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="f7644-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-768">Az.Network</span></span>
* <span data-ttu-id="f7644-769">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="f7644-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f7644-770">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="f7644-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="f7644-771">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-772">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-773">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-774">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f7644-776">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="f7644-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f7644-777">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="f7644-777">New cmdlet:</span></span>
        - <span data-ttu-id="f7644-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f7644-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f7644-779">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="f7644-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f7644-780">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f7644-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f7644-781">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f7644-782">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="f7644-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f7644-783">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="f7644-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f7644-784">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="f7644-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f7644-785">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f7644-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f7644-786">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-786">New cmdlets added:</span></span>
        - <span data-ttu-id="f7644-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f7644-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f7644-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7644-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f7644-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7644-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f7644-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7644-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f7644-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f7644-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f7644-792">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="f7644-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f7644-793">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="f7644-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f7644-794">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="f7644-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f7644-795">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="f7644-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f7644-796">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f7644-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f7644-797">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f7644-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f7644-798">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f7644-799">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-799">New cmdlets added:</span></span>
        - <span data-ttu-id="f7644-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f7644-801">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="f7644-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f7644-802">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f7644-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f7644-803">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f7644-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f7644-804">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f7644-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f7644-805">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f7644-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f7644-806">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f7644-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f7644-807">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="f7644-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f7644-808">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-808">New cmdlets added:</span></span>
        - <span data-ttu-id="f7644-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f7644-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f7644-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f7644-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f7644-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f7644-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f7644-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f7644-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f7644-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f7644-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f7644-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7644-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f7644-815">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="f7644-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f7644-816">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f7644-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f7644-817">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="f7644-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f7644-818">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="f7644-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f7644-819">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="f7644-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f7644-820">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="f7644-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f7644-821">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f7644-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f7644-822">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f7644-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f7644-823">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="f7644-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f7644-824">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="f7644-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f7644-825">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="f7644-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f7644-826">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-826">New cmdlets added:</span></span>
        - <span data-ttu-id="f7644-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f7644-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="f7644-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f7644-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f7644-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f7644-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f7644-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f7644-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-832">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="f7644-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-833">Az.Sql</span></span>
* <span data-ttu-id="f7644-834">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="f7644-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f7644-835">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="f7644-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f7644-836">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="f7644-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f7644-837">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="f7644-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f7644-838">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="f7644-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f7644-839">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f7644-840">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="f7644-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f7644-841">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="f7644-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f7644-842">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-843">Az.Storage</span></span>
* <span data-ttu-id="f7644-844">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f7644-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f7644-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f7644-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f7644-847">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="f7644-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f7644-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f7644-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f7644-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f7644-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f7644-850">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f7644-851">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-851">General</span></span>
* <span data-ttu-id="f7644-852">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f7644-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-853">Az.Accounts</span></span>
* <span data-ttu-id="f7644-854">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="f7644-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f7644-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-855">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-856">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="f7644-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f7644-857">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="f7644-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-858">Az.Automation</span></span>
* <span data-ttu-id="f7644-859">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="f7644-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f7644-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7644-860">Az.Batch</span></span>
* <span data-ttu-id="f7644-861">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-862">Az.Compute</span></span>
* <span data-ttu-id="f7644-863">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="f7644-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f7644-864">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="f7644-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f7644-865">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="f7644-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f7644-866">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="f7644-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-867">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-868">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f7644-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f7644-869">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f7644-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f7644-870">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-872">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="f7644-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f7644-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f7644-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="f7644-874">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f7644-875">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="f7644-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f7644-876">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="f7644-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f7644-877">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="f7644-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-878">Az.IotHub</span></span>
* <span data-ttu-id="f7644-879">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="f7644-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f7644-880">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="f7644-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-881">Az.Monitor</span></span>
* <span data-ttu-id="f7644-882">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="f7644-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f7644-883">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="f7644-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f7644-884">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="f7644-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f7644-885">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f7644-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-886">Az.Network</span></span>
* <span data-ttu-id="f7644-887">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="f7644-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f7644-888">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="f7644-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f7644-889">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-889">New cmdlets added:</span></span>
        - <span data-ttu-id="f7644-890">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7644-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f7644-891">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f7644-892">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="f7644-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f7644-893">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="f7644-894">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f7644-895">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f7644-896">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f7644-897">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="f7644-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f7644-898">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f7644-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f7644-899">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f7644-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f7644-900">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="f7644-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f7644-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f7644-901">Az.RedisCache</span></span>
* <span data-ttu-id="f7644-902">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="f7644-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-903">Az.Sql</span></span>
* <span data-ttu-id="f7644-904">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="f7644-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-905">Az.Storage</span></span>
* <span data-ttu-id="f7644-906">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f7644-907">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="f7644-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f7644-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7644-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f7644-909">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="f7644-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f7644-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f7644-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f7644-911">Az.StorageSync</span></span>
* <span data-ttu-id="f7644-912">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="f7644-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-913">Az.Websites</span></span>
* <span data-ttu-id="f7644-914">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="f7644-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f7644-915">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f7644-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-916">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-917">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="f7644-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f7644-918">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f7644-919">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7644-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-920">Az.Automation</span></span>
* <span data-ttu-id="f7644-921">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="f7644-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f7644-922">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="f7644-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f7644-923">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="f7644-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-924">Az.Compute</span></span>
* <span data-ttu-id="f7644-925">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f7644-926">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f7644-927">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="f7644-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f7644-928">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="f7644-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f7644-929">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="f7644-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f7644-930">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="f7644-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f7644-931">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="f7644-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f7644-932">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="f7644-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f7644-933">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-934">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-935">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="f7644-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f7644-936">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="f7644-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f7644-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7644-937">Az.HDInsight</span></span>
* <span data-ttu-id="f7644-938">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="f7644-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-939">Az.IotHub</span></span>
* <span data-ttu-id="f7644-940">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7644-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f7644-941">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="f7644-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f7644-942">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-942">New cmdlets are:</span></span>
    - <span data-ttu-id="f7644-943">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="f7644-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f7644-944">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="f7644-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f7644-945">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="f7644-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f7644-946">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="f7644-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-947">Az.Monitor</span></span>
* <span data-ttu-id="f7644-948">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="f7644-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f7644-949">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="f7644-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f7644-950">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="f7644-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f7644-951">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="f7644-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f7644-952">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="f7644-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f7644-953">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="f7644-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f7644-954">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="f7644-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f7644-955">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="f7644-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f7644-956">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="f7644-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f7644-957">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="f7644-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f7644-958">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="f7644-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f7644-959">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="f7644-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f7644-960">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="f7644-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f7644-961">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="f7644-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f7644-962">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="f7644-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f7644-963">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="f7644-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f7644-964">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="f7644-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f7644-965">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="f7644-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f7644-966">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f7644-967">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="f7644-967">Overall improved help files</span></span>
* <span data-ttu-id="f7644-968">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="f7644-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-969">Az.Network</span></span>
* <span data-ttu-id="f7644-970">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="f7644-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f7644-971">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="f7644-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f7644-972">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="f7644-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f7644-973">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="f7644-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f7644-974">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="f7644-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f7644-975">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="f7644-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f7644-976">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f7644-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f7644-977">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7644-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f7644-978">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="f7644-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f7644-979">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="f7644-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f7644-980">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f7644-981">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="f7644-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f7644-982">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-982">New cmdlets</span></span>
        - <span data-ttu-id="f7644-983">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="f7644-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f7644-984">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="f7644-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f7644-985">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="f7644-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="f7644-986">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="f7644-986">New-VpnSite</span></span>
        - <span data-ttu-id="f7644-987">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="f7644-987">Update-VpnSite</span></span>
        - <span data-ttu-id="f7644-988">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="f7644-988">New-VpnConnection</span></span>
        - <span data-ttu-id="f7644-989">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-989">Update-VpnConnection</span></span>
* <span data-ttu-id="f7644-990">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="f7644-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-992">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="f7644-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f7644-993">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7644-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-994">Az.Resources</span></span>
* <span data-ttu-id="f7644-995">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="f7644-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-997">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="f7644-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f7644-998">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="f7644-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f7644-999">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="f7644-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f7644-1000">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="f7644-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f7644-1001">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="f7644-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f7644-1002">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="f7644-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f7644-1003">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="f7644-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f7644-1004">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="f7644-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f7644-1005">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="f7644-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f7644-1006">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="f7644-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f7644-1007">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="f7644-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f7644-1008">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="f7644-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f7644-1009">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="f7644-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f7644-1010">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="f7644-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f7644-1011">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="f7644-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f7644-1012">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="f7644-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f7644-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f7644-1013">Az.SignalR</span></span>
* <span data-ttu-id="f7644-1014">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="f7644-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1015">Az.Sql</span></span>
* <span data-ttu-id="f7644-1016">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="f7644-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f7644-1017">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="f7644-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f7644-1018">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7644-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f7644-1019">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="f7644-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f7644-1020">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="f7644-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1021">Az.Storage</span></span>
* <span data-ttu-id="f7644-1022">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="f7644-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f7644-1023">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="f7644-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f7644-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f7644-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f7644-1026">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7644-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f7644-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f7644-1028">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="f7644-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f7644-1029">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="f7644-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f7644-1030">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="f7644-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f7644-1031">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="f7644-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f7644-1032">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="f7644-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1033">Az.Websites</span></span>
* <span data-ttu-id="f7644-1034">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="f7644-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f7644-1035">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="f7644-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f7644-1036">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="f7644-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f7644-1037">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f7644-1038">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-1038">General</span></span>
* <span data-ttu-id="f7644-1039">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="f7644-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1040">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1041">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="f7644-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f7644-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f7644-1042">Az.Aks</span></span>
* <span data-ttu-id="f7644-1043">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="f7644-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f7644-1044">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="f7644-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f7644-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-1046">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="f7644-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f7644-1047">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f7644-1048">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f7644-1049">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="f7644-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f7644-1050">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="f7644-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f7644-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7644-1051">Az.Batch</span></span>
* <span data-ttu-id="f7644-1052">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7644-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-1053">Az.Cdn</span></span>
* <span data-ttu-id="f7644-1054">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="f7644-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1055">Az.Compute</span></span>
* <span data-ttu-id="f7644-1056">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f7644-1057">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7644-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f7644-1058">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7644-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f7644-1059">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f7644-1060">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f7644-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f7644-1061">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f7644-1062">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f7644-1063">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="f7644-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-1064">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-1065">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="f7644-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f7644-1066">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="f7644-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f7644-1067">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="f7644-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f7644-1068">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="f7644-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-1070">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7644-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1071">Az.EventHub</span></span>
* <span data-ttu-id="f7644-1072">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f7644-1073">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="f7644-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f7644-1074">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="f7644-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f7644-1075">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="f7644-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f7644-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f7644-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f7644-1077">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="f7644-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-1078">Az.Monitor</span></span>
* <span data-ttu-id="f7644-1079">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1080">Az.Network</span></span>
* <span data-ttu-id="f7644-1081">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f7644-1082">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="f7644-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f7644-1083">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="f7644-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f7644-1084">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f7644-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f7644-1085">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="f7644-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f7644-1086">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f7644-1087">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="f7644-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7644-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7644-1089">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="f7644-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f7644-1090">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="f7644-1090">Added example</span></span>
    - <span data-ttu-id="f7644-1091">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="f7644-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f7644-1092">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f7644-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f7644-1093">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="f7644-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1095">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1096">Az.Resources</span></span>
* <span data-ttu-id="f7644-1097">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="f7644-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f7644-1098">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="f7644-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f7644-1099">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="f7644-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f7644-1100">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7644-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7644-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="f7644-1102">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f7644-1103">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="f7644-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f7644-1104">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="f7644-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-1106">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="f7644-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f7644-1107">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="f7644-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f7644-1108">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="f7644-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f7644-1109">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="f7644-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f7644-1110">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="f7644-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f7644-1111">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="f7644-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1112">Az.Sql</span></span>
* <span data-ttu-id="f7644-1113">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="f7644-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1114">Az.Storage</span></span>
* <span data-ttu-id="f7644-1115">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="f7644-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f7644-1116">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="f7644-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f7644-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f7644-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f7644-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f7644-1119">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="f7644-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f7644-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f7644-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1121">Az.Websites</span></span>
* <span data-ttu-id="f7644-1122">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="f7644-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f7644-1123">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1124">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1125">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f7644-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f7644-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f7644-1127">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="f7644-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1128">Az.Automation</span></span>
* <span data-ttu-id="f7644-1129">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7644-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-1131">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1132">Az.Compute</span></span>
* <span data-ttu-id="f7644-1133">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7644-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f7644-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7644-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f7644-1135">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f7644-1136">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="f7644-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-1137">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-1138">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f7644-1139">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="f7644-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7644-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1140">Az.EventHub</span></span>
* <span data-ttu-id="f7644-1141">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="f7644-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f7644-1142">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="f7644-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-1143">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-1144">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f7644-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f7644-1145">Az.LogicApp</span></span>
* <span data-ttu-id="f7644-1146">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f7644-1147">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f7644-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="f7644-1149">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="f7644-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1150">Az.Network</span></span>
* <span data-ttu-id="f7644-1151">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="f7644-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f7644-1152">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1152">New cmdlets</span></span>
        - <span data-ttu-id="f7644-1153">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f7644-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f7644-1154">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="f7644-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f7644-1155">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-1156">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-1157">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-1158">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f7644-1159">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="f7644-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f7644-1160">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="f7644-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f7644-1161">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f7644-1162">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f7644-1163">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f7644-1164">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f7644-1165">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="f7644-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f7644-1166">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f7644-1167">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="f7644-1168">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f7644-1169">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f7644-1170">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f7644-1171">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="f7644-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f7644-1172">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f7644-1173">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="f7644-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="f7644-1174">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f7644-1175">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f7644-1176">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="f7644-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f7644-1177">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="f7644-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f7644-1178">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="f7644-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f7644-1179">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="f7644-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7644-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7644-1181">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="f7644-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f7644-1182">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1184">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f7644-1185">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f7644-1186">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f7644-1187">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f7644-1188">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f7644-1189">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f7644-1190">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f7644-1191">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f7644-1192">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f7644-1193">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="f7644-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1194">Az.Resources</span></span>
- <span data-ttu-id="f7644-1195">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f7644-1196">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f7644-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7644-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7644-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="f7644-1198">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="f7644-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f7644-1199">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="f7644-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1200">Az.Sql</span></span>
* <span data-ttu-id="f7644-1201">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="f7644-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f7644-1202">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f7644-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f7644-1203">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1204">Az.Storage</span></span>
* <span data-ttu-id="f7644-1205">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f7644-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f7644-1206">Az.StorageSync</span></span>
* <span data-ttu-id="f7644-1207">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="f7644-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f7644-1208">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="f7644-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1209">Az.Websites</span></span>
* <span data-ttu-id="f7644-1210">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="f7644-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f7644-1211">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="f7644-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f7644-1212">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="f7644-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f7644-1213">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1214">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1215">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="f7644-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f7644-1216">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f7644-1217">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f7644-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f7644-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f7644-1218">Az.Advisor</span></span>
* <span data-ttu-id="f7644-1219">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="f7644-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f7644-1220">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7644-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f7644-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-1222">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="f7644-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f7644-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f7644-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f7644-1224">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="f7644-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f7644-1225">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="f7644-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f7644-1226">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="f7644-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f7644-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f7644-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f7644-1228">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1229">Az.Automation</span></span>
* <span data-ttu-id="f7644-1230">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1231">Az.Compute</span></span>
* <span data-ttu-id="f7644-1232">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-1233">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-1234">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="f7644-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f7644-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f7644-1235">Az.EventGrid</span></span>
* <span data-ttu-id="f7644-1236">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f7644-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1237">Az.IotHub</span></span>
* <span data-ttu-id="f7644-1238">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1239">Az.Network</span></span>
* <span data-ttu-id="f7644-1240">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="f7644-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f7644-1241">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="f7644-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7644-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7644-1243">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f7644-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f7644-1244">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="f7644-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7644-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7644-1246">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="f7644-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1248">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="f7644-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1249">Az.Resources</span></span>
    - <span data-ttu-id="f7644-1250">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="f7644-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f7644-1251">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="f7644-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f7644-1252">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="f7644-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f7644-1253">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="f7644-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7644-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7644-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="f7644-1255">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="f7644-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1256">Az.Sql</span></span>
* <span data-ttu-id="f7644-1257">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7644-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f7644-1258">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="f7644-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f7644-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f7644-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f7644-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f7644-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f7644-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f7644-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f7644-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f7644-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f7644-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f7644-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f7644-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f7644-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f7644-1265">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f7644-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1266">Az.Storage</span></span>
* <span data-ttu-id="f7644-1267">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="f7644-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f7644-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f7644-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f7644-1269">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="f7644-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f7644-1270">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f7644-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f7644-1271">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="f7644-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f7644-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f7644-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f7644-1274">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="f7644-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f7644-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f7644-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f7644-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f7644-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f7644-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f7644-1277">Az.StorageSync</span></span>
* <span data-ttu-id="f7644-1278">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7644-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f7644-1279">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1280">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1281">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="f7644-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f7644-1282">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="f7644-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f7644-1283">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="f7644-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f7644-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f7644-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f7644-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="f7644-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1286">Az.Compute</span></span>
* <span data-ttu-id="f7644-1287">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f7644-1288">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f7644-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f7644-1289">Az.Dns</span></span>
* <span data-ttu-id="f7644-1290">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="f7644-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f7644-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f7644-1291">Az.EventGrid</span></span>
* <span data-ttu-id="f7644-1292">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f7644-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f7644-1293">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-1293">New cmdlets:</span></span>
    - <span data-ttu-id="f7644-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f7644-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f7644-1295">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f7644-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f7644-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f7644-1297">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f7644-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f7644-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f7644-1299">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f7644-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f7644-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f7644-1301">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f7644-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f7644-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f7644-1303">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f7644-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f7644-1304">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f7644-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f7644-1305">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f7644-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f7644-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f7644-1307">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f7644-1308">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f7644-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f7644-1309">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f7644-1310">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="f7644-1311">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f7644-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f7644-1312">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f7644-1313">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f7644-1314">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f7644-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f7644-1315">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f7644-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f7644-1316">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="f7644-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f7644-1317">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f7644-1318">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f7644-1319">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="f7644-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f7644-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f7644-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f7644-1321">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f7644-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f7644-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f7644-1323">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f7644-1324">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f7644-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7644-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="f7644-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f7644-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f7644-1327">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="f7644-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f7644-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f7644-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f7644-1329">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1330">Az.Network</span></span>
* <span data-ttu-id="f7644-1331">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f7644-1332">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1332">New cmdlets</span></span>
        - <span data-ttu-id="f7644-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f7644-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f7644-1334">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="f7644-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f7644-1335">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1335">New cmdlets</span></span>
        - <span data-ttu-id="f7644-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f7644-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f7644-1337">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="f7644-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f7644-1338">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1338">New cmdlets</span></span>
        - <span data-ttu-id="f7644-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f7644-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f7644-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f7644-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f7644-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f7644-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f7644-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f7644-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f7644-1344">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f7644-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f7644-1345">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1345">New cmdlets</span></span>
        - <span data-ttu-id="f7644-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7644-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f7644-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7644-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f7644-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7644-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f7644-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f7644-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f7644-1350">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f7644-1351">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f7644-1352">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f7644-1353">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="f7644-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f7644-1354">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="f7644-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f7644-1355">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="f7644-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f7644-1356">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f7644-1357">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="f7644-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f7644-1358">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f7644-1359">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="f7644-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f7644-1360">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f7644-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f7644-1361">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="f7644-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f7644-1362">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="f7644-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f7644-1363">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f7644-1364">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="f7644-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f7644-1365">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f7644-1366">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f7644-1367">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f7644-1368">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="f7644-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f7644-1369">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f7644-1370">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="f7644-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f7644-1371">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="f7644-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f7644-1372">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="f7644-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7644-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7644-1374">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f7644-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1375">Az.Resources</span></span>
* <span data-ttu-id="f7644-1376">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="f7644-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f7644-1377">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="f7644-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f7644-1378">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="f7644-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f7644-1379">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-1381">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f7644-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1382">Az.Sql</span></span>
* <span data-ttu-id="f7644-1383">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="f7644-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f7644-1384">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="f7644-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f7644-1385">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f7644-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f7644-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f7644-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f7644-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f7644-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f7644-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f7644-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f7644-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f7644-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f7644-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f7644-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1391">Az.Storage</span></span>
* <span data-ttu-id="f7644-1392">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f7644-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="f7644-1394">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f7644-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1396">Az.Websites</span></span>
* <span data-ttu-id="f7644-1397">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f7644-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f7644-1398">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="f7644-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f7644-1399">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f7644-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-1400">Az.Cdn</span></span>
* <span data-ttu-id="f7644-1401">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f7644-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1402">Az.Compute</span></span>
* <span data-ttu-id="f7644-1403">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="f7644-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f7644-1404">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7644-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1405">Az.EventHub</span></span>
* <span data-ttu-id="f7644-1406">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="f7644-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f7644-1407">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f7644-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1408">Az.Network</span></span>
* <span data-ttu-id="f7644-1409">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="f7644-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f7644-1410">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="f7644-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7644-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7644-1412">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="f7644-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1414">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="f7644-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7644-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7644-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="f7644-1416">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f7644-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-1418">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="f7644-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f7644-1419">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="f7644-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1420">Az.Sql</span></span>
* <span data-ttu-id="f7644-1421">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7644-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f7644-1422">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="f7644-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f7644-1423">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="f7644-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f7644-1424">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="f7644-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1425">Az.Websites</span></span>
* <span data-ttu-id="f7644-1426">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="f7644-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f7644-1427">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f7644-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-1429">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f7644-1430">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f7644-1431">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f7644-1432">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="f7644-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f7644-1433">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="f7644-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f7644-1434">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="f7644-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f7644-1435">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f7644-1436">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f7644-1437">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7644-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f7644-1438">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f7644-1439">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f7644-1440">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="f7644-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f7644-1441">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="f7644-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f7644-1442">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f7644-1443">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f7644-1444">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f7644-1445">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f7644-1446">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f7644-1447">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="f7644-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f7644-1448">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="f7644-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f7644-1449">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f7644-1450">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="f7644-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f7644-1451">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="f7644-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f7644-1452">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7644-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f7644-1453">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="f7644-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f7644-1454">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="f7644-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f7644-1455">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="f7644-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f7644-1456">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7644-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f7644-1457">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7644-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f7644-1458">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f7644-1459">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f7644-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f7644-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f7644-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f7644-1461">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f7644-1462">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f7644-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f7644-1463">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f7644-1464">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="f7644-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f7644-1465">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f7644-1466">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="f7644-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f7644-1467">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="f7644-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f7644-1468">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f7644-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f7644-1469">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f7644-1470">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f7644-1471">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f7644-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f7644-1472">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f7644-1473">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f7644-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f7644-1474">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f7644-1475">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f7644-1476">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f7644-1477">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="f7644-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f7644-1478">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f7644-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f7644-1479">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f7644-1480">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="f7644-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f7644-1481">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="f7644-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f7644-1482">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="f7644-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f7644-1483">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="f7644-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f7644-1484">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7644-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f7644-1485">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="f7644-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f7644-1486">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f7644-1487">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f7644-1488">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f7644-1489">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="f7644-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f7644-1490">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f7644-1491">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f7644-1492">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f7644-1493">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f7644-1494">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f7644-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f7644-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f7644-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f7644-1496">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="f7644-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f7644-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f7644-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f7644-1498">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f7644-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f7644-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f7644-1500">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="f7644-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f7644-1501">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="f7644-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f7644-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f7644-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f7644-1503">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="f7644-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f7644-1504">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f7644-1505">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="f7644-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1506">Az.Automation</span></span>
* <span data-ttu-id="f7644-1507">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="f7644-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f7644-1508">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="f7644-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f7644-1509">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="f7644-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f7644-1510">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f7644-1511">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="f7644-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f7644-1512">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="f7644-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f7644-1513">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="f7644-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1514">Az.Compute</span></span>
* <span data-ttu-id="f7644-1515">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f7644-1516">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f7644-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-1518">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-1519">Az.Monitor</span></span>
* <span data-ttu-id="f7644-1520">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1521">Az.Network</span></span>
* <span data-ttu-id="f7644-1522">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f7644-1523">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="f7644-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="f7644-1524">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f7644-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f7644-1525">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="f7644-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1526">Az.Resources</span></span>
* <span data-ttu-id="f7644-1527">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1528">Az.Sql</span></span>
* <span data-ttu-id="f7644-1529">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f7644-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f7644-1530">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1531">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1532">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="f7644-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-1534">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="f7644-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f7644-1535">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7644-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1536">Az.Compute</span></span>
* <span data-ttu-id="f7644-1537">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="f7644-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f7644-1538">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f7644-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f7644-1539">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f7644-1540">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f7644-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f7644-1541">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f7644-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f7644-1542">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7644-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f7644-1543">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="f7644-1543">Breaking changes</span></span>
    - <span data-ttu-id="f7644-1544">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f7644-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f7644-1545">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f7644-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f7644-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f7644-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="f7644-1547">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="f7644-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f7644-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f7644-1548">Az.Dns</span></span>
* <span data-ttu-id="f7644-1549">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f7644-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f7644-1550">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="f7644-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f7644-1551">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="f7644-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f7644-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7644-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="f7644-1553">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f7644-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f7644-1554">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="f7644-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f7644-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7644-1555">Az.HDInsight</span></span>
* <span data-ttu-id="f7644-1556">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="f7644-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f7644-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f7644-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f7644-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f7644-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f7644-1559">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="f7644-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f7644-1560">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="f7644-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f7644-1561">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f7644-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f7644-1562">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="f7644-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-1563">Az.Monitor</span></span>
* <span data-ttu-id="f7644-1564">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="f7644-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f7644-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f7644-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f7644-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7644-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f7644-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f7644-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f7644-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f7644-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f7644-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f7644-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f7644-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f7644-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f7644-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7644-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7644-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7644-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7644-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7644-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7644-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7644-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7644-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7644-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7644-1576">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="f7644-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f7644-1577">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="f7644-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1578">Az.Network</span></span>
* <span data-ttu-id="f7644-1579">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="f7644-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f7644-1580">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1580">New cmdlets</span></span>
        - <span data-ttu-id="f7644-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="f7644-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f7644-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f7644-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f7644-1585">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="f7644-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="f7644-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f7644-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f7644-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f7644-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f7644-1588">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="f7644-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f7644-1589">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f7644-1590">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7644-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7644-1592">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f7644-1593">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f7644-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f7644-1594">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="f7644-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1596">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7644-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f7644-1597">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7644-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f7644-1598">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7644-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f7644-1599">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="f7644-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f7644-1600">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="f7644-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f7644-1601">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="f7644-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f7644-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f7644-1602">Az.Relay</span></span>
* <span data-ttu-id="f7644-1603">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7644-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7644-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="f7644-1605">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f7644-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1606">Az.Storage</span></span>
* <span data-ttu-id="f7644-1607">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="f7644-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f7644-1608">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="f7644-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f7644-1609">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f7644-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f7644-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="f7644-1611">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="f7644-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f7644-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f7644-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f7644-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1615">Az.Websites</span></span>
* <span data-ttu-id="f7644-1616">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="f7644-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f7644-1617">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="f7644-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f7644-1618">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7644-1619">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7644-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="f7644-1620">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7644-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="f7644-1621">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f7644-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f7644-1622">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f7644-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f7644-1623">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f7644-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f7644-1624">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7644-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7644-1625">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f7644-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f7644-1626">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f7644-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1627">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1628">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="f7644-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f7644-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7644-1629">Az.Batch</span></span>
* <span data-ttu-id="f7644-1630">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7644-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-1631">Az.Cdn</span></span>
* <span data-ttu-id="f7644-1632">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-1634">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1635">Az.Compute</span></span>
* <span data-ttu-id="f7644-1636">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="f7644-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f7644-1637">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7644-1638">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7644-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-1639">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-1640">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="f7644-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-1642">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f7644-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f7644-1643">Az.EventGrid</span></span>
* <span data-ttu-id="f7644-1644">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="f7644-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7644-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1645">Az.EventHub</span></span>
* <span data-ttu-id="f7644-1646">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f7644-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f7644-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7644-1647">Az.HDInsight</span></span>
* <span data-ttu-id="f7644-1648">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1649">Az.IotHub</span></span>
* <span data-ttu-id="f7644-1650">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-1651">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-1652">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7644-1653">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7644-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f7644-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f7644-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="f7644-1655">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f7644-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f7644-1656">Az.Media</span></span>
* <span data-ttu-id="f7644-1657">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-1658">Az.Monitor</span></span>
  * <span data-ttu-id="f7644-1659">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="f7644-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f7644-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f7644-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f7644-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f7644-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f7644-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7644-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f7644-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7644-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f7644-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7644-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f7644-1665">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1666">Az.Network</span></span>
* <span data-ttu-id="f7644-1667">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7644-1668">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7644-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f7644-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f7644-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="f7644-1670">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7644-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7644-1672">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f7644-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f7644-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f7644-1674">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1676">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7644-1677">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f7644-1678">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f7644-1679">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="f7644-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f7644-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f7644-1680">Az.RedisCache</span></span>
* <span data-ttu-id="f7644-1681">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1682">Az.Resources</span></span>
* <span data-ttu-id="f7644-1683">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7644-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1684">Az.Sql</span></span>
* <span data-ttu-id="f7644-1685">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="f7644-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f7644-1686">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7644-1687">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f7644-1688">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="f7644-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f7644-1689">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f7644-1690">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7644-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f7644-1691">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7644-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1692">Az.Websites</span></span>
* <span data-ttu-id="f7644-1693">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="f7644-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f7644-1694">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7644-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7644-1695">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f7644-1696">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f7644-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f7644-1697">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7644-1698">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7644-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="f7644-1699">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7644-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="f7644-1700">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f7644-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f7644-1701">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f7644-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f7644-1702">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f7644-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f7644-1703">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7644-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7644-1704">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f7644-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f7644-1705">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f7644-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7644-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1706">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1707">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f7644-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="f7644-1709">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f7644-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f7644-1710">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1711">Az.Automation</span></span>
* <span data-ttu-id="f7644-1712">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="f7644-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f7644-1713">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="f7644-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f7644-1714">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1715">Az.Compute</span></span>
* <span data-ttu-id="f7644-1716">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f7644-1717">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f7644-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f7644-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="f7644-1719">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="f7644-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-1720">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-1721">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="f7644-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f7644-1722">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1723">Az.Resources</span></span>
* <span data-ttu-id="f7644-1724">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="f7644-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f7644-1725">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f7644-1726">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="f7644-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f7644-1727">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="f7644-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f7644-1728">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="f7644-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f7644-1729">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="f7644-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1730">Az.Sql</span></span>
* <span data-ttu-id="f7644-1731">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1732">Az.Storage</span></span>
* <span data-ttu-id="f7644-1733">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f7644-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7644-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="f7644-1735">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="f7644-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f7644-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f7644-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f7644-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f7644-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f7644-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f7644-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f7644-1740">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f7644-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f7644-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f7644-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f7644-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f7644-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f7644-1745">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7644-1746">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7644-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="f7644-1747">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7644-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="f7644-1748">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f7644-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f7644-1749">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f7644-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f7644-1750">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f7644-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f7644-1751">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7644-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7644-1752">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f7644-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f7644-1753">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f7644-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1754">Az.Automation</span></span>
* <span data-ttu-id="f7644-1755">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="f7644-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f7644-1756">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="f7644-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="f7644-1757">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="f7644-1757">Pre-Post script</span></span>
    * <span data-ttu-id="f7644-1758">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1759">Az.Compute</span></span>
* <span data-ttu-id="f7644-1760">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="f7644-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f7644-1761">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-1762">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-1763">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f7644-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1764">Az.Network</span></span>
* <span data-ttu-id="f7644-1765">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f7644-1766">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1768">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7644-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f7644-1769">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="f7644-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1770">Az.Resources</span></span>
* <span data-ttu-id="f7644-1771">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f7644-1772">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="f7644-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1773">Az.Sql</span></span>
* <span data-ttu-id="f7644-1774">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1775">Az.Storage</span></span>
* <span data-ttu-id="f7644-1776">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7644-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f7644-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f7644-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f7644-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7644-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f7644-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f7644-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f7644-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f7644-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f7644-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f7644-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1783">Az.Websites</span></span>
* <span data-ttu-id="f7644-1784">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="f7644-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f7644-1785">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1786">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1787">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="f7644-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f7644-1788">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="f7644-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1789">Az.Automation</span></span>
* <span data-ttu-id="f7644-1790">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f7644-1791">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f7644-1792">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="f7644-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7644-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-1793">Az.Cdn</span></span>
* <span data-ttu-id="f7644-1794">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="f7644-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1795">Az.Compute</span></span>
* <span data-ttu-id="f7644-1796">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="f7644-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-1797">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-1798">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="f7644-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f7644-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f7644-1799">Az.LogicApp</span></span>
* <span data-ttu-id="f7644-1800">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="f7644-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1801">Az.Network</span></span>
* <span data-ttu-id="f7644-1802">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="f7644-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1804">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f7644-1805">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="f7644-1805">SDK Update</span></span>
* <span data-ttu-id="f7644-1806">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f7644-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f7644-1807">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f7644-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1808">Az.Resources</span></span>
* <span data-ttu-id="f7644-1809">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f7644-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f7644-1810">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="f7644-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f7644-1811">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="f7644-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f7644-1812">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="f7644-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f7644-1813">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="f7644-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f7644-1814">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="f7644-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1815">Az.Sql</span></span>
* <span data-ttu-id="f7644-1816">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="f7644-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f7644-1817">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="f7644-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1818">Az.Storage</span></span>
* <span data-ttu-id="f7644-1819">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f7644-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f7644-1820">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f7644-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="f7644-1822">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="f7644-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1823">Az.Automation</span></span>
* <span data-ttu-id="f7644-1824">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f7644-1825">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f7644-1826">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-1828">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7644-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1829">Az.Compute</span></span>
* <span data-ttu-id="f7644-1830">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="f7644-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f7644-1831">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="f7644-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f7644-1832">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7644-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f7644-1833">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7644-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-1835">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="f7644-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7644-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1836">Az.EventHub</span></span>
* <span data-ttu-id="f7644-1837">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="f7644-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-1838">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-1839">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="f7644-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f7644-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f7644-1840">Az.LogicApp</span></span>
* <span data-ttu-id="f7644-1841">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="f7644-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f7644-1842">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f7644-1843">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="f7644-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f7644-1844">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f7644-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f7644-1845">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f7644-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f7644-1846">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f7644-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f7644-1847">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="f7644-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f7644-1848">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="f7644-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f7644-1849">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f7644-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f7644-1850">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f7644-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f7644-1851">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f7644-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f7644-1852">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7644-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f7644-1853">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7644-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-1854">Az.Monitor</span></span>
* <span data-ttu-id="f7644-1855">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="f7644-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1856">Az.Network</span></span>
* <span data-ttu-id="f7644-1857">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="f7644-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7644-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7644-1859">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f7644-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f7644-1860">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7644-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f7644-1861">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="f7644-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1862">Az.Resources</span></span>
* <span data-ttu-id="f7644-1863">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="f7644-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f7644-1864">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="f7644-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f7644-1865">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="f7644-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f7644-1866">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="f7644-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1867">Az.Sql</span></span>
* <span data-ttu-id="f7644-1868">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f7644-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f7644-1869">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="f7644-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1870">Az.Websites</span></span>
* <span data-ttu-id="f7644-1871">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="f7644-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f7644-1872">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1873">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1874">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f7644-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f7644-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="f7644-1876">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="f7644-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1877">Az.Compute</span></span>
* <span data-ttu-id="f7644-1878">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="f7644-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f7644-1879">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="f7644-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f7644-1880">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="f7644-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="f7644-1882">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="f7644-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1883">Az.Resources</span></span>
* <span data-ttu-id="f7644-1884">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f7644-1885">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="f7644-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f7644-1886">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="f7644-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f7644-1887">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="f7644-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1888">Az.Sql</span></span>
* <span data-ttu-id="f7644-1889">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7644-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f7644-1890">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f7644-1891">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="f7644-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f7644-1892">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1893">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1894">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f7644-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="f7644-1896">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7644-1898">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f7644-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f7644-1899">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1900">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1901">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7644-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7644-1902">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7644-1903">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="f7644-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f7644-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f7644-1904">Az.Aks</span></span>
* <span data-ttu-id="f7644-1905">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7644-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-1906">Az.Automation</span></span>
* <span data-ttu-id="f7644-1907">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="f7644-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f7644-1908">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7644-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7644-1909">Az.Cdn</span></span>
* <span data-ttu-id="f7644-1910">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1911">Az.Compute</span></span>
* <span data-ttu-id="f7644-1912">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="f7644-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f7644-1913">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7644-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f7644-1914">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7644-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f7644-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7644-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f7644-1916">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7644-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7644-1917">Az.DataFactory</span></span>
* <span data-ttu-id="f7644-1918">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-1920">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="f7644-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f7644-1921">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="f7644-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f7644-1922">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1923">Az.IotHub</span></span>
* <span data-ttu-id="f7644-1924">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f7644-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7644-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-1925">Az.KeyVault</span></span>
* <span data-ttu-id="f7644-1926">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-1927">Az.Network</span></span>
* <span data-ttu-id="f7644-1928">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1929">Az.Resources</span></span>
* <span data-ttu-id="f7644-1930">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="f7644-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f7644-1931">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f7644-1932">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f7644-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f7644-1933">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="f7644-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f7644-1934">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="f7644-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f7644-1935">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f7644-1936">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="f7644-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-1938">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="f7644-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f7644-1939">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f7644-1939">Fix some error messages.</span></span>
* <span data-ttu-id="f7644-1940">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="f7644-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f7644-1941">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="f7644-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f7644-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f7644-1942">Az.SignalR</span></span>
* <span data-ttu-id="f7644-1943">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1944">Az.Sql</span></span>
* <span data-ttu-id="f7644-1945">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7644-1946">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f7644-1947">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="f7644-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f7644-1948">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="f7644-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1949">Az.Storage</span></span>
* <span data-ttu-id="f7644-1950">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7644-1951">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="f7644-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f7644-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f7644-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f7644-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f7644-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f7644-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f7644-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="f7644-1955">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-1956">Az.Websites</span></span>
* <span data-ttu-id="f7644-1957">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7644-1958">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="f7644-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f7644-1959">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="f7644-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f7644-1960">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7644-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-1961">Az.Accounts</span></span>
* <span data-ttu-id="f7644-1962">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="f7644-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-1963">Az.Compute</span></span>
* <span data-ttu-id="f7644-1964">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="f7644-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f7644-1965">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="f7644-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f7644-1966">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7644-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-1968">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="f7644-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f7644-1969">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="f7644-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f7644-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f7644-1970">Az.EventGrid</span></span>
* <span data-ttu-id="f7644-1971">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f7644-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f7644-1972">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f7644-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f7644-1973">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f7644-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f7644-1974">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="f7644-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f7644-1975">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="f7644-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f7644-1976">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f7644-1977">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f7644-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f7644-1978">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="f7644-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f7644-1979">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="f7644-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f7644-1980">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f7644-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="f7644-1981">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f7644-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f7644-1982">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="f7644-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7644-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7644-1983">Az.IotHub</span></span>
* <span data-ttu-id="f7644-1984">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="f7644-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f7644-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f7644-1985">Az.LogicApp</span></span>
* <span data-ttu-id="f7644-1986">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="f7644-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-1987">Az.Resources</span></span>
* <span data-ttu-id="f7644-1988">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="f7644-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f7644-1989">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="f7644-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f7644-1990">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f7644-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f7644-1991">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7644-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f7644-1992">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="f7644-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f7644-1993">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="f7644-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f7644-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f7644-1994">Az.SignalR</span></span>
* <span data-ttu-id="f7644-1995">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7644-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-1996">Az.Sql</span></span>
* <span data-ttu-id="f7644-1997">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="f7644-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7644-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-1998">Az.Storage</span></span>
* <span data-ttu-id="f7644-1999">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="f7644-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f7644-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7644-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="f7644-2001">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f7644-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f7644-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f7644-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-2003">Az.Websites</span></span>
* <span data-ttu-id="f7644-2004">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="f7644-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f7644-2005">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7644-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f7644-2006">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f7644-2007">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-2007">General</span></span>

- <span data-ttu-id="f7644-2008">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="f7644-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="f7644-2009">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="f7644-2009">Online help for each module</span></span>
- <span data-ttu-id="f7644-2010">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="f7644-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f7644-2011">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f7644-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7644-2012">Az.Accounts</span></span>
- <span data-ttu-id="f7644-2013">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="f7644-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="f7644-2014">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="f7644-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f7644-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="f7644-2016">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="f7644-2016">Fixes for #7002</span></span>
- <span data-ttu-id="f7644-2017">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f7644-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7644-2018">Az.Batch</span></span>
- <span data-ttu-id="f7644-2019">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f7644-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f7644-2020">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="f7644-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f7644-2021">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f7644-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f7644-2022">Az.Billing</span></span>
- <span data-ttu-id="f7644-2023">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="f7644-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f7644-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f7644-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="f7644-2025">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="f7644-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f7644-2026">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f7644-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f7644-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f7644-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="f7644-2028">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="f7644-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f7644-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f7644-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f7644-2030">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f7644-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="f7644-2032">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f7644-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7644-2033">Az.Monitor</span></span>
- <span data-ttu-id="f7644-2034">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f7644-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7644-2035">Az.KeyVault</span></span>
- <span data-ttu-id="f7644-2036">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="f7644-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f7644-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f7644-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="f7644-2038">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f7644-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f7644-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f7644-2039">Az.Media</span></span>
- <span data-ttu-id="f7644-2040">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f7644-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f7644-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-2041">Az.Network</span></span>
<span data-ttu-id="f7644-2042">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="f7644-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f7644-2043">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="f7644-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7644-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7644-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7644-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7644-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7644-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7644-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7644-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7644-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7644-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7644-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f7644-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f7644-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f7644-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f7644-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7644-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f7644-2052">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7644-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f7644-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7644-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f7644-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7644-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f7644-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7644-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f7644-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f7644-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f7644-2058">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f7644-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f7644-2059">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7644-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f7644-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f7644-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f7644-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f7644-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f7644-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f7644-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f7644-2063">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f7644-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f7644-2064">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f7644-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="f7644-2066">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f7644-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f7644-2067">Az.Profile</span></span>
- <span data-ttu-id="f7644-2068">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7644-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="f7644-2070">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f7644-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-2071">Az.Resources</span></span>
- <span data-ttu-id="f7644-2072">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f7644-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="f7644-2074">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="f7644-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f7644-2075">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f7644-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f7644-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="f7644-2077">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f7644-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f7644-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-2078">Az.Sql</span></span>
- <span data-ttu-id="f7644-2079">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="f7644-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f7644-2080">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f7644-2081">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f7644-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-2082">Az.Storage</span></span>
- <span data-ttu-id="f7644-2083">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f7644-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-2084">Az.Websites</span></span>
- <span data-ttu-id="f7644-2085">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7644-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f7644-2086">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f7644-2087">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-2087">General</span></span>

* <span data-ttu-id="f7644-2088">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="f7644-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f7644-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-2089">Az.Compute</span></span>

* <span data-ttu-id="f7644-2090">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f7644-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f7644-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="f7644-2092">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="f7644-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f7644-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7644-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="f7644-2094">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="f7644-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="f7644-2095">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f7644-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f7644-2096">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f7644-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f7644-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7644-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="f7644-2098">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f7644-2099">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="f7644-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f7644-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-2100">Az.Resources</span></span>

* <span data-ttu-id="f7644-2101">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="f7644-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f7644-2102">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="f7644-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f7644-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-2103">Az.Sql</span></span>

* <span data-ttu-id="f7644-2104">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="f7644-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f7644-2105">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="f7644-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f7644-2106">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="f7644-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f7644-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7644-2107">Az.Storage</span></span>

* <span data-ttu-id="f7644-2108">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f7644-2109">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="f7644-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f7644-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f7644-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f7644-2111">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="f7644-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="f7644-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f7644-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f7644-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f7644-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f7644-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-2114">Az.Websites</span></span>

* <span data-ttu-id="f7644-2115">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f7644-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f7644-2116">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="f7644-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f7644-2117">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f7644-2118">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f7644-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7644-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="f7644-2120">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7644-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f7644-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7644-2121">Az.Automation</span></span>
* <span data-ttu-id="f7644-2122">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="f7644-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f7644-2123">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="f7644-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f7644-2124">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="f7644-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f7644-2125">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="f7644-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f7644-2126">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="f7644-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f7644-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-2127">Az.Compute</span></span>
* <span data-ttu-id="f7644-2128">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="f7644-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f7644-2129">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7644-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f7644-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f7644-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="f7644-2131">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7644-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f7644-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f7644-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f7644-2133">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="f7644-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f7644-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-2134">Az.Network</span></span>
* <span data-ttu-id="f7644-2135">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="f7644-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f7644-2136">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f7644-2137">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f7644-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f7644-2138">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7644-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f7644-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f7644-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f7644-2140">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f7644-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f7644-2141">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="f7644-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f7644-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f7644-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f7644-2143">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f7644-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f7644-2144">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7644-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f7644-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f7644-2145">Az.Relay</span></span>
* <span data-ttu-id="f7644-2146">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="f7644-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f7644-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-2147">Az.Resources</span></span>
* <span data-ttu-id="f7644-2148">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="f7644-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f7644-2149">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="f7644-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f7644-2150">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="f7644-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f7644-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-2152">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="f7644-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f7644-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-2153">Az.Sql</span></span>
* <span data-ttu-id="f7644-2154">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f7644-2155">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7644-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7644-2156">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7644-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7644-2157">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7644-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7644-2158">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7644-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7644-2159">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7644-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f7644-2160">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7644-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f7644-2161">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7644-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f7644-2162">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7644-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f7644-2163">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="f7644-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f7644-2164">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="f7644-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f7644-2165">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="f7644-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f7644-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7644-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f7644-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7644-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f7644-2168">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7644-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f7644-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7644-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f7644-2170">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="f7644-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f7644-2171">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f7644-2172">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7644-2172">General</span></span>
* <span data-ttu-id="f7644-2173">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="f7644-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f7644-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f7644-2174">Az.Profile</span></span>
* <span data-ttu-id="f7644-2175">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f7644-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f7644-2176">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="f7644-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f7644-2177">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f7644-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f7644-2178">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="f7644-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f7644-2179">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f7644-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f7644-2180">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="f7644-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f7644-2181">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="f7644-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-2183">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f7644-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-2184">Az.Compute</span></span>
* <span data-ttu-id="f7644-2185">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f7644-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f7644-2186">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f7644-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f7644-2187">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="f7644-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-2189">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f7644-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f7644-2190">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="f7644-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f7644-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f7644-2191">Az.Insights</span></span>
* <span data-ttu-id="f7644-2192">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="f7644-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f7644-2193">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f7644-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f7644-2194">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="f7644-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f7644-2195">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="f7644-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-2196">Az.Network</span></span>
* <span data-ttu-id="f7644-2197">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="f7644-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f7644-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7644-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f7644-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f7644-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f7644-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f7644-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f7644-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f7644-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f7644-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7644-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f7644-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f7644-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7644-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7644-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7644-2205">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="f7644-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-2206">Az.Resources</span></span>
* <span data-ttu-id="f7644-2207">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="f7644-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f7644-2208">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f7644-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7644-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7644-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="f7644-2210">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="f7644-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7644-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7644-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7644-2212">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="f7644-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f7644-2213">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f7644-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f7644-2214">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f7644-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f7644-2215">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f7644-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f7644-2216">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f7644-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f7644-2217">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f7644-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f7644-2218">Az.Profile</span></span>
* <span data-ttu-id="f7644-2219">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="f7644-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f7644-2220">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f7644-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-2221">Az.Compute</span></span>
* <span data-ttu-id="f7644-2222">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="f7644-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f7644-2223">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="f7644-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7644-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7644-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7644-2225">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="f7644-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f7644-2226">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7644-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f7644-2227">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7644-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f7644-2228">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7644-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f7644-2229">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7644-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-2230">Az.Network</span></span>
* <span data-ttu-id="f7644-2231">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="f7644-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f7644-2232">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="f7644-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-2233">Az.Resources</span></span>
* <span data-ttu-id="f7644-2234">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="f7644-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f7644-2235">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="f7644-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f7644-2236">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f7644-2237">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f7644-2237">Azure.Storage</span></span>
* <span data-ttu-id="f7644-2238">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="f7644-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f7644-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f7644-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f7644-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f7644-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f7644-2241">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="f7644-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f7644-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f7644-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7644-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7644-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7644-2244">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7644-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7644-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7644-2245">Az.Compute</span></span>
* <span data-ttu-id="f7644-2246">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="f7644-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f7644-2247">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7644-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f7644-2248">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f7644-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f7644-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f7644-2250">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f7644-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7644-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7644-2251">Az.Network</span></span>
* <span data-ttu-id="f7644-2252">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="f7644-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f7644-2253">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7644-2253">new cmdlets added</span></span>
    - <span data-ttu-id="f7644-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7644-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7644-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7644-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7644-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7644-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7644-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7644-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7644-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f7644-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f7644-2260">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="f7644-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f7644-2261">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f7644-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f7644-2262">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f7644-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f7644-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f7644-2263">Az.RedisCache</span></span>
* <span data-ttu-id="f7644-2264">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="f7644-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f7644-2265">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="f7644-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7644-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7644-2266">Az.Resources</span></span>
* <span data-ttu-id="f7644-2267">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f7644-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f7644-2268">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="f7644-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7644-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7644-2269">Az.Sql</span></span>
* <span data-ttu-id="f7644-2270">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="f7644-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7644-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7644-2271">Az.Websites</span></span>
* <span data-ttu-id="f7644-2272">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="f7644-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f7644-2273">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="f7644-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f7644-2274">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7644-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f7644-2275">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="f7644-2275">Initial Release</span></span>