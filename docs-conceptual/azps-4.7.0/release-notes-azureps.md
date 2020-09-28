---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 98bae70dbd61c74aa92e69cb67afc89ebae23f70
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928615"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="482b4-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="482b4-103">Azure PowerShell release notes</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="482b4-104">4.7.0 — сентябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-104">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-105">Az.Accounts</span></span>
* <span data-ttu-id="482b4-106">Изменен формат сообщений о предстоящих критических изменениях.</span><span class="sxs-lookup"><span data-stu-id="482b4-106">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="482b4-107">Версия Azure.Core обновлена до 1.4.1.</span><span class="sxs-lookup"><span data-stu-id="482b4-107">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="482b4-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="482b4-108">Az.Aks</span></span>
* <span data-ttu-id="482b4-109">Добавлена логика проверки параметров на стороне клиента для командлетов New-AzAksCluster, Set-AzAksCluster и New-AzAksNodePool.</span><span class="sxs-lookup"><span data-stu-id="482b4-109">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="482b4-110">[12372]</span><span class="sxs-lookup"><span data-stu-id="482b4-110">[#12372]</span></span>
* <span data-ttu-id="482b4-111">Добавлена поддержка для надстроек в командлете New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-111">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="482b4-112">[11239]</span><span class="sxs-lookup"><span data-stu-id="482b4-112">[#11239]</span></span>
* <span data-ttu-id="482b4-113">Добавлены командлеты Enable-AzAksAddOn и Disable-AzAksAddOn для надстроек.</span><span class="sxs-lookup"><span data-stu-id="482b4-113">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="482b4-114">[11239]</span><span class="sxs-lookup"><span data-stu-id="482b4-114">[#11239]</span></span>
* <span data-ttu-id="482b4-115">Добавлен параметр GenerateSshKey для командлета New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-115">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="482b4-116">[12371]</span><span class="sxs-lookup"><span data-stu-id="482b4-116">[#12371]</span></span>
* <span data-ttu-id="482b4-117">Обновлена версия API до 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-117">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-119">Реализовано отображение дополнительных юридических условий для определенных API.</span><span class="sxs-lookup"><span data-stu-id="482b4-119">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-120">Az.Compute</span></span>
* <span data-ttu-id="482b4-121">Добавлен необязательный параметр -EncryptionType к командлету New-AzVmDiskEncryptionSetConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-121">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="482b4-122">Новые командлеты для нового типа ресурсов: DiskAccess (Get-AzDiskAccess, New-AzDiskAccess, Get-AzDiskAccess).</span><span class="sxs-lookup"><span data-stu-id="482b4-122">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="482b4-123">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-123">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="482b4-124">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-124">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="482b4-125">Добавлено свойство PatchStatus к представлению экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="482b4-125">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="482b4-126">Добавлено свойство VMHealth к представлению экземпляра виртуальной машины, которое является возвращенным объектом при вызове Get-AzVm с параметром -Status.</span><span class="sxs-lookup"><span data-stu-id="482b4-126">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="482b4-127">Добавлено поле AssignedHost к представлениям экземпляра Get-AzVM и Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-127">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="482b4-128">В поле отображается идентификатор ресурса для экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="482b4-128">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="482b4-129">Добавлен необязательный параметр -SupportAutomaticPlacement к командлету New-AzHostGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-129">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="482b4-130">Добавлен параметр -HostGroupId к командлетам New-AzVm и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-130">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-131">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-132">Версия пакета SDK ADF для .NET обновлена до 4.11.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-132">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-133">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-133">Az.EventHub</span></span>
* <span data-ttu-id="482b4-134">Добавлены новые командлеты кластера: New-AzEventHubCluster, Set-AzEventHubCluster, Get-AzEventHubCluster, Remove-AzEventHubCluster, Get-AzEventHubClustersAvailableRegions.</span><span class="sxs-lookup"><span data-stu-id="482b4-134">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="482b4-135">Исправление для проблемы № 10722: исправление ошибки, из-за которой свойству AuthorizationRule.Rights назначалось только значение Listen (Прослушивание).</span><span class="sxs-lookup"><span data-stu-id="482b4-135">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="482b4-136">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="482b4-136">Az.Functions</span></span>
* <span data-ttu-id="482b4-137">Удалена возможность создавать Функции версии 2 в регионах, которые не поддерживают ее.</span><span class="sxs-lookup"><span data-stu-id="482b4-137">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="482b4-138">PowerShell 6.2 не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="482b4-138">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="482b4-139">Добавлено предупреждение при создании пользователем приложения-функции PowerShell 6.2 о том, что рекомендуется создать приложение-функцию PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-139">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-140">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-141">Добавлена поддержка создания кластера с использованием конфигурации автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="482b4-141">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="482b4-142">Добавлен новый параметр AutoscaleConfiguration к командлету New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-142">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="482b4-143">Добавлена поддержка управления конфигурацией автомасштабирования для кластера.</span><span class="sxs-lookup"><span data-stu-id="482b4-143">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="482b4-144">Добавлен новый командлет Get-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-144">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="482b4-145">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-145">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="482b4-146">Добавлен новый командлет Set-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-146">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="482b4-147">Добавлен новый командлет Remove-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-147">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="482b4-148">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleScheduleCondition.</span><span class="sxs-lookup"><span data-stu-id="482b4-148">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-149">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-149">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-150">Добавлена поддержка авторизации с помощью RBAC [10557].</span><span class="sxs-lookup"><span data-stu-id="482b4-150">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="482b4-151">Расширена обработка ошибок в командлете Set-AzKeyVaultAccessPolicy [4007].</span><span class="sxs-lookup"><span data-stu-id="482b4-151">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="482b4-152">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="482b4-152">Az.Kusto</span></span>
* <span data-ttu-id="482b4-153">Выпущена общедоступная версия модуля Az.Kusto.</span><span class="sxs-lookup"><span data-stu-id="482b4-153">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-154">Az.Network</span></span>
* <span data-ttu-id="482b4-155">[Критическое изменение] Обновлены приведенные ниже командлеты для соответствия виртуальному маршрутизатору ресурсов и виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="482b4-155">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="482b4-156">New-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="482b4-156">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="482b4-157">Добавлен параметр -HostedSubnet для поддержки дочернего ресурса конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="482b4-157">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="482b4-158">Удалены параметры -HostedGateway и -HostedGatewayId.</span><span class="sxs-lookup"><span data-stu-id="482b4-158">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="482b4-159">Get-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="482b4-159">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="482b4-160">добавлен набор параметров на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-160">Added subscription level parameter set</span></span>
    - <span data-ttu-id="482b4-161">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="482b4-161">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="482b4-162">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="482b4-162">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="482b4-163">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="482b4-163">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="482b4-164">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="482b4-164">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="482b4-165">Добавлен новый командлет для порта Azure Express Route.</span><span class="sxs-lookup"><span data-stu-id="482b4-165">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="482b4-166">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="482b4-166">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="482b4-167">Добавлено свойство RemoteBgpCommunities к ресурсу пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-167">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="482b4-168">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="482b4-168">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="482b4-169">Добавлено свойство VpnGatewayIpConfigurations в выходные данные командлета Get-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-169">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="482b4-170">Исправлена ошибка командлета Set-AzApplicationGatewaySslCertificate [9488].</span><span class="sxs-lookup"><span data-stu-id="482b4-170">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="482b4-171">Добавлен параметр AllowActiveFTP в AzureFirewall.</span><span class="sxs-lookup"><span data-stu-id="482b4-171">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="482b4-172">Обновлены следующие команды для функции: Включена возможность настройки и удаления параметров безопасности в Интернете на VPN-шлюзе P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-172">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="482b4-173">Обновлен командлет New-AzP2sVpnGateway: Добавлен необязательный параметр EnableInternetSecurityFlag для клиентов, позволяющий задать значение true для включения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="482b4-173">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="482b4-174">Обновлен командлет Update-AzP2sVpnGateway: Добавлены необязательные параметры EnableInternetSecurityFlag и DisableInternetSecurityFlag для клиентов, позволяющий задать значение true/false для включения/отключения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="482b4-174">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="482b4-175">Добавлен новый командлет Reset-AzP2sVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз P2S виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="482b4-175">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="482b4-176">Добавлен новый командлет Reset-AzVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="482b4-176">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="482b4-177">Обновлен командлет Set-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-177">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="482b4-178">Для свойств группы безопасности сети и таблицы маршрутизации подсети теперь задаются значения NULL, если они явно указаны в параметрах [1548][9718].</span><span class="sxs-lookup"><span data-stu-id="482b4-178">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-180">Исправлено состояние удаления для элементов резервного копирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="482b4-180">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-181">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-181">Az.Resources</span></span>
* <span data-ttu-id="482b4-182">Добавлена отсутствующая проверка для командлета Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="482b4-182">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="482b4-183">Добавлен важный атрибут в параметр SubscriptionId командлета Get-AzResourceGroupDeploymentOperation.</span><span class="sxs-lookup"><span data-stu-id="482b4-183">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="482b4-184">Обновлены командлеты What-If шаблона ARM для отображения изменений ресурса Ignore последними.</span><span class="sxs-lookup"><span data-stu-id="482b4-184">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="482b4-185">Исправлены проблемы безопасности и сериализации параметров массива для командлетов развертывания [12773].</span><span class="sxs-lookup"><span data-stu-id="482b4-185">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-186">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-186">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-187">Добавлены новые командлеты для управляемых кластеров и типов узлов:</span><span class="sxs-lookup"><span data-stu-id="482b4-187">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="482b4-188">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="482b4-188">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="482b4-189">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="482b4-189">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="482b4-190">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="482b4-190">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="482b4-191">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="482b4-191">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="482b4-192">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="482b4-192">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="482b4-193">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="482b4-193">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="482b4-194">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="482b4-194">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="482b4-195">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="482b4-195">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="482b4-196">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="482b4-196">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="482b4-197">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="482b4-197">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="482b4-198">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="482b4-198">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="482b4-199">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="482b4-199">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="482b4-200">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="482b4-200">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="482b4-201">Restart-AzServiceFabricManagedNodeTyp</span><span class="sxs-lookup"><span data-stu-id="482b4-201">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="482b4-202">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2020-03-01 поставщика ресурсов Service Fabric для текущей модели и 2020-01-01-preview для управляемых кластеров.</span><span class="sxs-lookup"><span data-stu-id="482b4-202">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-203">Az.Sql</span></span>
* <span data-ttu-id="482b4-204">Добавлен параметр BackupStorageRedundancy к командлетам New-AzSqlInstance и Get-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="482b4-204">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="482b4-205">Добавлен командлет Get-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="482b4-205">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="482b4-206">Добавлен командлет Enable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="482b4-206">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="482b4-207">Добавлен параметр Force к командлету New-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="482b4-207">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="482b4-208">Добавлены командлеты для службы воспроизведения журнала управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-208">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="482b4-209">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="482b4-209">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="482b4-210">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="482b4-210">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="482b4-211">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="482b4-211">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="482b4-212">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="482b4-212">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="482b4-213">Добавлен командлет Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="482b4-213">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="482b4-214">Добавлен командлет Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="482b4-214">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="482b4-215">Добавлен командлет Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="482b4-215">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="482b4-216">Обновлены командлеты New-AzSqlDatabaseImport и New-AzSqlDatabaseExport для поддержки функциональности сетевой изоляции.</span><span class="sxs-lookup"><span data-stu-id="482b4-216">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="482b4-217">Добавлен командлет New-AzSqlDatabaseImportExisting.</span><span class="sxs-lookup"><span data-stu-id="482b4-217">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="482b4-218">Обновлены командлеты баз данных для поддержки указания типа хранилища резервных копий.</span><span class="sxs-lookup"><span data-stu-id="482b4-218">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="482b4-219">Добавлен параметр Force к командлету New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="482b4-219">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="482b4-220">Добавлено предупреждение для конфигурации BackupStorageRedundancy в выбранных регионах в командлете New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="482b4-220">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="482b4-221">Обновлены командлеты ActiveDirectoryOnlyAuthentication для сервера и экземпляра для включения ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-221">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-222">Az.Storage</span></span>
* <span data-ttu-id="482b4-223">Исправлен сбой отправки BLOB-объекта путем обновления до Microsoft.Azure.Storage.DataMovement 2.0.0 [12220].</span><span class="sxs-lookup"><span data-stu-id="482b4-223">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="482b4-224">Реализована поддержка восстановления до точки во времени.</span><span class="sxs-lookup"><span data-stu-id="482b4-224">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="482b4-225">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-225">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="482b4-226">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-226">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="482b4-227">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="482b4-227">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="482b4-228">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="482b4-228">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="482b4-229">Реализована поддержка получения состояния восстановления BLOB-объекта путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeBlobRestoreStatus.</span><span class="sxs-lookup"><span data-stu-id="482b4-229">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="482b4-230">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-230">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="482b4-231">Добавлено важное сообщение с предупреждением о предстоящем изменении выходных данных командлета.</span><span class="sxs-lookup"><span data-stu-id="482b4-231">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="482b4-232">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-232">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="482b4-233">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-233">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="482b4-234">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-234">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="482b4-235">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-235">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="482b4-236">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="482b4-236">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="482b4-237">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="482b4-237">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="482b4-238">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.8.</span><span class="sxs-lookup"><span data-stu-id="482b4-238">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="482b4-239">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="482b4-239">Thanks to our community contributors</span></span>
* <span data-ttu-id="482b4-240">Томас Ван Лере (Thomas Van Laere) (@ThomVanL), добавление Dockerfile-alpine-3.10 (12911).</span><span class="sxs-lookup"><span data-stu-id="482b4-240">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="482b4-241">Лохит Чаудари Чилукури (Lohith Chowdary Chilukuri) (@Lochiluk), обновление Remove-AzNetworkInterfaceIpConfig.md (12807).</span><span class="sxs-lookup"><span data-stu-id="482b4-241">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="482b4-242">Роберт Стрэнд (Roberth Strand) (@roberthstrand), Get-AzResourceGroup — новый пример и очистка (12828).</span><span class="sxs-lookup"><span data-stu-id="482b4-242">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="482b4-243">Рави Мишра (Ravi Mishra) (@inmishrar), обновление стека среды выполнения веб-приложений Azure до .NET Core (12833).</span><span class="sxs-lookup"><span data-stu-id="482b4-243">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="482b4-244">@jack-education, обновление Set-AzVirtualNetworkSubnetConfig для разрешения удаления группы безопасности сети и таблицы маршрутизации из подсети (12351).</span><span class="sxs-lookup"><span data-stu-id="482b4-244">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="482b4-245">@hagop-globanet, обновление Add-AzApplicationGatewayCustomError.md (12784).</span><span class="sxs-lookup"><span data-stu-id="482b4-245">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="482b4-246">Джошуа Ван Даален (Joshua Van Daalen) (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="482b4-246">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="482b4-247">Изменение правописания Proeprty на Property (12821)</span><span class="sxs-lookup"><span data-stu-id="482b4-247">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="482b4-248">Обновление примеров New-AzResourceLock.md (12806)</span><span class="sxs-lookup"><span data-stu-id="482b4-248">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="482b4-249">Эрагон Риддл (Eragon Riddle) (@eragonriddle), исправлено имя поля параметра в примере (12825)</span><span class="sxs-lookup"><span data-stu-id="482b4-249">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="482b4-250">@rossifumax, исправление опечатки в New-AzConfigurationAssignment.md (12701)</span><span class="sxs-lookup"><span data-stu-id="482b4-250">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="482b4-251">4.6.1 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-251">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="482b4-252">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-252">Az.Compute</span></span>
* <span data-ttu-id="482b4-253">Исправлен параметр -EncryptionAtHost в New-AzVm для удаления значения false по умолчанию [№ 12776].</span><span class="sxs-lookup"><span data-stu-id="482b4-253">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="482b4-254">4.6.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-254">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-255">Az.Accounts</span></span>
* <span data-ttu-id="482b4-256">Загружаются все общедоступные облачные среды, когда конечная точка обнаружения не возвращает AzureCloud по умолчанию или другие общедоступные среды [№ 12633]</span><span class="sxs-lookup"><span data-stu-id="482b4-256">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="482b4-257">В Get-AzSubscription предоставлен параметр SubscriptionPolicies [№ 12551].</span><span class="sxs-lookup"><span data-stu-id="482b4-257">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-258">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-258">Az.Automation</span></span>
* <span data-ttu-id="482b4-259">В Set-AzAutomationWebhook добавлен параметр -RunOn для определения группы гибридной рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="482b4-259">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-260">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-260">Az.Compute</span></span>
* <span data-ttu-id="482b4-261">В New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр -EncryptionAtHost.</span><span class="sxs-lookup"><span data-stu-id="482b4-261">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="482b4-262">В возвращаемый объект Get-AzVM и Get-AzVmss добавлен параметр SecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="482b4-262">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="482b4-263">В Get-AzHostGroup добавлен необязательный параметр -InstanceView.</span><span class="sxs-lookup"><span data-stu-id="482b4-263">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="482b4-264">Добавлен новый командлет Invoke-AzVmPatchAssessment.</span><span class="sxs-lookup"><span data-stu-id="482b4-264">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-265">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-265">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-266">В класс PSPipelineRun добавлены отсутствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="482b4-266">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-267">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-267">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-268">Включена поддержка создания кластера с функцией шифрования на узле.</span><span class="sxs-lookup"><span data-stu-id="482b4-268">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-269">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-269">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-270">Добавлены предупреждающие сообщения для планирования отключения обратимого удаления.</span><span class="sxs-lookup"><span data-stu-id="482b4-270">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="482b4-271">Добавлены предупреждающие сообщения для планирования удаления атрибута SecretValueText.</span><span class="sxs-lookup"><span data-stu-id="482b4-271">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="482b4-272">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="482b4-272">Az.Maintenance</span></span>
* <span data-ttu-id="482b4-273">В New-AzMaintenanceConfiguration добавлены дополнительные поля, связанные с расписанием.</span><span class="sxs-lookup"><span data-stu-id="482b4-273">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="482b4-274">Добавлен новый командлет для Get-AzMaintenancePublicConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-274">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="482b4-275">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="482b4-275">Az.ManagedServices</span></span>
* <span data-ttu-id="482b4-276">Добавлены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="482b4-276">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-277">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-277">Az.Monitor</span></span>
* <span data-ttu-id="482b4-278">Расширен набор параметров, заданный в Set-AzDiagnosticSetting, для разделения включения журналов и метрик [№ 12482].</span><span class="sxs-lookup"><span data-stu-id="482b4-278">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="482b4-279">Для Add-AzMetricAlertRuleV2 исправлена ошибка, возникающая при получении оповещения метрики из конвейера.</span><span class="sxs-lookup"><span data-stu-id="482b4-279">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-280">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-280">Az.Resources</span></span>
* <span data-ttu-id="482b4-281">Изменен ответ Get-AzPolicyAlias для включения сведений о том, изменяется ли этот псевдоним Политикой Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-281">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="482b4-282">Создан новый командлет Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="482b4-282">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="482b4-283">Добавлен командлет Get-AzDeploymentManagementGroupWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области группы управления.</span><span class="sxs-lookup"><span data-stu-id="482b4-283">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="482b4-284">Добавлен командлет Get-AzTenantWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области арендатора.</span><span class="sxs-lookup"><span data-stu-id="482b4-284">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="482b4-285">Переопределены параметры -WhatIf и -Confirm для New-AzManagementGroupDeployment и New-AzTenantDeployment для использования результатов выполнения What-If в шаблоне ARM.</span><span class="sxs-lookup"><span data-stu-id="482b4-285">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="482b4-286">Исправлено поведение параметров -WhatIf и -Confirm для новых командлетов развертывания, чтобы они соответствовали значению False.</span><span class="sxs-lookup"><span data-stu-id="482b4-286">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="482b4-287">Исправлена ошибка сериализации для -TemplateObject и TemplateParameterObject [№ 1528] [№ 6292].</span><span class="sxs-lookup"><span data-stu-id="482b4-287">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="482b4-288">Добавлен атрибут критического изменения в Get-AzResourceGroupDeploymentOperation для предстоящего изменения типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-288">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="482b4-289">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="482b4-289">Az.SignalR</span></span>
* <span data-ttu-id="482b4-290">Исправлены ошибки файлов справки Restart-AzSignalR и Update-AzSignalR.</span><span class="sxs-lookup"><span data-stu-id="482b4-290">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="482b4-291">Добавлены командлеты Update-AzSignalRNetworkAcl, Set-AzSignalRUpstream.</span><span class="sxs-lookup"><span data-stu-id="482b4-291">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-292">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-292">Az.Storage</span></span>
* <span data-ttu-id="482b4-293">Поддерживается ускорение запросов больших двоичных объектов:</span><span class="sxs-lookup"><span data-stu-id="482b4-293">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="482b4-294">Get-AzStorageBlobQueryResult;</span><span class="sxs-lookup"><span data-stu-id="482b4-294">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="482b4-295">New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-295">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="482b4-296">Обновлен файл справки; дополнено описание и исправлена опечатка.</span><span class="sxs-lookup"><span data-stu-id="482b4-296">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="482b4-297">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-297">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="482b4-298">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="482b4-298">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="482b4-299">Исправлена ошибка, из-за которой работа большого двоичного объекта завершается ошибкой, если связанный подкаталог не существует [№ 12592].</span><span class="sxs-lookup"><span data-stu-id="482b4-299">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="482b4-300">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="482b4-300">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="482b4-301">Включена поддержка задания, получения и удаления политики репликации объекта в учетных записях хранения:</span><span class="sxs-lookup"><span data-stu-id="482b4-301">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="482b4-302">New-AzStorageObjectReplicationPolicyRule;</span><span class="sxs-lookup"><span data-stu-id="482b4-302">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="482b4-303">Set-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="482b4-303">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="482b4-304">Get-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="482b4-304">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="482b4-305">Remove-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-305">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="482b4-306">Включена поддержка включения и отключения канала изменений в службе BLOB-объектов учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="482b4-306">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="482b4-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-307">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="482b4-308">4.5.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-308">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-309">Az.Accounts</span></span>
* <span data-ttu-id="482b4-310">Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).</span><span class="sxs-lookup"><span data-stu-id="482b4-310">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="482b4-311">Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).</span><span class="sxs-lookup"><span data-stu-id="482b4-311">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="482b4-312">Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-312">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="482b4-313">Исправлено имя модуля и сведения о версии в данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="482b4-313">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="482b4-314">Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.</span><span class="sxs-lookup"><span data-stu-id="482b4-314">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="482b4-315">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="482b4-315">Az.Aks</span></span>
* <span data-ttu-id="482b4-316">Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).</span><span class="sxs-lookup"><span data-stu-id="482b4-316">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="482b4-317">Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).</span><span class="sxs-lookup"><span data-stu-id="482b4-317">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-318">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-318">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-319">Добавлен новый командлет Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-319">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="482b4-320">Добавлен новый командлет Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-320">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="482b4-321">Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-321">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="482b4-322">Добавлен новый командлет Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="482b4-322">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="482b4-323">Добавлен новый командлет New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-323">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="482b4-324">Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-324">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="482b4-325">Добавлен новый командлет New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-325">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="482b4-326">Добавлен новый командлет Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-326">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="482b4-327">Добавлен новый командлет Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-327">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="482b4-328">Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-328">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="482b4-329">Добавлен новый командлет Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-329">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="482b4-330">Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="482b4-330">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-331">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-331">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-332">Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="482b4-332">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-333">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-333">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-334">Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).</span><span class="sxs-lookup"><span data-stu-id="482b4-334">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-335">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-335">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-336">Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-336">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="482b4-337">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-337">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="482b4-338">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-338">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="482b4-339">Добавлена поддержка создания кластера с функцией приватного канала:</span><span class="sxs-lookup"><span data-stu-id="482b4-339">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="482b4-340">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-340">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="482b4-341">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-341">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="482b4-342">Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-342">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-343">Az.Network</span></span>
* <span data-ttu-id="482b4-344">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-344">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="482b4-345">Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-345">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="482b4-346">Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="482b4-346">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="482b4-347">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="482b4-347">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-348">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-348">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-349">Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.</span><span class="sxs-lookup"><span data-stu-id="482b4-349">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="482b4-350">Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.</span><span class="sxs-lookup"><span data-stu-id="482b4-350">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="482b4-351">Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="482b4-351">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-352">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-353">Улучшена работа с обнаружением контейнеров и элементов Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="482b4-353">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-354">Az.Resources</span></span>
* <span data-ttu-id="482b4-355">Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="482b4-355">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="482b4-356">Это касается всех соответствующих изменений моделей данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-356">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-357">Az.Sql</span></span>
* <span data-ttu-id="482b4-358">Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="482b4-358">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="482b4-359">Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="482b4-359">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-360">Az.Storage</span></span>
* <span data-ttu-id="482b4-361">Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="482b4-361">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="482b4-362">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="482b4-362">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="482b4-363">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="482b4-363">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="482b4-364">Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.</span><span class="sxs-lookup"><span data-stu-id="482b4-364">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="482b4-365">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="482b4-365">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="482b4-366">Добавлена поддержка получения данных об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="482b4-366">Supported get single file share usage</span></span>
    - <span data-ttu-id="482b4-367">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="482b4-367">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="482b4-368">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-368">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-369">Az.Accounts</span></span>
* <span data-ttu-id="482b4-370">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="482b4-370">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="482b4-371">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="482b4-371">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="482b4-372">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="482b4-372">Az.Aks</span></span>
* <span data-ttu-id="482b4-373">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="482b4-373">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="482b4-374">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="482b4-374">Az.AnalysisServices</span></span>
* <span data-ttu-id="482b4-375">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="482b4-375">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-376">Az.Automation</span></span>
* <span data-ttu-id="482b4-377">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="482b4-377">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-378">Az.Compute</span></span>
* <span data-ttu-id="482b4-379">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="482b4-379">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-380">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-380">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-381">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-381">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="482b4-382">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="482b4-382">Az.EventGrid</span></span>
* <span data-ttu-id="482b4-383">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-383">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="482b4-384">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="482b4-384">Added new features:</span></span>
    - <span data-ttu-id="482b4-385">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="482b4-385">Input mapping</span></span>
    - <span data-ttu-id="482b4-386">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="482b4-386">Event Delivery Schema</span></span>
    - <span data-ttu-id="482b4-387">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="482b4-387">Private Link</span></span>
    - <span data-ttu-id="482b4-388">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="482b4-388">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="482b4-389">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="482b4-389">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="482b4-390">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="482b4-390">Azure Function As Destination</span></span>
    - <span data-ttu-id="482b4-391">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="482b4-391">WebHook Batching</span></span>
    - <span data-ttu-id="482b4-392">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="482b4-392">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="482b4-393">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="482b4-393">IpFiltering</span></span>
* <span data-ttu-id="482b4-394">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-394">Updated cmdlets:</span></span>
    - <span data-ttu-id="482b4-395">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="482b4-395">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="482b4-396">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="482b4-396">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="482b4-397">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="482b4-397">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="482b4-398">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="482b4-398">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="482b4-399">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="482b4-399">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="482b4-400">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="482b4-400">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="482b4-401">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="482b4-401">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="482b4-402">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="482b4-402">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="482b4-403">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-403">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-404">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-404">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-405">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-405">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="482b4-406">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="482b4-406">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-407">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-407">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-408">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="482b4-408">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-409">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-409">Az.Monitor</span></span>
* <span data-ttu-id="482b4-410">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="482b4-410">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-411">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-411">Az.Network</span></span>
* <span data-ttu-id="482b4-412">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-412">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="482b4-413">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-413">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="482b4-414">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="482b4-414">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="482b4-415">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="482b4-415">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="482b4-416">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="482b4-416">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="482b4-417">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="482b4-417">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="482b4-418">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-418">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="482b4-419">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-419">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="482b4-420">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="482b4-420">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="482b4-421">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="482b4-421">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="482b4-422">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="482b4-422">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="482b4-423">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="482b4-423">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="482b4-424">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="482b4-424">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="482b4-425">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-425">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="482b4-426">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="482b4-426">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="482b4-427">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="482b4-427">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="482b4-428">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="482b4-428">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-429">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-429">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-430">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="482b4-430">Removed project reference to Authentication</span></span>
* <span data-ttu-id="482b4-431">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="482b4-431">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="482b4-432">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="482b4-432">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-433">Az.Resources</span></span>
* <span data-ttu-id="482b4-434">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="482b4-434">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="482b4-435">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="482b4-435">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-436">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-436">Az.Sql</span></span>
* <span data-ttu-id="482b4-437">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="482b4-437">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="482b4-438">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-438">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="482b4-439">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="482b4-439">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-440">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-440">Az.Storage</span></span>
* <span data-ttu-id="482b4-441">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="482b4-441">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="482b4-442">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="482b4-442">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="482b4-443">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-443">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="482b4-444">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-444">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="482b4-445">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-445">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="482b4-446">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-446">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="482b4-447">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="482b4-447">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="482b4-448">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="482b4-448">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="482b4-449">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="482b4-449">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="482b4-450">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="482b4-450">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="482b4-451">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="482b4-451">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="482b4-452">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="482b4-452">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="482b4-453">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="482b4-453">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="482b4-454">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="482b4-454">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="482b4-455">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="482b4-455">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="482b4-456">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="482b4-456">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="482b4-457">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-457">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="482b4-458">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="482b4-458">Az.StorageSync</span></span>
* <span data-ttu-id="482b4-459">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-459">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="482b4-460">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="482b4-460">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="482b4-461">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="482b4-461">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="482b4-462">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="482b4-462">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-463">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-463">Az.Websites</span></span>
* <span data-ttu-id="482b4-464">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="482b4-464">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="482b4-465">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="482b4-465">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-466">Az.Accounts</span></span>
* <span data-ttu-id="482b4-467">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="482b4-467">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="482b4-468">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="482b4-468">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="482b4-469">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="482b4-469">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="482b4-470">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="482b4-470">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="482b4-471">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="482b4-471">Az.Aks</span></span>
* <span data-ttu-id="482b4-472">Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="482b4-472">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="482b4-473">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-473">Az.Batch</span></span>
* <span data-ttu-id="482b4-474">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-474">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="482b4-475">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="482b4-475">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-476">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-476">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-477">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="482b4-477">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="482b4-478">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="482b4-478">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-479">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-479">Az.Compute</span></span>
* <span data-ttu-id="482b4-480">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-480">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="482b4-481">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="482b4-481">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="482b4-482">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="482b4-482">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="482b4-483">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-483">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="482b4-484">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="482b4-484">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-485">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-486">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-486">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-487">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-487">Az.EventHub</span></span>
* <span data-ttu-id="482b4-488">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="482b4-488">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="482b4-489">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="482b4-489">Az.Functions</span></span>
* <span data-ttu-id="482b4-490">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="482b4-490">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-491">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-491">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-492">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="482b4-492">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="482b4-493">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="482b4-493">Az.HealthcareApis</span></span>
* <span data-ttu-id="482b4-494">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-494">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="482b4-495">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="482b4-495">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-496">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-496">Az.Monitor</span></span>
* <span data-ttu-id="482b4-497">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="482b4-497">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="482b4-498">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="482b4-498">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-499">Az.Network</span></span>
* <span data-ttu-id="482b4-500">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-500">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="482b4-501">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-501">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="482b4-502">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="482b4-502">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="482b4-503">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="482b4-503">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="482b4-504">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="482b4-504">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="482b4-505">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-505">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="482b4-506">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="482b4-506">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="482b4-507">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="482b4-507">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="482b4-508">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="482b4-508">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="482b4-509">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="482b4-509">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="482b4-510">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-510">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="482b4-511">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-511">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="482b4-512">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="482b4-512">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="482b4-513">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-513">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="482b4-514">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="482b4-514">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="482b4-515">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="482b4-515">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="482b4-516">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="482b4-516">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="482b4-517">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="482b4-517">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="482b4-518">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="482b4-518">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="482b4-519">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="482b4-519">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="482b4-520">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="482b4-520">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="482b4-521">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="482b4-521">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="482b4-522">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="482b4-522">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="482b4-523">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="482b4-523">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="482b4-524">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="482b4-524">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="482b4-525">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="482b4-525">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="482b4-526">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="482b4-526">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="482b4-527">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="482b4-527">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="482b4-528">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-528">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="482b4-529">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-529">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="482b4-530">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-530">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="482b4-531">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-531">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="482b4-532">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-532">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="482b4-533">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-533">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="482b4-534">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="482b4-534">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="482b4-535">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="482b4-535">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="482b4-536">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-536">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="482b4-537">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-537">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="482b4-538">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-538">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="482b4-539">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-539">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="482b4-540">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-540">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="482b4-541">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-541">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="482b4-542">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-542">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="482b4-543">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-543">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="482b4-544">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-544">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="482b4-545">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-545">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="482b4-546">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-546">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="482b4-547">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-547">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="482b4-548">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-548">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-549">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-549">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-550">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="482b4-550">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="482b4-551">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="482b4-551">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="482b4-552">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="482b4-552">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="482b4-553">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="482b4-553">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="482b4-554">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="482b4-554">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-555">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-556">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="482b4-556">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="482b4-557">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="482b4-557">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-558">Az.Resources</span></span>
* <span data-ttu-id="482b4-559">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="482b4-559">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="482b4-560">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="482b4-560">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="482b4-561">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="482b4-561">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="482b4-562">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-562">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="482b4-563">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="482b4-563">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="482b4-564">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="482b4-564">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-565">Az.Sql</span></span>
* <span data-ttu-id="482b4-566">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="482b4-566">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="482b4-567">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-567">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="482b4-568">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="482b4-568">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-569">Az.Storage</span></span>
* <span data-ttu-id="482b4-570">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="482b4-570">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="482b4-571">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-571">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="482b4-572">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="482b4-572">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-573">Az.Websites</span></span>
* <span data-ttu-id="482b4-574">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="482b4-574">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="482b4-575">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="482b4-575">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="482b4-576">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="482b4-576">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="482b4-577">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="482b4-577">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="482b4-578">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="482b4-578">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="482b4-579">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="482b4-579">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="482b4-580">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-580">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-581">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-581">Az.Accounts</span></span>
* <span data-ttu-id="482b4-582">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="482b4-582">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="482b4-583">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="482b4-583">Az.AnalysisServices</span></span>
* <span data-ttu-id="482b4-584">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-584">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-585">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-585">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-586">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="482b4-586">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="482b4-587">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="482b4-587">Az.Billing</span></span>
* <span data-ttu-id="482b4-588">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="482b4-588">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-589">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-590">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="482b4-590">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-591">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-592">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="482b4-592">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="482b4-593">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="482b4-593">Az.DataShare</span></span>
* <span data-ttu-id="482b4-594">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="482b4-594">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="482b4-595">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="482b4-595">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="482b4-596">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="482b4-596">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-597">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-597">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-598">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-598">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="482b4-599">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-599">Added optional parameters to</span></span> 
    - <span data-ttu-id="482b4-600">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="482b4-600">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="482b4-601">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="482b4-601">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-602">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-602">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-603">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="482b4-603">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="482b4-604">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="482b4-604">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="482b4-605">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="482b4-605">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="482b4-606">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="482b4-606">Az.PrivateDns</span></span>
* <span data-ttu-id="482b4-607">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-607">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-608">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-608">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-609">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="482b4-609">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="482b4-610">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="482b4-610">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-611">Az.Resources</span></span>
* <span data-ttu-id="482b4-612">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="482b4-612">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="482b4-613">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="482b4-613">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="482b4-614">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-614">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="482b4-615">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="482b4-615">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="482b4-616">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="482b4-616">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-617">Az.Sql</span></span>
* <span data-ttu-id="482b4-618">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="482b4-618">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="482b4-619">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="482b4-619">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="482b4-620">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-620">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-621">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-621">Az.Storage</span></span>
* <span data-ttu-id="482b4-622">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-622">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="482b4-623">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-623">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="482b4-624">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-624">Highlights since the last release</span></span>
* <span data-ttu-id="482b4-625">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="482b4-625">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="482b4-626">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="482b4-626">General availability of Az.Functions</span></span> 
* <span data-ttu-id="482b4-627">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="482b4-627">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-628">Az.Accounts</span></span>
* <span data-ttu-id="482b4-629">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="482b4-629">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="482b4-630">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="482b4-630">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="482b4-631">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="482b4-631">Az.Aks</span></span>
* <span data-ttu-id="482b4-632">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-632">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="482b4-633">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="482b4-633">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="482b4-634">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="482b4-634">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-635">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-635">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-636">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="482b4-636">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="482b4-637">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="482b4-637">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="482b4-638">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="482b4-638">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="482b4-639">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="482b4-639">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="482b4-640">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="482b4-640">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="482b4-641">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="482b4-641">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="482b4-642">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="482b4-642">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="482b4-643">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="482b4-643">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="482b4-644">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="482b4-644">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="482b4-645">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="482b4-645">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="482b4-646">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="482b4-646">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="482b4-647">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="482b4-647">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="482b4-648">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="482b4-648">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="482b4-649">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-649">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="482b4-650">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="482b4-650">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="482b4-651">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="482b4-651">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="482b4-652">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-652">Az.ApplicationInsights</span></span>
* <span data-ttu-id="482b4-653">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="482b4-653">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="482b4-654">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="482b4-654">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="482b4-655">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-655">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="482b4-656">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-656">Az.Batch</span></span>
* <span data-ttu-id="482b4-657">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-657">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="482b4-658">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="482b4-658">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="482b4-659">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="482b4-659">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="482b4-660">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="482b4-660">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="482b4-661">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="482b4-661">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="482b4-662">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="482b4-662">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="482b4-663">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-663">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="482b4-664">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-664">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="482b4-665">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="482b4-665">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-666">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-666">Az.Compute</span></span>
* <span data-ttu-id="482b4-667">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="482b4-667">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="482b4-668">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="482b4-668">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="482b4-669">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="482b4-669">Breaking changes</span></span>
    - <span data-ttu-id="482b4-670">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="482b4-670">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="482b4-671">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-671">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="482b4-672">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-672">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="482b4-673">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-673">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="482b4-674">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-674">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="482b4-675">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="482b4-675">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="482b4-676">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-676">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-677">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-677">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-678">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="482b4-678">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-679">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-679">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-680">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="482b4-680">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="482b4-681">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="482b4-681">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="482b4-682">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="482b4-682">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="482b4-683">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="482b4-683">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="482b4-684">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="482b4-684">Az.Functions</span></span>
* <span data-ttu-id="482b4-685">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="482b4-685">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-686">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-686">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-687">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="482b4-687">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="482b4-688">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="482b4-688">Az.HealthcareApis</span></span>
* <span data-ttu-id="482b4-689">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="482b4-689">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-690">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-690">Az.IotHub</span></span>
* <span data-ttu-id="482b4-691">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="482b4-691">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="482b4-692">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="482b4-692">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="482b4-693">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="482b4-693">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="482b4-694">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="482b4-694">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="482b4-695">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="482b4-695">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="482b4-696">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-696">New cmdlets are:</span></span>
    - <span data-ttu-id="482b4-697">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="482b4-697">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="482b4-698">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="482b4-698">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="482b4-699">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="482b4-699">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="482b4-700">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-700">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="482b4-701">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-701">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="482b4-702">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="482b4-702">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-703">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-703">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-704">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="482b4-704">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="482b4-705">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="482b4-705">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="482b4-706">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="482b4-706">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="482b4-707">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="482b4-707">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="482b4-708">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="482b4-708">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="482b4-709">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="482b4-709">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="482b4-710">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="482b4-710">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-711">Az.Monitor</span></span>
* <span data-ttu-id="482b4-712">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="482b4-712">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="482b4-713">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="482b4-713">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="482b4-714">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="482b4-714">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="482b4-715">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="482b4-715">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="482b4-716">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="482b4-716">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="482b4-717">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="482b4-717">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="482b4-718">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="482b4-718">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-719">Az.Network</span></span>
* <span data-ttu-id="482b4-720">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="482b4-720">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="482b4-721">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="482b4-721">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="482b4-722">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="482b4-722">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="482b4-723">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-723">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="482b4-724">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="482b4-724">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="482b4-725">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-725">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-726">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="482b4-726">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="482b4-727">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="482b4-727">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="482b4-728">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="482b4-728">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="482b4-729">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="482b4-729">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="482b4-730">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="482b4-730">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="482b4-731">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-731">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="482b4-732">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="482b4-732">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="482b4-733">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="482b4-733">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="482b4-734">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="482b4-734">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="482b4-735">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="482b4-735">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="482b4-736">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="482b4-736">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="482b4-737">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="482b4-737">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="482b4-738">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="482b4-738">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="482b4-739">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="482b4-739">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="482b4-740">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-740">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="482b4-741">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="482b4-741">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="482b4-742">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="482b4-742">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="482b4-743">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="482b4-743">Updated cmdlet:</span></span>
        - <span data-ttu-id="482b4-744">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="482b4-744">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-745">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-745">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-746">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="482b4-746">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="482b4-747">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-747">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="482b4-748">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="482b4-748">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="482b4-749">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="482b4-749">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="482b4-750">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="482b4-750">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="482b4-751">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="482b4-751">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="482b4-752">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-752">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="482b4-753">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="482b4-753">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-754">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-754">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-755">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="482b4-755">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="482b4-756">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="482b4-756">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="482b4-757">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-757">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="482b4-758">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="482b4-758">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="482b4-759">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="482b4-759">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-760">Az.Resources</span></span>
* <span data-ttu-id="482b4-761">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="482b4-761">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="482b4-762">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="482b4-762">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="482b4-763">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="482b4-763">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="482b4-764">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="482b4-764">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="482b4-765">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="482b4-765">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="482b4-766">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="482b4-766">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="482b4-767">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="482b4-767">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="482b4-768">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="482b4-768">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="482b4-769">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="482b4-769">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="482b4-770">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="482b4-770">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="482b4-771">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="482b4-771">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="482b4-772">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="482b4-772">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="482b4-773">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="482b4-773">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="482b4-774">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="482b4-774">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="482b4-775">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="482b4-775">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="482b4-776">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="482b4-776">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="482b4-777">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="482b4-777">'New-AzDeployment'</span></span>
    - <span data-ttu-id="482b4-778">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="482b4-778">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="482b4-779">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="482b4-779">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="482b4-780">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-780">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-781">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-781">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-782">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="482b4-782">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-783">Az.Sql</span></span>
* <span data-ttu-id="482b4-784">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="482b4-784">Enhance performance of:</span></span>
    - <span data-ttu-id="482b4-785">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="482b4-785">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="482b4-786">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="482b4-786">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="482b4-787">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="482b4-787">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="482b4-788">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="482b4-788">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="482b4-789">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="482b4-789">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="482b4-790">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="482b4-790">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="482b4-791">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="482b4-791">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="482b4-792">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="482b4-792">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="482b4-793">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-793">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="482b4-794">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="482b4-794">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-795">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-795">Az.Storage</span></span>
* <span data-ttu-id="482b4-796">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="482b4-796">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="482b4-797">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="482b4-797">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="482b4-798">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-798">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="482b4-799">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="482b4-799">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="482b4-800">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="482b4-800">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="482b4-801">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="482b4-801">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="482b4-802">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="482b4-802">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="482b4-803">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-803">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="482b4-804">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="482b4-804">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="482b4-805">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="482b4-805">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="482b4-806">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="482b4-806">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="482b4-807">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="482b4-807">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="482b4-808">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="482b4-808">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="482b4-809">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-809">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="482b4-810">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-810">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="482b4-811">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-811">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="482b4-812">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-812">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="482b4-813">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="482b4-813">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="482b4-814">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="482b4-814">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="482b4-815">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-815">Supported failover Storage account</span></span>
    - <span data-ttu-id="482b4-816">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="482b4-816">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="482b4-817">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="482b4-817">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="482b4-818">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="482b4-818">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="482b4-819">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="482b4-819">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="482b4-820">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-820">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="482b4-821">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="482b4-821">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="482b4-822">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="482b4-822">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="482b4-823">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="482b4-823">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="482b4-824">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="482b4-824">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="482b4-825">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="482b4-825">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="482b4-826">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-826">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="482b4-827">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="482b4-827">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="482b4-828">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="482b4-828">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="482b4-829">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-829">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="482b4-830">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="482b4-830">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="482b4-831">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="482b4-831">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="482b4-832">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="482b4-832">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="482b4-833">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-833">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="482b4-834">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="482b4-834">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="482b4-835">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="482b4-835">Az.TrafficManager</span></span>
* <span data-ttu-id="482b4-836">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="482b4-836">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-837">Az.Websites</span></span>
* <span data-ttu-id="482b4-838">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-838">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="482b4-839">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-839">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="482b4-840">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-840">Highlights since the last release</span></span>
* <span data-ttu-id="482b4-841">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="482b4-841">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-842">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-842">Az.Accounts</span></span>
* <span data-ttu-id="482b4-843">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="482b4-843">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-844">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-845">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="482b4-845">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="482b4-846">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="482b4-846">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="482b4-847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-847">Az.Cdn</span></span>
* <span data-ttu-id="482b4-848">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="482b4-848">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-849">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-850">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="482b4-850">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-851">Az.Compute</span></span>
* <span data-ttu-id="482b4-852">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="482b4-852">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="482b4-853">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="482b4-853">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-854">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-854">Az.IotHub</span></span>
* <span data-ttu-id="482b4-855">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-855">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="482b4-856">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="482b4-856">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="482b4-857">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="482b4-857">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="482b4-858">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-858">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="482b4-859">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-859">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="482b4-860">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="482b4-860">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="482b4-861">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="482b4-861">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="482b4-862">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="482b4-862">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="482b4-863">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-863">New cmdlets are:</span></span>
    - <span data-ttu-id="482b4-864">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-864">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="482b4-865">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-865">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="482b4-866">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-866">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="482b4-867">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-867">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="482b4-868">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-868">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-869">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-869">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-870">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="482b4-870">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="482b4-871">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="482b4-871">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="482b4-872">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="482b4-872">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="482b4-873">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="482b4-873">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="482b4-874">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="482b4-874">Az.Maintenance</span></span>
* <span data-ttu-id="482b4-875">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="482b4-875">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-876">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-876">Az.Monitor</span></span>
* <span data-ttu-id="482b4-877">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="482b4-877">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="482b4-878">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="482b4-878">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="482b4-879">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="482b4-879">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="482b4-880">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="482b4-880">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="482b4-881">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="482b4-881">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="482b4-882">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="482b4-882">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="482b4-883">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="482b4-883">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="482b4-884">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="482b4-884">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-885">Az.Network</span></span>
* <span data-ttu-id="482b4-886">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="482b4-886">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="482b4-887">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-887">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="482b4-888">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-888">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="482b4-889">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-889">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="482b4-890">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-890">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="482b4-891">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="482b4-891">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="482b4-892">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-892">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="482b4-893">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="482b4-893">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="482b4-894">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="482b4-894">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="482b4-895">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-895">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="482b4-896">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="482b4-896">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="482b4-897">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-897">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="482b4-898">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="482b4-898">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="482b4-899">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="482b4-899">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="482b4-900">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="482b4-900">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="482b4-901">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-901">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-902">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-902">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-903">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="482b4-903">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="482b4-904">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="482b4-904">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-905">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-905">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-906">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-906">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-907">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-907">Az.Sql</span></span>
* <span data-ttu-id="482b4-908">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="482b4-908">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="482b4-909">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-909">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-910">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-910">Az.Storage</span></span>
* <span data-ttu-id="482b4-911">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="482b4-911">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="482b4-912">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-912">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="482b4-913">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-913">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="482b4-914">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-914">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="482b4-915">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="482b4-915">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="482b4-916">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="482b4-916">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="482b4-917">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="482b4-917">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="482b4-918">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="482b4-918">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="482b4-919">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="482b4-919">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="482b4-920">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="482b4-920">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="482b4-921">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="482b4-921">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="482b4-922">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="482b4-922">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="482b4-923">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="482b4-923">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="482b4-924">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-924">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="482b4-925">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-925">General</span></span>
* <span data-ttu-id="482b4-926">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="482b4-926">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="482b4-927">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="482b4-927">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="482b4-928">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="482b4-928">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="482b4-929">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="482b4-929">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="482b4-930">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="482b4-930">Az.Billing</span></span>
  - <span data-ttu-id="482b4-931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-931">Az.Compute</span></span>
  - <span data-ttu-id="482b4-932">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="482b4-932">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="482b4-933">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-933">Az.EventHub</span></span>
  - <span data-ttu-id="482b4-934">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-934">Az.IotHub</span></span>
  - <span data-ttu-id="482b4-935">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-935">Az.KeyVault</span></span>
  - <span data-ttu-id="482b4-936">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-936">Az.Monitor</span></span>
  - <span data-ttu-id="482b4-937">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-937">Az.Network</span></span>
  - <span data-ttu-id="482b4-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-938">Az.Resources</span></span>
  - <span data-ttu-id="482b4-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-939">Az.Storage</span></span>
  - <span data-ttu-id="482b4-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-940">Az.Websites</span></span>
* <span data-ttu-id="482b4-941">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="482b4-941">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="482b4-942">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="482b4-942">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="482b4-943">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="482b4-943">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="482b4-944">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-944">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-945">Az.Accounts</span></span>
* <span data-ttu-id="482b4-946">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="482b4-946">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-947">Az.Compute</span></span>
* <span data-ttu-id="482b4-948">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="482b4-948">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="482b4-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="482b4-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="482b4-950">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="482b4-950">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="482b4-951">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="482b4-951">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="482b4-952">[11354]</span><span class="sxs-lookup"><span data-stu-id="482b4-952">[#11354]</span></span>
* <span data-ttu-id="482b4-953">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="482b4-953">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="482b4-954">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="482b4-954">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="482b4-955">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="482b4-955">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="482b4-956">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="482b4-956">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="482b4-957">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="482b4-957">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="482b4-958">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="482b4-958">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="482b4-959">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="482b4-959">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="482b4-960">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="482b4-960">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="482b4-961">[11257]</span><span class="sxs-lookup"><span data-stu-id="482b4-961">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-962">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-963">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-963">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="482b4-964">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="482b4-964">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-965">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-965">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-966">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="482b4-966">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="482b4-967">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="482b4-967">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-968">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-968">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-969">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="482b4-969">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-970">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-970">Az.IotHub</span></span>
* <span data-ttu-id="482b4-971">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="482b4-971">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="482b4-972">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="482b4-972">New Cmdlets are:</span></span>
    - <span data-ttu-id="482b4-973">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="482b4-973">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="482b4-974">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="482b4-974">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-975">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-975">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-976">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="482b4-976">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-977">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-977">Az.Monitor</span></span>
* <span data-ttu-id="482b4-978">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="482b4-978">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-979">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-979">Az.Network</span></span>
* <span data-ttu-id="482b4-980">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="482b4-980">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="482b4-981">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-981">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="482b4-982">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-982">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="482b4-983">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="482b4-983">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="482b4-984">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="482b4-984">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="482b4-985">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="482b4-985">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-986">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-986">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-987">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="482b4-987">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-988">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-988">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-989">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-989">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="482b4-990">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="482b4-990">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="482b4-991">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="482b4-991">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="482b4-992">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="482b4-992">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="482b4-993">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="482b4-993">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="482b4-994">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-994">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-995">Az.Resources</span></span>
* <span data-ttu-id="482b4-996">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="482b4-996">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="482b4-997">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="482b4-997">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="482b4-998">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="482b4-998">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="482b4-999">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="482b4-999">Added example.</span></span>
* <span data-ttu-id="482b4-1000">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="482b4-1000">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="482b4-1001">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="482b4-1001">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1002">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1002">Az.Sql</span></span>
* <span data-ttu-id="482b4-1003">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="482b4-1003">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="482b4-1004">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="482b4-1004">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="482b4-1005">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-1005">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="482b4-1006">Az.Support</span><span class="sxs-lookup"><span data-stu-id="482b4-1006">Az.Support</span></span>
* <span data-ttu-id="482b4-1007">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="482b4-1007">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-1008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-1008">Az.Websites</span></span>
* <span data-ttu-id="482b4-1009">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-1009">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="482b4-1010">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="482b4-1010">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="482b4-1011">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="482b4-1011">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="482b4-1012">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="482b4-1012">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="482b4-1013">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="482b4-1013">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="482b4-1014">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1014">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-1015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1015">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1016">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="482b4-1016">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="482b4-1017">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="482b4-1017">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="482b4-1018">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="482b4-1018">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-1019">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-1019">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-1020">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="482b4-1020">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="482b4-1021">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="482b4-1021">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="482b4-1022">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="482b4-1022">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="482b4-1023">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="482b4-1023">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-1024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-1024">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-1025">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="482b4-1025">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-1026">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1026">Az.IotHub</span></span>
* <span data-ttu-id="482b4-1027">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1027">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="482b4-1028">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="482b4-1028">New Cmdlets are:</span></span>
    - <span data-ttu-id="482b4-1029">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1029">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="482b4-1030">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1030">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="482b4-1031">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1031">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="482b4-1032">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1032">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="482b4-1033">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1033">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="482b4-1034">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="482b4-1034">New Cmdlets are:</span></span>
    - <span data-ttu-id="482b4-1035">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="482b4-1035">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="482b4-1036">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="482b4-1036">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="482b4-1037">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="482b4-1037">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="482b4-1038">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="482b4-1038">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="482b4-1039">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1039">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="482b4-1040">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1040">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="482b4-1041">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1041">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="482b4-1042">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="482b4-1042">New Cmdlets are:</span></span>
    - <span data-ttu-id="482b4-1043">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="482b4-1043">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="482b4-1044">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="482b4-1044">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="482b4-1045">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="482b4-1045">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-1046">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-1046">Az.Monitor</span></span>
* <span data-ttu-id="482b4-1047">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="482b4-1047">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1048">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1048">Az.Network</span></span>
* <span data-ttu-id="482b4-1049">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="482b4-1049">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="482b4-1050">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="482b4-1050">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="482b4-1051">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="482b4-1051">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="482b4-1052">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="482b4-1052">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1053">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1053">Az.Resources</span></span>
* <span data-ttu-id="482b4-1054">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="482b4-1054">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="482b4-1055">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="482b4-1055">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="482b4-1056">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="482b4-1056">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="482b4-1057">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="482b4-1057">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="482b4-1058">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="482b4-1058">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="482b4-1059">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="482b4-1059">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="482b4-1060">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="482b4-1060">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="482b4-1061">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="482b4-1061">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="482b4-1062">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="482b4-1062">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="482b4-1063">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="482b4-1063">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="482b4-1064">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="482b4-1064">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="482b4-1065">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="482b4-1065">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="482b4-1066">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="482b4-1066">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="482b4-1067">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1067">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1068">Az.Sql</span></span>
* <span data-ttu-id="482b4-1069">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="482b4-1069">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="482b4-1070">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-1070">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="482b4-1071">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-1071">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="482b4-1072">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="482b4-1072">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="482b4-1073">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="482b4-1073">Remove an LTR backup</span></span>
    - <span data-ttu-id="482b4-1074">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-1074">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="482b4-1075">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="482b4-1075">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="482b4-1076">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="482b4-1076">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="482b4-1077">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="482b4-1077">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1078">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1078">Az.Storage</span></span>
* <span data-ttu-id="482b4-1079">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-1079">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="482b4-1080">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-1080">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="482b4-1081">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="482b4-1081">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="482b4-1082">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="482b4-1082">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="482b4-1083">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="482b4-1083">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-1084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-1084">Az.Websites</span></span>
* <span data-ttu-id="482b4-1085">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="482b4-1085">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="482b4-1086">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="482b4-1086">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="482b4-1087">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="482b4-1087">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="482b4-1088">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1088">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="482b4-1089">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="482b4-1089">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="482b4-1090">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1090">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="482b4-1091">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-1091">Highlights since the last major release</span></span>
* <span data-ttu-id="482b4-1092">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="482b4-1092">Updated client side telemetry.</span></span>
* <span data-ttu-id="482b4-1093">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="482b4-1093">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="482b4-1094">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="482b4-1094">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-1095">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1095">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1096">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1096">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-1097">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-1097">Az.Automation</span></span>
* <span data-ttu-id="482b4-1098">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-1098">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-1100">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1100">Updated SDK to 7.0</span></span>
* <span data-ttu-id="482b4-1101">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="482b4-1101">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1102">Az.Compute</span></span>
* <span data-ttu-id="482b4-1103">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="482b4-1103">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-1104">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-1104">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-1105">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="482b4-1105">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-1106">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1106">Az.IotHub</span></span>
* <span data-ttu-id="482b4-1107">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1107">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="482b4-1108">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="482b4-1108">New Cmdlets are:</span></span>
    - <span data-ttu-id="482b4-1109">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1109">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="482b4-1110">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1110">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="482b4-1111">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1111">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="482b4-1112">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="482b4-1112">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-1113">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-1114">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1114">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-1115">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-1115">Az.Monitor</span></span>
* <span data-ttu-id="482b4-1116">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="482b4-1116">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="482b4-1117">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="482b4-1117">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="482b4-1118">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="482b4-1118">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1119">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1119">Az.Network</span></span>
* <span data-ttu-id="482b4-1120">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="482b4-1120">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="482b4-1121">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1121">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="482b4-1122">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1122">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="482b4-1123">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-1123">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="482b4-1124">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="482b4-1124">No new cmdlets are added.</span></span> <span data-ttu-id="482b4-1125">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1125">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1126">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1127">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="482b4-1127">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1128">Az.Resources</span></span>
* <span data-ttu-id="482b4-1129">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="482b4-1129">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="482b4-1130">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-1130">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="482b4-1131">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-1131">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="482b4-1132">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-1132">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="482b4-1133">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-1133">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="482b4-1134">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="482b4-1134">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="482b4-1135">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="482b4-1135">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="482b4-1136">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-1136">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1137">Az.Sql</span></span>
* <span data-ttu-id="482b4-1138">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="482b4-1138">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="482b4-1139">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="482b4-1139">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="482b4-1140">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="482b4-1140">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="482b4-1141">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="482b4-1141">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="482b4-1142">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="482b4-1142">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="482b4-1143">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="482b4-1143">Az.StorageSync</span></span>
* <span data-ttu-id="482b4-1144">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1144">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="482b4-1145">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1145">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="482b4-1146">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-1146">Highlights since the last major release</span></span>
* <span data-ttu-id="482b4-1147">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="482b4-1147">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="482b4-1148">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="482b4-1148">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1149">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1150">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="482b4-1150">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="482b4-1151">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="482b4-1151">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-1152">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-1152">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-1153">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="482b4-1153">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="482b4-1154">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="482b4-1154">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="482b4-1155">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="482b4-1155">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="482b4-1156">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="482b4-1156">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1157">Az.Compute</span></span>
* <span data-ttu-id="482b4-1158">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="482b4-1158">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="482b4-1159">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="482b4-1159">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="482b4-1160">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1160">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="482b4-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="482b4-1162">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-1162">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1163">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1163">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1164">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1164">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="482b4-1165">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="482b4-1165">Az.DeploymentManager</span></span>
* <span data-ttu-id="482b4-1166">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="482b4-1166">Adds LIST operations for resources</span></span>
* <span data-ttu-id="482b4-1167">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="482b4-1167">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-1168">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-1168">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-1169">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="482b4-1169">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-1170">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-1170">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-1171">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="482b4-1171">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1172">Az.Network</span></span>
* <span data-ttu-id="482b4-1173">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="482b4-1173">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="482b4-1174">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="482b4-1174">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="482b4-1175">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="482b4-1175">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="482b4-1176">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="482b4-1176">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="482b4-1177">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="482b4-1177">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="482b4-1178">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1178">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="482b4-1179">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="482b4-1179">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="482b4-1180">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1180">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="482b4-1181">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1181">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="482b4-1183">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-1183">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="482b4-1184">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="482b4-1184">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="482b4-1185">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="482b4-1185">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-1186">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-1186">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-1187">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="482b4-1187">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="482b4-1188">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="482b4-1188">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="482b4-1189">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="482b4-1189">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="482b4-1190">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="482b4-1190">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1191">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1191">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1192">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="482b4-1192">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="482b4-1193">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="482b4-1193">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1194">Az.Resources</span></span>
* <span data-ttu-id="482b4-1195">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="482b4-1195">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="482b4-1196">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="482b4-1196">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1197">Az.Sql</span></span>
<span data-ttu-id="482b4-1198">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="482b4-1198">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1199">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1199">Az.Storage</span></span>
* <span data-ttu-id="482b4-1200">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="482b4-1200">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="482b4-1201">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-1201">New-AzStorageAccount</span></span>
* <span data-ttu-id="482b4-1202">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="482b4-1202">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="482b4-1203">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-1203">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-1204">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-1204">Az.Websites</span></span>
* <span data-ttu-id="482b4-1205">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="482b4-1205">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="482b4-1206">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="482b4-1206">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="482b4-1207">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1207">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-1208">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1208">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1209">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="482b4-1209">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="482b4-1210">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-1210">Az.Cdn</span></span>
* <span data-ttu-id="482b4-1211">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="482b4-1211">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1212">Az.Compute</span></span>
* <span data-ttu-id="482b4-1213">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="482b4-1213">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="482b4-1214">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="482b4-1214">Az.ContainerInstance</span></span>
* <span data-ttu-id="482b4-1215">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-1215">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="482b4-1216">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="482b4-1216">Az.DataBoxEdge</span></span>
* <span data-ttu-id="482b4-1217">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="482b4-1217">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="482b4-1218">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1218">Get the Edge Storage Container</span></span>
* <span data-ttu-id="482b4-1219">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="482b4-1219">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="482b4-1220">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1220">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="482b4-1221">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="482b4-1221">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="482b4-1222">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1222">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="482b4-1223">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="482b4-1223">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="482b4-1224">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1224">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="482b4-1225">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="482b4-1225">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="482b4-1226">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1226">Get the Edge Storage Account</span></span>
* <span data-ttu-id="482b4-1227">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="482b4-1227">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="482b4-1228">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1228">Create new Edge Storage Account</span></span>
* <span data-ttu-id="482b4-1229">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="482b4-1229">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="482b4-1230">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1230">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="482b4-1231">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="482b4-1231">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="482b4-1232">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="482b4-1232">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="482b4-1233">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="482b4-1233">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="482b4-1234">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="482b4-1234">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1235">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1235">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1236">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="482b4-1236">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="482b4-1237">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1237">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="482b4-1238">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="482b4-1238">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="482b4-1239">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="482b4-1239">Az.DevTestLabs</span></span>
* <span data-ttu-id="482b4-1240">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1240">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-1241">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1241">Az.EventHub</span></span>
* <span data-ttu-id="482b4-1242">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="482b4-1242">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-1243">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-1243">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-1244">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1244">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="482b4-1245">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="482b4-1245">Az.MachineLearning</span></span>
* <span data-ttu-id="482b4-1246">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1246">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="482b4-1247">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="482b4-1247">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="482b4-1248">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="482b4-1248">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="482b4-1249">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="482b4-1249">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="482b4-1250">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="482b4-1250">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="482b4-1251">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="482b4-1251">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="482b4-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="482b4-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="482b4-1253">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="482b4-1253">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1254">Az.Network</span></span>
* <span data-ttu-id="482b4-1255">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="482b4-1255">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1256">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1256">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1257">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1257">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="482b4-1258">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1258">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="482b4-1259">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1259">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="482b4-1260">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1260">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1261">Az.Resources</span></span>
* <span data-ttu-id="482b4-1262">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="482b4-1262">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1263">Az.Sql</span></span>
* <span data-ttu-id="482b4-1264">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1264">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="482b4-1265">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="482b4-1265">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="482b4-1266">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="482b4-1266">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="482b4-1267">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="482b4-1267">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1268">Az.Storage</span></span>
* <span data-ttu-id="482b4-1269">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="482b4-1269">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="482b4-1270">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-1270">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="482b4-1271">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="482b4-1271">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="482b4-1272">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="482b4-1272">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="482b4-1273">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1273">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="482b4-1274">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-1274">General</span></span>
* <span data-ttu-id="482b4-1275">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="482b4-1275">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-1276">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1276">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1277">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="482b4-1277">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="482b4-1278">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="482b4-1278">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="482b4-1279">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-1279">Az.Batch</span></span>
* <span data-ttu-id="482b4-1280">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="482b4-1280">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1281">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1282">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1282">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-1283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-1283">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-1284">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="482b4-1284">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="482b4-1285">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1285">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="482b4-1286">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="482b4-1286">Az.HealthcareApis</span></span>
* <span data-ttu-id="482b4-1287">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="482b4-1287">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-1288">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-1289">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="482b4-1289">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="482b4-1290">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="482b4-1290">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="482b4-1291">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1291">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-1292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-1292">Az.Monitor</span></span>
* <span data-ttu-id="482b4-1293">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="482b4-1293">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="482b4-1294">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="482b4-1294">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="482b4-1295">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="482b4-1295">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1296">Az.Network</span></span>
* <span data-ttu-id="482b4-1297">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="482b4-1297">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1298">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1298">Az.Resources</span></span>
* <span data-ttu-id="482b4-1299">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1299">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="482b4-1300">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="482b4-1300">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1301">Az.Sql</span></span>
* <span data-ttu-id="482b4-1302">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="482b4-1302">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1303">Az.Storage</span></span>
* <span data-ttu-id="482b4-1304">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="482b4-1304">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="482b4-1305">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="482b4-1305">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="482b4-1306">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="482b4-1306">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="482b4-1307">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="482b4-1307">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="482b4-1308">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="482b4-1308">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="482b4-1309">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-1309">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="482b4-1310">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="482b4-1310">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="482b4-1311">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="482b4-1311">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="482b4-1312">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="482b4-1312">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="482b4-1313">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="482b4-1313">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="482b4-1314">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="482b4-1314">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="482b4-1315">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="482b4-1315">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="482b4-1316">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="482b4-1316">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="482b4-1317">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1317">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="482b4-1318">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-1318">Highlights since the last major release</span></span>
* <span data-ttu-id="482b4-1319">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="482b4-1319">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="482b4-1320">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="482b4-1320">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1321">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1321">Az.Compute</span></span>
* <span data-ttu-id="482b4-1322">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="482b4-1322">VM Reapply feature</span></span>
    - <span data-ttu-id="482b4-1323">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-1323">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="482b4-1324">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="482b4-1324">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="482b4-1325">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="482b4-1325">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="482b4-1326">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-1326">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="482b4-1327">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-1327">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="482b4-1328">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="482b4-1328">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="482b4-1329">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="482b4-1329">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="482b4-1330">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="482b4-1330">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="482b4-1331">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="482b4-1331">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="482b4-1332">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-1332">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="482b4-1333">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="482b4-1333">Az.DataBoxEdge</span></span>
* <span data-ttu-id="482b4-1334">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1334">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="482b4-1335">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="482b4-1335">Get the Order</span></span>
* <span data-ttu-id="482b4-1336">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1336">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="482b4-1337">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="482b4-1337">Create new Order</span></span>
* <span data-ttu-id="482b4-1338">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1338">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="482b4-1339">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="482b4-1339">Remove the Order</span></span>
* <span data-ttu-id="482b4-1340">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1340">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="482b4-1341">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="482b4-1341">Now creates Local Share</span></span>
* <span data-ttu-id="482b4-1342">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1342">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="482b4-1343">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="482b4-1343">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="482b4-1344">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1344">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="482b4-1345">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="482b4-1345">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="482b4-1346">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1346">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="482b4-1347">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="482b4-1347">Gets the information about Triggers</span></span>
* <span data-ttu-id="482b4-1348">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1348">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="482b4-1349">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="482b4-1349">Create new Triggers</span></span>
* <span data-ttu-id="482b4-1350">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1350">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="482b4-1351">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="482b4-1351">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1352">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1353">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1353">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="482b4-1354">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="482b4-1354">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-1355">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-1355">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-1356">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="482b4-1356">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-1357">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1357">Az.EventHub</span></span>
* <span data-ttu-id="482b4-1358">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="482b4-1358">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-1359">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-1359">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-1360">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-1360">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="482b4-1361">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-1361">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="482b4-1362">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="482b4-1362">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="482b4-1363">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="482b4-1363">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1364">Az.Network</span></span>
* <span data-ttu-id="482b4-1365">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1365">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="482b4-1366">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="482b4-1366">Az.PrivateDns</span></span>
* <span data-ttu-id="482b4-1367">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="482b4-1367">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1368">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1369">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="482b4-1369">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="482b4-1370">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="482b4-1370">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="482b4-1371">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="482b4-1371">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="482b4-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="482b4-1372">Az.RedisCache</span></span>
* <span data-ttu-id="482b4-1373">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="482b4-1373">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="482b4-1374">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="482b4-1374">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="482b4-1375">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="482b4-1375">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1376">Az.Resources</span></span>
- <span data-ttu-id="482b4-1377">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="482b4-1377">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="482b4-1378">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="482b4-1378">Updated create policy definition help example</span></span>
- <span data-ttu-id="482b4-1379">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="482b4-1379">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="482b4-1380">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-1380">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="482b4-1381">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1381">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1382">Az.Sql</span></span>
* <span data-ttu-id="482b4-1383">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-1383">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="482b4-1384">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="482b4-1384">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="482b4-1385">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1385">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="482b4-1386">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-1386">General</span></span>
* <span data-ttu-id="482b4-1387">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="482b4-1387">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-1388">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1388">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1389">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="482b4-1389">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="482b4-1390">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="482b4-1390">Az.Advisor</span></span>
* <span data-ttu-id="482b4-1391">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="482b4-1391">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="482b4-1392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-1392">Az.Batch</span></span>
* <span data-ttu-id="482b4-1393">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1393">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="482b4-1394">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1394">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="482b4-1395">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1395">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="482b4-1396">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1396">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="482b4-1397">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1397">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="482b4-1398">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1398">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="482b4-1399">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="482b4-1399">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="482b4-1400">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="482b4-1400">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="482b4-1401">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="482b4-1401">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="482b4-1402">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1402">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="482b4-1403">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1403">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="482b4-1404">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1404">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="482b4-1405">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1405">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="482b4-1406">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1406">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="482b4-1407">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1407">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="482b4-1408">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1408">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="482b4-1409">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1409">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="482b4-1410">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1410">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="482b4-1411">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1411">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="482b4-1412">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="482b4-1412">This operation is no longer supported.</span></span>
* <span data-ttu-id="482b4-1413">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1413">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="482b4-1414">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1414">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="482b4-1415">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1415">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="482b4-1416">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1416">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="482b4-1417">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="482b4-1417">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="482b4-1418">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="482b4-1418">New non-verified images are also now returned.</span></span> <span data-ttu-id="482b4-1419">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="482b4-1419">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="482b4-1420">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1420">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="482b4-1421">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="482b4-1421">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="482b4-1422">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1422">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="482b4-1423">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="482b4-1423">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="482b4-1424">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1424">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="482b4-1425">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1425">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="482b4-1426">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="482b4-1426">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="482b4-1427">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="482b4-1427">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="482b4-1428">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="482b4-1428">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="482b4-1429">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-1429">Az.Cdn</span></span>
* <span data-ttu-id="482b4-1430">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="482b4-1430">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="482b4-1431">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="482b4-1431">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1432">Az.Compute</span></span>
* <span data-ttu-id="482b4-1433">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="482b4-1433">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="482b4-1434">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="482b4-1434">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="482b4-1435">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="482b4-1435">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="482b4-1436">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-1436">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="482b4-1437">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-1437">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="482b4-1438">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="482b4-1438">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="482b4-1439">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="482b4-1439">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="482b4-1440">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="482b4-1440">Breaking changes</span></span>
    - <span data-ttu-id="482b4-1441">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="482b4-1441">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="482b4-1442">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="482b4-1442">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1443">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1444">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1444">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-1445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-1445">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-1446">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="482b4-1446">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="482b4-1447">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="482b4-1447">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="482b4-1448">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="482b4-1448">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="482b4-1449">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="482b4-1449">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="482b4-1450">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="482b4-1450">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="482b4-1451">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="482b4-1451">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-1452">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-1452">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-1453">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="482b4-1453">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-1454">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-1454">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-1455">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="482b4-1455">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="482b4-1456">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="482b4-1456">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="482b4-1457">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="482b4-1457">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="482b4-1458">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="482b4-1458">Removed five cmdlets:</span></span>
    - <span data-ttu-id="482b4-1459">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="482b4-1459">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="482b4-1460">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="482b4-1460">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="482b4-1461">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="482b4-1461">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="482b4-1462">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="482b4-1462">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="482b4-1463">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="482b4-1463">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="482b4-1464">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="482b4-1464">Added three cmdlets:</span></span>
    - <span data-ttu-id="482b4-1465">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="482b4-1465">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="482b4-1466">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="482b4-1466">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="482b4-1467">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="482b4-1467">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="482b4-1468">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1468">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="482b4-1469">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="482b4-1469">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="482b4-1470">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="482b4-1470">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="482b4-1471">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="482b4-1471">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="482b4-1472">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="482b4-1472">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="482b4-1473">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="482b4-1473">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="482b4-1474">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="482b4-1474">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="482b4-1475">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="482b4-1475">Added some scenario test cases.</span></span>
* <span data-ttu-id="482b4-1476">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="482b4-1476">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-1477">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1477">Az.IotHub</span></span>
* <span data-ttu-id="482b4-1478">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="482b4-1478">Breaking changes:</span></span>
    - <span data-ttu-id="482b4-1479">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1479">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="482b4-1480">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-1480">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="482b4-1481">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1481">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="482b4-1482">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-1482">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="482b4-1483">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="482b4-1483">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="482b4-1484">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="482b4-1484">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="482b4-1485">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="482b4-1485">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="482b4-1486">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="482b4-1486">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="482b4-1487">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1487">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="482b4-1488">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-1488">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="482b4-1489">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1489">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="482b4-1490">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="482b4-1490">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1491">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1491">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1492">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1492">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="482b4-1493">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1493">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="482b4-1494">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1494">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="482b4-1495">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1495">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="482b4-1496">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1496">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="482b4-1497">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1497">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="482b4-1498">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1498">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="482b4-1499">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1499">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="482b4-1500">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="482b4-1500">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1501">Az.Resources</span></span>
* <span data-ttu-id="482b4-1502">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="482b4-1502">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1503">Az.Network</span></span>
* <span data-ttu-id="482b4-1504">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="482b4-1504">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="482b4-1505">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="482b4-1505">Updated cmdlet:</span></span>
        - <span data-ttu-id="482b4-1506">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1506">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1507">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1507">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1508">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1508">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1509">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1509">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1510">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-1510">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="482b4-1511">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="482b4-1511">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="482b4-1512">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="482b4-1512">New cmdlet:</span></span>
        - <span data-ttu-id="482b4-1513">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="482b4-1513">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="482b4-1514">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="482b4-1514">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="482b4-1515">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="482b4-1515">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="482b4-1516">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-1516">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="482b4-1517">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="482b4-1517">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="482b4-1518">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="482b4-1518">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="482b4-1519">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="482b4-1519">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="482b4-1520">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1520">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="482b4-1521">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1521">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-1522">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="482b4-1522">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="482b4-1523">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-1523">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="482b4-1524">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-1524">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="482b4-1525">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-1525">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="482b4-1526">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1526">Set-AzVirtualHub</span></span>
* <span data-ttu-id="482b4-1527">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="482b4-1527">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="482b4-1528">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="482b4-1528">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="482b4-1529">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="482b4-1529">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="482b4-1530">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="482b4-1530">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="482b4-1531">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="482b4-1531">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="482b4-1532">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="482b4-1532">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="482b4-1533">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-1533">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="482b4-1534">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1534">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-1535">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-1535">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="482b4-1536">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="482b4-1536">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="482b4-1537">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="482b4-1537">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="482b4-1538">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="482b4-1538">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="482b4-1539">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="482b4-1539">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="482b4-1540">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="482b4-1540">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="482b4-1541">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="482b4-1541">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="482b4-1542">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="482b4-1542">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="482b4-1543">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1543">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-1544">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="482b4-1544">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="482b4-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="482b4-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="482b4-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="482b4-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="482b4-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="482b4-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="482b4-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="482b4-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="482b4-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="482b4-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="482b4-1550">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="482b4-1550">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="482b4-1551">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="482b4-1551">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="482b4-1552">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="482b4-1552">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="482b4-1553">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="482b4-1553">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="482b4-1554">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="482b4-1554">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="482b4-1555">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="482b4-1555">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="482b4-1556">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="482b4-1556">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="482b4-1557">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="482b4-1557">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="482b4-1558">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="482b4-1558">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="482b4-1559">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="482b4-1559">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="482b4-1560">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="482b4-1560">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="482b4-1561">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1561">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-1562">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="482b4-1562">New-AzIpGroup</span></span>
        - <span data-ttu-id="482b4-1563">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="482b4-1563">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="482b4-1564">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="482b4-1564">Get-AzIpGroup</span></span>
        - <span data-ttu-id="482b4-1565">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="482b4-1565">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-1566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-1566">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-1567">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="482b4-1567">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1568">Az.Sql</span></span>
* <span data-ttu-id="482b4-1569">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="482b4-1569">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="482b4-1570">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="482b4-1570">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="482b4-1571">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="482b4-1571">Removed deprecated aliases:</span></span>
* <span data-ttu-id="482b4-1572">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="482b4-1572">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="482b4-1573">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="482b4-1573">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="482b4-1574">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-1574">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="482b4-1575">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="482b4-1575">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="482b4-1576">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="482b4-1576">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="482b4-1577">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-1577">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1578">Az.Storage</span></span>
* <span data-ttu-id="482b4-1579">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="482b4-1579">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="482b4-1580">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-1580">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="482b4-1581">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-1581">Set-AzStorageAccount</span></span>
* <span data-ttu-id="482b4-1582">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="482b4-1582">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="482b4-1583">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="482b4-1583">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="482b4-1584">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="482b4-1584">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="482b4-1585">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1585">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="482b4-1586">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-1586">General</span></span>
* <span data-ttu-id="482b4-1587">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="482b4-1587">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1588">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1589">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="482b4-1589">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-1590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-1590">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-1591">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="482b4-1591">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="482b4-1592">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="482b4-1592">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-1593">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-1593">Az.Automation</span></span>
* <span data-ttu-id="482b4-1594">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="482b4-1594">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="482b4-1595">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-1595">Az.Batch</span></span>
* <span data-ttu-id="482b4-1596">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1596">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1597">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1597">Az.Compute</span></span>
* <span data-ttu-id="482b4-1598">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="482b4-1598">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="482b4-1599">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="482b4-1599">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="482b4-1600">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="482b4-1600">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="482b4-1601">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="482b4-1601">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1602">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1602">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1603">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="482b4-1603">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="482b4-1604">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="482b4-1604">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="482b4-1605">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1605">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-1606">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-1606">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-1607">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="482b4-1607">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="482b4-1608">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="482b4-1608">Az.HealthcareApis</span></span>
* <span data-ttu-id="482b4-1609">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1609">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="482b4-1610">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="482b4-1610">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="482b4-1611">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="482b4-1611">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="482b4-1612">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="482b4-1612">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-1613">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1613">Az.IotHub</span></span>
* <span data-ttu-id="482b4-1614">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="482b4-1614">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="482b4-1615">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="482b4-1615">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-1616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-1616">Az.Monitor</span></span>
* <span data-ttu-id="482b4-1617">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="482b4-1617">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="482b4-1618">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="482b4-1618">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="482b4-1619">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="482b4-1619">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="482b4-1620">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="482b4-1620">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1621">Az.Network</span></span>
* <span data-ttu-id="482b4-1622">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="482b4-1622">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="482b4-1623">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="482b4-1623">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="482b4-1624">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1624">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-1625">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-1625">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="482b4-1626">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1626">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="482b4-1627">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="482b4-1627">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="482b4-1628">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1628">Updated cmdlets:</span></span>
        - <span data-ttu-id="482b4-1629">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1629">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="482b4-1630">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1630">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="482b4-1631">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1631">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="482b4-1632">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="482b4-1632">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="482b4-1633">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="482b4-1633">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="482b4-1634">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="482b4-1634">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="482b4-1635">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="482b4-1635">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="482b4-1636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="482b4-1636">Az.RedisCache</span></span>
* <span data-ttu-id="482b4-1637">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="482b4-1637">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1638">Az.Sql</span></span>
* <span data-ttu-id="482b4-1639">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="482b4-1639">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1640">Az.Storage</span></span>
* <span data-ttu-id="482b4-1641">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1641">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="482b4-1642">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="482b4-1642">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="482b4-1643">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="482b4-1643">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="482b4-1644">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-1644">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="482b4-1645">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-1645">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="482b4-1646">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="482b4-1646">Az.StorageSync</span></span>
* <span data-ttu-id="482b4-1647">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="482b4-1647">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-1648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-1648">Az.Websites</span></span>
* <span data-ttu-id="482b4-1649">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1649">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="482b4-1650">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1650">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="482b4-1651">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-1651">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-1652">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="482b4-1652">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="482b4-1653">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-1653">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="482b4-1654">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="482b4-1654">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-1655">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-1655">Az.Automation</span></span>
* <span data-ttu-id="482b4-1656">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="482b4-1656">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="482b4-1657">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="482b4-1657">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="482b4-1658">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="482b4-1658">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1659">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1659">Az.Compute</span></span>
* <span data-ttu-id="482b4-1660">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1660">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="482b4-1661">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1661">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="482b4-1662">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="482b4-1662">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="482b4-1663">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="482b4-1663">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="482b4-1664">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="482b4-1664">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="482b4-1665">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="482b4-1665">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="482b4-1666">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="482b4-1666">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="482b4-1667">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="482b4-1667">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="482b4-1668">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-1668">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1669">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1669">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1670">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="482b4-1670">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="482b4-1671">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="482b4-1671">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-1672">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-1672">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-1673">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1673">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-1674">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1674">Az.IotHub</span></span>
* <span data-ttu-id="482b4-1675">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="482b4-1675">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="482b4-1676">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="482b4-1676">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="482b4-1677">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-1677">New cmdlets are:</span></span>
    - <span data-ttu-id="482b4-1678">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="482b4-1678">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="482b4-1679">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="482b4-1679">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="482b4-1680">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="482b4-1680">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="482b4-1681">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="482b4-1681">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-1682">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-1682">Az.Monitor</span></span>
* <span data-ttu-id="482b4-1683">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="482b4-1683">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="482b4-1684">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="482b4-1684">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="482b4-1685">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="482b4-1685">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="482b4-1686">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1686">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="482b4-1687">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="482b4-1687">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="482b4-1688">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="482b4-1688">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="482b4-1689">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1689">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="482b4-1690">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1690">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="482b4-1691">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="482b4-1691">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="482b4-1692">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="482b4-1692">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="482b4-1693">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="482b4-1693">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="482b4-1694">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="482b4-1694">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="482b4-1695">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="482b4-1695">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="482b4-1696">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="482b4-1696">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="482b4-1697">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="482b4-1697">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="482b4-1698">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="482b4-1698">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="482b4-1699">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="482b4-1699">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="482b4-1700">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="482b4-1700">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="482b4-1701">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-1701">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="482b4-1702">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="482b4-1702">Overall improved help files</span></span>
* <span data-ttu-id="482b4-1703">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="482b4-1703">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1704">Az.Network</span></span>
* <span data-ttu-id="482b4-1705">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-1705">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="482b4-1706">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1706">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="482b4-1707">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="482b4-1707">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="482b4-1708">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="482b4-1708">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="482b4-1709">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="482b4-1709">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="482b4-1710">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="482b4-1710">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="482b4-1711">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="482b4-1711">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="482b4-1712">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="482b4-1712">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="482b4-1713">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="482b4-1713">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="482b4-1714">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="482b4-1714">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="482b4-1715">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1715">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="482b4-1716">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="482b4-1716">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="482b4-1717">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-1717">New cmdlets</span></span>
        - <span data-ttu-id="482b4-1718">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="482b4-1718">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="482b4-1719">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="482b4-1719">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="482b4-1720">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="482b4-1720">Updated cmdlet:</span></span>
        - <span data-ttu-id="482b4-1721">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="482b4-1721">New-VpnSite</span></span>
        - <span data-ttu-id="482b4-1722">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="482b4-1722">Update-VpnSite</span></span>
        - <span data-ttu-id="482b4-1723">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="482b4-1723">New-VpnConnection</span></span>
        - <span data-ttu-id="482b4-1724">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1724">Update-VpnConnection</span></span>
* <span data-ttu-id="482b4-1725">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="482b4-1725">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1726">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1726">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1727">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="482b4-1727">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="482b4-1728">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1728">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1729">Az.Resources</span></span>
* <span data-ttu-id="482b4-1730">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="482b4-1730">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-1731">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-1731">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-1732">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="482b4-1732">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="482b4-1733">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="482b4-1733">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="482b4-1734">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="482b4-1734">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="482b4-1735">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="482b4-1735">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="482b4-1736">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="482b4-1736">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="482b4-1737">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="482b4-1737">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="482b4-1738">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="482b4-1738">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="482b4-1739">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="482b4-1739">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="482b4-1740">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="482b4-1740">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="482b4-1741">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="482b4-1741">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="482b4-1742">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="482b4-1742">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="482b4-1743">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="482b4-1743">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="482b4-1744">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="482b4-1744">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="482b4-1745">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="482b4-1745">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="482b4-1746">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="482b4-1746">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="482b4-1747">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="482b4-1747">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="482b4-1748">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="482b4-1748">Az.SignalR</span></span>
* <span data-ttu-id="482b4-1749">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="482b4-1749">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1750">Az.Sql</span></span>
* <span data-ttu-id="482b4-1751">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="482b4-1751">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="482b4-1752">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="482b4-1752">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="482b4-1753">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-1753">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="482b4-1754">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="482b4-1754">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="482b4-1755">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="482b4-1755">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1756">Az.Storage</span></span>
* <span data-ttu-id="482b4-1757">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="482b4-1757">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="482b4-1758">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="482b4-1758">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="482b4-1759">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="482b4-1759">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="482b4-1760">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="482b4-1760">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="482b4-1761">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-1761">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="482b4-1762">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="482b4-1762">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="482b4-1763">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="482b4-1763">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="482b4-1764">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="482b4-1764">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="482b4-1765">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="482b4-1765">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="482b4-1766">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="482b4-1766">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="482b4-1767">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="482b4-1767">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-1768">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-1768">Az.Websites</span></span>
* <span data-ttu-id="482b4-1769">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="482b4-1769">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="482b4-1770">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="482b4-1770">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="482b4-1771">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="482b4-1771">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="482b4-1772">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1772">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="482b4-1773">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-1773">General</span></span>
* <span data-ttu-id="482b4-1774">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="482b4-1774">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-1775">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1775">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1776">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="482b4-1776">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="482b4-1777">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="482b4-1777">Az.Aks</span></span>
* <span data-ttu-id="482b4-1778">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="482b4-1778">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="482b4-1779">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="482b4-1779">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-1780">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-1780">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-1781">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="482b4-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="482b4-1782">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="482b4-1782">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="482b4-1783">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="482b4-1783">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="482b4-1784">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="482b4-1784">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="482b4-1785">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="482b4-1785">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="482b4-1786">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-1786">Az.Batch</span></span>
* <span data-ttu-id="482b4-1787">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="482b4-1787">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="482b4-1788">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-1788">Az.Cdn</span></span>
* <span data-ttu-id="482b4-1789">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="482b4-1789">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1790">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1790">Az.Compute</span></span>
* <span data-ttu-id="482b4-1791">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1791">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="482b4-1792">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-1792">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="482b4-1793">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="482b4-1793">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="482b4-1794">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-1794">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="482b4-1795">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="482b4-1795">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="482b4-1796">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-1796">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="482b4-1797">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1797">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="482b4-1798">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="482b4-1798">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1799">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1800">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="482b4-1800">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="482b4-1801">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="482b4-1801">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="482b4-1802">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="482b4-1802">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="482b4-1803">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="482b4-1803">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-1804">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-1804">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-1805">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="482b4-1805">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-1806">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1806">Az.EventHub</span></span>
* <span data-ttu-id="482b4-1807">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-1807">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="482b4-1808">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="482b4-1808">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="482b4-1809">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="482b4-1809">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="482b4-1810">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="482b4-1810">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="482b4-1811">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="482b4-1811">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="482b4-1812">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="482b4-1812">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-1813">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-1813">Az.Monitor</span></span>
* <span data-ttu-id="482b4-1814">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="482b4-1814">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1815">Az.Network</span></span>
* <span data-ttu-id="482b4-1816">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1816">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="482b4-1817">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="482b4-1817">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="482b4-1818">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="482b4-1818">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="482b4-1819">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="482b4-1819">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="482b4-1820">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="482b4-1820">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="482b4-1821">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="482b4-1821">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="482b4-1822">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="482b4-1822">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-1823">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-1823">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-1824">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="482b4-1824">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="482b4-1825">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="482b4-1825">Added example</span></span>
    - <span data-ttu-id="482b4-1826">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="482b4-1826">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="482b4-1827">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="482b4-1827">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="482b4-1828">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="482b4-1828">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1829">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1830">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1830">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1831">Az.Resources</span></span>
* <span data-ttu-id="482b4-1832">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="482b4-1832">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="482b4-1833">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="482b4-1833">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="482b4-1834">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="482b4-1834">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="482b4-1835">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-1835">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="482b4-1836">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="482b4-1836">Az.ServiceBus</span></span>
* <span data-ttu-id="482b4-1837">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-1837">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="482b4-1838">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="482b4-1838">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="482b4-1839">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="482b4-1839">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-1840">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-1840">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-1841">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="482b4-1841">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="482b4-1842">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="482b4-1842">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="482b4-1843">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="482b4-1843">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="482b4-1844">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="482b4-1844">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="482b4-1845">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="482b4-1845">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="482b4-1846">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="482b4-1846">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1847">Az.Sql</span></span>
* <span data-ttu-id="482b4-1848">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="482b4-1848">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1849">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1849">Az.Storage</span></span>
* <span data-ttu-id="482b4-1850">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="482b4-1850">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="482b4-1851">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="482b4-1851">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="482b4-1852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="482b4-1852">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="482b4-1853">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-1853">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="482b4-1854">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="482b4-1854">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="482b4-1855">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-1855">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-1856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-1856">Az.Websites</span></span>
* <span data-ttu-id="482b4-1857">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="482b4-1857">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="482b4-1858">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1858">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-1859">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1859">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1860">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="482b4-1860">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="482b4-1861">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-1861">Az.ApplicationInsights</span></span>
* <span data-ttu-id="482b4-1862">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="482b4-1862">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-1863">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-1863">Az.Automation</span></span>
* <span data-ttu-id="482b4-1864">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="482b4-1864">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-1865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1865">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-1866">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-1866">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1867">Az.Compute</span></span>
* <span data-ttu-id="482b4-1868">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="482b4-1868">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="482b4-1869">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="482b4-1869">Az.ContainerRegistry</span></span>
* <span data-ttu-id="482b4-1870">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="482b4-1870">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="482b4-1871">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="482b4-1871">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1872">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1873">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-1873">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="482b4-1874">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="482b4-1874">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-1875">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1875">Az.EventHub</span></span>
* <span data-ttu-id="482b4-1876">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="482b4-1876">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="482b4-1877">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="482b4-1877">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-1878">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-1878">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-1879">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1879">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="482b4-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="482b4-1880">Az.LogicApp</span></span>
* <span data-ttu-id="482b4-1881">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="482b4-1881">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="482b4-1882">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="482b4-1882">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="482b4-1883">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1883">Az.ManagedServices</span></span>
* <span data-ttu-id="482b4-1884">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="482b4-1884">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1885">Az.Network</span></span>
* <span data-ttu-id="482b4-1886">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="482b4-1886">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="482b4-1887">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-1887">New cmdlets</span></span>
        - <span data-ttu-id="482b4-1888">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="482b4-1888">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="482b4-1889">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="482b4-1889">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="482b4-1890">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1890">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1891">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1891">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1892">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1892">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1893">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1893">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="482b4-1894">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="482b4-1894">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="482b4-1895">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="482b4-1895">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="482b4-1896">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-1896">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="482b4-1897">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1897">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="482b4-1898">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="482b4-1898">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="482b4-1899">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="482b4-1899">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="482b4-1900">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="482b4-1900">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="482b4-1901">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-1901">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="482b4-1902">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-1902">Updated cmdlets</span></span>
        - <span data-ttu-id="482b4-1903">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1903">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="482b4-1904">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1904">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="482b4-1905">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1905">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="482b4-1906">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1906">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="482b4-1907">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-1907">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="482b4-1908">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="482b4-1908">Updated cmdlet:</span></span>
        - <span data-ttu-id="482b4-1909">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1909">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="482b4-1910">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1910">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="482b4-1911">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="482b4-1911">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="482b4-1912">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="482b4-1912">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="482b4-1913">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="482b4-1913">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="482b4-1914">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="482b4-1914">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-1915">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-1915">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-1916">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="482b4-1916">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="482b4-1917">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="482b4-1917">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1918">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1918">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1919">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1919">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="482b4-1920">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1920">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="482b4-1921">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1921">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="482b4-1922">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1922">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="482b4-1923">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1923">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="482b4-1924">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1924">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="482b4-1925">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1925">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="482b4-1926">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1926">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="482b4-1927">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-1927">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="482b4-1928">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="482b4-1928">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1929">Az.Resources</span></span>
- <span data-ttu-id="482b4-1930">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-1930">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="482b4-1931">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-1931">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="482b4-1932">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="482b4-1932">Az.ServiceBus</span></span>
* <span data-ttu-id="482b4-1933">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="482b4-1933">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="482b4-1934">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="482b4-1934">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1935">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1935">Az.Sql</span></span>
* <span data-ttu-id="482b4-1936">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="482b4-1936">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="482b4-1937">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="482b4-1937">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="482b4-1938">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1938">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-1939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-1939">Az.Storage</span></span>
* <span data-ttu-id="482b4-1940">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1940">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="482b4-1941">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="482b4-1941">Az.StorageSync</span></span>
* <span data-ttu-id="482b4-1942">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="482b4-1942">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="482b4-1943">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="482b4-1943">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-1944">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-1944">Az.Websites</span></span>
* <span data-ttu-id="482b4-1945">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="482b4-1945">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="482b4-1946">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="482b4-1946">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="482b4-1947">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="482b4-1947">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="482b4-1948">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-1948">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-1949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-1949">Az.Accounts</span></span>
* <span data-ttu-id="482b4-1950">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="482b4-1950">Add support for profile cmdlets</span></span>
* <span data-ttu-id="482b4-1951">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="482b4-1951">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="482b4-1952">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="482b4-1952">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="482b4-1953">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="482b4-1953">Az.Advisor</span></span>
* <span data-ttu-id="482b4-1954">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="482b4-1954">GA release of Az.Advisor</span></span>
* <span data-ttu-id="482b4-1955">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="482b4-1955">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="482b4-1956">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-1956">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-1957">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="482b4-1957">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="482b4-1958">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="482b4-1958">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="482b4-1959">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="482b4-1959">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="482b4-1960">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="482b4-1960">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="482b4-1961">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="482b4-1961">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="482b4-1962">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="482b4-1962">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="482b4-1963">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="482b4-1963">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-1964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-1964">Az.Automation</span></span>
* <span data-ttu-id="482b4-1965">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="482b4-1965">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-1966">Az.Compute</span></span>
* <span data-ttu-id="482b4-1967">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="482b4-1967">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-1968">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-1968">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-1969">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="482b4-1969">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="482b4-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="482b4-1970">Az.EventGrid</span></span>
* <span data-ttu-id="482b4-1971">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="482b4-1971">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-1972">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-1972">Az.IotHub</span></span>
* <span data-ttu-id="482b4-1973">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="482b4-1973">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-1974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-1974">Az.Network</span></span>
* <span data-ttu-id="482b4-1975">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="482b4-1975">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="482b4-1976">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="482b4-1976">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-1977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-1977">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-1978">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="482b4-1978">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="482b4-1979">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="482b4-1979">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-1980">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-1980">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-1981">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="482b4-1981">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-1983">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="482b4-1983">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-1984">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-1984">Az.Resources</span></span>
    - <span data-ttu-id="482b4-1985">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="482b4-1985">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="482b4-1986">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="482b4-1986">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="482b4-1987">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-1987">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="482b4-1988">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="482b4-1988">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="482b4-1989">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="482b4-1989">Az.ServiceBus</span></span>
* <span data-ttu-id="482b4-1990">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="482b4-1990">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-1991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-1991">Az.Sql</span></span>
* <span data-ttu-id="482b4-1992">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="482b4-1992">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="482b4-1993">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="482b4-1993">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="482b4-1994">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="482b4-1994">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="482b4-1995">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="482b4-1995">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="482b4-1996">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="482b4-1996">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="482b4-1997">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="482b4-1997">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="482b4-1998">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="482b4-1998">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="482b4-1999">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="482b4-1999">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="482b4-2000">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="482b4-2000">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2001">Az.Storage</span></span>
* <span data-ttu-id="482b4-2002">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="482b4-2002">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="482b4-2003">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="482b4-2003">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="482b4-2004">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="482b4-2004">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="482b4-2005">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="482b4-2005">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="482b4-2006">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="482b4-2006">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="482b4-2007">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2007">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="482b4-2008">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2008">Set-AzStorageAccount</span></span>
* <span data-ttu-id="482b4-2009">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="482b4-2009">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="482b4-2010">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="482b4-2010">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="482b4-2011">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="482b4-2011">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="482b4-2012">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="482b4-2012">Az.StorageSync</span></span>
* <span data-ttu-id="482b4-2013">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2013">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="482b4-2014">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2014">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-2015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2015">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2016">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="482b4-2016">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="482b4-2017">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="482b4-2017">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="482b4-2018">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="482b4-2018">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="482b4-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="482b4-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="482b4-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="482b4-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2021">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2021">Az.Compute</span></span>
* <span data-ttu-id="482b4-2022">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-2022">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="482b4-2023">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-2023">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="482b4-2024">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="482b4-2024">Az.Dns</span></span>
* <span data-ttu-id="482b4-2025">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="482b4-2025">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="482b4-2026">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="482b4-2026">Az.EventGrid</span></span>
* <span data-ttu-id="482b4-2027">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-2027">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="482b4-2028">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-2028">New cmdlets:</span></span>
    - <span data-ttu-id="482b4-2029">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="482b4-2029">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="482b4-2030">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2030">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="482b4-2031">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="482b4-2031">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="482b4-2032">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2032">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="482b4-2033">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="482b4-2033">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="482b4-2034">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2034">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="482b4-2035">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="482b4-2035">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="482b4-2036">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2036">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="482b4-2037">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="482b4-2037">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="482b4-2038">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="482b4-2038">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="482b4-2039">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="482b4-2039">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="482b4-2040">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2040">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="482b4-2041">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="482b4-2041">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="482b4-2042">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2042">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="482b4-2043">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="482b4-2043">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="482b4-2044">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2044">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="482b4-2045">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-2045">Updated cmdlets:</span></span>
    - <span data-ttu-id="482b4-2046">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="482b4-2046">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="482b4-2047">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="482b4-2047">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="482b4-2048">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="482b4-2048">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="482b4-2049">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="482b4-2049">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="482b4-2050">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="482b4-2050">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="482b4-2051">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="482b4-2051">Event subscription expiration date,</span></span>
            - <span data-ttu-id="482b4-2052">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="482b4-2052">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="482b4-2053">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2053">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="482b4-2054">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="482b4-2054">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="482b4-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="482b4-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="482b4-2056">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2056">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="482b4-2057">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="482b4-2057">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="482b4-2058">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="482b4-2058">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="482b4-2059">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="482b4-2059">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-2060">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-2060">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-2061">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="482b4-2061">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="482b4-2062">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="482b4-2062">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="482b4-2063">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="482b4-2063">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="482b4-2064">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2064">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2065">Az.Network</span></span>
* <span data-ttu-id="482b4-2066">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-2066">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="482b4-2067">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-2067">New cmdlets</span></span>
        - <span data-ttu-id="482b4-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="482b4-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="482b4-2069">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="482b4-2069">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="482b4-2070">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-2070">New cmdlets</span></span>
        - <span data-ttu-id="482b4-2071">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="482b4-2071">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="482b4-2072">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="482b4-2072">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="482b4-2073">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-2073">New cmdlets</span></span>
        - <span data-ttu-id="482b4-2074">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="482b4-2074">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="482b4-2075">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="482b4-2075">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="482b4-2076">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="482b4-2076">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="482b4-2077">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-2077">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="482b4-2078">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-2078">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="482b4-2079">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="482b4-2079">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="482b4-2080">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-2080">New cmdlets</span></span>
        - <span data-ttu-id="482b4-2081">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="482b4-2081">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="482b4-2082">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="482b4-2082">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="482b4-2083">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="482b4-2083">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="482b4-2084">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="482b4-2084">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="482b4-2085">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2085">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="482b4-2086">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2086">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="482b4-2087">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2087">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="482b4-2088">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="482b4-2088">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="482b4-2089">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="482b4-2089">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="482b4-2090">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="482b4-2090">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="482b4-2091">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2091">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="482b4-2092">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="482b4-2092">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="482b4-2093">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2093">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="482b4-2094">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="482b4-2094">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="482b4-2095">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="482b4-2095">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="482b4-2096">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="482b4-2096">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="482b4-2097">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="482b4-2097">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="482b4-2098">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2098">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="482b4-2099">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="482b4-2099">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="482b4-2100">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2100">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="482b4-2101">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-2101">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="482b4-2102">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-2102">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="482b4-2103">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="482b4-2103">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="482b4-2104">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-2104">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="482b4-2105">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="482b4-2105">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="482b4-2106">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="482b4-2106">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="482b4-2107">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="482b4-2107">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-2108">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-2108">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-2109">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="482b4-2109">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2110">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2110">Az.Resources</span></span>
* <span data-ttu-id="482b4-2111">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="482b4-2111">Support for additional Template Export options</span></span>
    - <span data-ttu-id="482b4-2112">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="482b4-2112">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="482b4-2113">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="482b4-2113">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="482b4-2114">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2114">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-2115">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-2115">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-2116">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="482b4-2116">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2117">Az.Sql</span></span>
* <span data-ttu-id="482b4-2118">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="482b4-2118">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="482b4-2119">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="482b4-2119">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="482b4-2120">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="482b4-2120">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="482b4-2121">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="482b4-2121">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="482b4-2122">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="482b4-2122">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="482b4-2123">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="482b4-2123">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="482b4-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="482b4-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="482b4-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="482b4-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2126">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2126">Az.Storage</span></span>
* <span data-ttu-id="482b4-2127">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2127">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="482b4-2128">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2128">New-AzStorageAccount</span></span>
* <span data-ttu-id="482b4-2129">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2129">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="482b4-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2131">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2131">Az.Websites</span></span>
* <span data-ttu-id="482b4-2132">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="482b4-2132">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="482b4-2133">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="482b4-2133">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="482b4-2134">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2134">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="482b4-2135">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-2135">Az.Cdn</span></span>
* <span data-ttu-id="482b4-2136">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="482b4-2136">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2137">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2137">Az.Compute</span></span>
* <span data-ttu-id="482b4-2138">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="482b4-2138">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="482b4-2139">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-2139">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-2140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-2140">Az.EventHub</span></span>
* <span data-ttu-id="482b4-2141">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="482b4-2141">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="482b4-2142">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="482b4-2142">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2143">Az.Network</span></span>
* <span data-ttu-id="482b4-2144">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="482b4-2144">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="482b4-2145">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-2145">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-2146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-2146">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-2147">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="482b4-2147">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2148">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-2149">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="482b4-2149">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="482b4-2150">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="482b4-2150">Az.ServiceBus</span></span>
* <span data-ttu-id="482b4-2151">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="482b4-2151">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-2152">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-2152">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-2153">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="482b4-2153">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="482b4-2154">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="482b4-2154">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2155">Az.Sql</span></span>
* <span data-ttu-id="482b4-2156">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="482b4-2156">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="482b4-2157">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="482b4-2157">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="482b4-2158">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="482b4-2158">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="482b4-2159">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="482b4-2159">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2160">Az.Websites</span></span>
* <span data-ttu-id="482b4-2161">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="482b4-2161">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="482b4-2162">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2162">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="482b4-2163">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-2163">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-2164">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2164">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="482b4-2165">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2165">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="482b4-2166">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2166">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="482b4-2167">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="482b4-2167">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="482b4-2168">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="482b4-2168">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="482b4-2169">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="482b4-2169">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="482b4-2170">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2170">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="482b4-2171">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2171">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="482b4-2172">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="482b4-2172">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="482b4-2173">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="482b4-2173">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="482b4-2174">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2174">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="482b4-2175">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="482b4-2175">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="482b4-2176">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="482b4-2176">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="482b4-2177">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2177">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="482b4-2178">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2178">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="482b4-2179">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2179">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="482b4-2180">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2180">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="482b4-2181">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2181">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="482b4-2182">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="482b4-2182">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="482b4-2183">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="482b4-2183">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="482b4-2184">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-2184">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="482b4-2185">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="482b4-2185">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="482b4-2186">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="482b4-2186">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="482b4-2187">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="482b4-2187">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="482b4-2188">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="482b4-2188">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="482b4-2189">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="482b4-2189">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="482b4-2190">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="482b4-2190">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="482b4-2191">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="482b4-2191">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="482b4-2192">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="482b4-2192">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="482b4-2193">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-2193">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="482b4-2194">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="482b4-2194">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="482b4-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="482b4-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="482b4-2196">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2196">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="482b4-2197">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="482b4-2197">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="482b4-2198">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2198">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="482b4-2199">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="482b4-2199">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="482b4-2200">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2200">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="482b4-2201">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="482b4-2201">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="482b4-2202">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="482b4-2202">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="482b4-2203">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="482b4-2203">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="482b4-2204">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2204">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="482b4-2205">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-2205">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="482b4-2206">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="482b4-2206">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="482b4-2207">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2207">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="482b4-2208">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="482b4-2208">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="482b4-2209">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2209">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="482b4-2210">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-2210">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="482b4-2211">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2211">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="482b4-2212">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="482b4-2212">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="482b4-2213">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="482b4-2213">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="482b4-2214">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2214">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="482b4-2215">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="482b4-2215">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="482b4-2216">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="482b4-2216">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="482b4-2217">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="482b4-2217">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="482b4-2218">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="482b4-2218">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="482b4-2219">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-2219">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="482b4-2220">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="482b4-2220">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="482b4-2221">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2221">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="482b4-2222">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2222">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="482b4-2223">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2223">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="482b4-2224">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="482b4-2224">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="482b4-2225">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2225">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="482b4-2226">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2226">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="482b4-2227">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2227">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="482b4-2228">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-2228">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="482b4-2229">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="482b4-2229">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="482b4-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="482b4-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="482b4-2231">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="482b4-2231">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="482b4-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="482b4-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="482b4-2233">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-2233">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="482b4-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="482b4-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="482b4-2235">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="482b4-2235">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="482b4-2236">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="482b4-2236">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="482b4-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="482b4-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="482b4-2238">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="482b4-2238">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="482b4-2239">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-2239">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="482b4-2240">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="482b4-2240">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-2241">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-2241">Az.Automation</span></span>
* <span data-ttu-id="482b4-2242">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="482b4-2242">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="482b4-2243">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="482b4-2243">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="482b4-2244">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="482b4-2244">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="482b4-2245">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2245">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="482b4-2246">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="482b4-2246">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="482b4-2247">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="482b4-2247">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="482b4-2248">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="482b4-2248">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2249">Az.Compute</span></span>
* <span data-ttu-id="482b4-2250">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-2250">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="482b4-2251">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="482b4-2251">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2252">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-2253">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-2253">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-2254">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-2254">Az.Monitor</span></span>
* <span data-ttu-id="482b4-2255">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="482b4-2255">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2256">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2256">Az.Network</span></span>
* <span data-ttu-id="482b4-2257">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2257">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="482b4-2258">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="482b4-2258">Updated cmdlet:</span></span>
        - <span data-ttu-id="482b4-2259">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="482b4-2259">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="482b4-2260">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="482b4-2260">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2261">Az.Resources</span></span>
* <span data-ttu-id="482b4-2262">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2262">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2263">Az.Sql</span></span>
* <span data-ttu-id="482b4-2264">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="482b4-2264">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="482b4-2265">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2265">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-2266">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2266">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2267">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="482b4-2267">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-2268">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2268">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-2269">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="482b4-2269">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="482b4-2270">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="482b4-2270">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2271">Az.Compute</span></span>
* <span data-ttu-id="482b4-2272">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="482b4-2272">Proximity placement group feature.</span></span>
    - <span data-ttu-id="482b4-2273">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="482b4-2273">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="482b4-2274">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-2274">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="482b4-2275">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="482b4-2275">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="482b4-2276">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="482b4-2276">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="482b4-2277">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-2277">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="482b4-2278">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="482b4-2278">Breaking changes</span></span>
    - <span data-ttu-id="482b4-2279">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="482b4-2279">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="482b4-2280">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="482b4-2280">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="482b4-2281">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="482b4-2281">Az.DeploymentManager</span></span>
* <span data-ttu-id="482b4-2282">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="482b4-2282">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="482b4-2283">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="482b4-2283">Az.Dns</span></span>
* <span data-ttu-id="482b4-2284">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="482b4-2284">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="482b4-2285">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="482b4-2285">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="482b4-2286">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="482b4-2286">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="482b4-2287">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-2287">Az.FrontDoor</span></span>
* <span data-ttu-id="482b4-2288">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="482b4-2288">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="482b4-2289">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="482b4-2289">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="482b4-2290">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-2290">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-2291">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="482b4-2291">Removed two cmdlets:</span></span>
    - <span data-ttu-id="482b4-2292">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="482b4-2292">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="482b4-2293">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="482b4-2293">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="482b4-2294">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="482b4-2294">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="482b4-2295">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="482b4-2295">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="482b4-2296">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="482b4-2296">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="482b4-2297">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="482b4-2297">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-2298">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-2298">Az.Monitor</span></span>
* <span data-ttu-id="482b4-2299">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="482b4-2299">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="482b4-2300">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="482b4-2300">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="482b4-2301">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="482b4-2301">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="482b4-2302">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="482b4-2302">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="482b4-2303">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="482b4-2303">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="482b4-2304">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="482b4-2304">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="482b4-2305">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="482b4-2305">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="482b4-2306">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2306">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="482b4-2307">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2307">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="482b4-2308">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2308">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="482b4-2309">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2309">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="482b4-2310">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2310">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="482b4-2311">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="482b4-2311">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="482b4-2312">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="482b4-2312">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2313">Az.Network</span></span>
* <span data-ttu-id="482b4-2314">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="482b4-2314">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="482b4-2315">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-2315">New cmdlets</span></span>
        - <span data-ttu-id="482b4-2316">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-2316">New-AzNatGateway</span></span>
        - <span data-ttu-id="482b4-2317">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-2317">Get-AzNatGateway</span></span>
        - <span data-ttu-id="482b4-2318">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-2318">Set-AzNatGateway</span></span>
        - <span data-ttu-id="482b4-2319">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-2319">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="482b4-2320">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="482b4-2320">Updated cmdlets</span></span>
        - <span data-ttu-id="482b4-2321">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="482b4-2321">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="482b4-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="482b4-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="482b4-2323">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="482b4-2323">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="482b4-2324">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2324">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="482b4-2325">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2325">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-2326">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-2326">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-2327">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2327">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="482b4-2328">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="482b4-2328">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="482b4-2329">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="482b4-2329">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2330">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-2331">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="482b4-2331">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="482b4-2332">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="482b4-2332">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="482b4-2333">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="482b4-2333">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="482b4-2334">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="482b4-2334">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="482b4-2335">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="482b4-2335">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="482b4-2336">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="482b4-2336">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="482b4-2337">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="482b4-2337">Az.Relay</span></span>
* <span data-ttu-id="482b4-2338">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2338">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="482b4-2339">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="482b4-2339">Az.ServiceBus</span></span>
* <span data-ttu-id="482b4-2340">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="482b4-2340">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2341">Az.Storage</span></span>
* <span data-ttu-id="482b4-2342">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="482b4-2342">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="482b4-2343">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-2343">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="482b4-2344">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="482b4-2344">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="482b4-2345">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2345">New-AzStorageAccount</span></span>
* <span data-ttu-id="482b4-2346">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="482b4-2346">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="482b4-2347">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2347">New-AzStorageAccount</span></span>
    - <span data-ttu-id="482b4-2348">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2348">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="482b4-2349">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2349">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2350">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2350">Az.Websites</span></span>
* <span data-ttu-id="482b4-2351">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="482b4-2351">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="482b4-2352">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="482b4-2352">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="482b4-2353">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2353">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="482b4-2354">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-2354">Highlights since the last major release</span></span>
* <span data-ttu-id="482b4-2355">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2355">General availability of `Az` module</span></span>
* <span data-ttu-id="482b4-2356">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="482b4-2356">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="482b4-2357">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="482b4-2357">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="482b4-2358">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="482b4-2358">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="482b4-2359">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="482b4-2359">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="482b4-2360">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="482b4-2360">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="482b4-2361">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="482b4-2361">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-2362">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2362">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2363">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="482b4-2363">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="482b4-2364">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-2364">Az.Batch</span></span>
* <span data-ttu-id="482b4-2365">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="482b4-2366">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-2366">Az.Cdn</span></span>
* <span data-ttu-id="482b4-2367">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-2368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2368">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-2369">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2370">Az.Compute</span></span>
* <span data-ttu-id="482b4-2371">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="482b4-2371">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="482b4-2372">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="482b4-2373">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="482b4-2373">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-2374">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-2374">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-2375">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="482b4-2375">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2376">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-2377">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2377">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="482b4-2378">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="482b4-2378">Az.EventGrid</span></span>
* <span data-ttu-id="482b4-2379">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="482b4-2379">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-2380">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-2380">Az.EventHub</span></span>
* <span data-ttu-id="482b4-2381">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="482b4-2381">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="482b4-2382">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="482b4-2382">Az.HDInsight</span></span>
* <span data-ttu-id="482b4-2383">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-2384">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-2384">Az.IotHub</span></span>
* <span data-ttu-id="482b4-2385">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2385">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-2386">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-2386">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-2387">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="482b4-2388">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="482b4-2388">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="482b4-2389">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="482b4-2389">Az.MachineLearning</span></span>
* <span data-ttu-id="482b4-2390">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2390">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="482b4-2391">Az.Media</span><span class="sxs-lookup"><span data-stu-id="482b4-2391">Az.Media</span></span>
* <span data-ttu-id="482b4-2392">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-2393">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-2393">Az.Monitor</span></span>
  * <span data-ttu-id="482b4-2394">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="482b4-2394">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="482b4-2395">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="482b4-2395">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="482b4-2396">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="482b4-2396">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="482b4-2397">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="482b4-2397">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="482b4-2398">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="482b4-2398">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="482b4-2399">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="482b4-2399">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="482b4-2400">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2400">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2401">Az.Network</span></span>
* <span data-ttu-id="482b4-2402">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="482b4-2403">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="482b4-2403">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="482b4-2404">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="482b4-2404">Az.NotificationHubs</span></span>
* <span data-ttu-id="482b4-2405">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-2406">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-2406">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-2407">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="482b4-2408">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="482b4-2408">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="482b4-2409">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2409">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2410">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2410">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-2411">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2411">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="482b4-2412">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2412">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="482b4-2413">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2413">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="482b4-2414">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="482b4-2414">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="482b4-2415">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="482b4-2415">Az.RedisCache</span></span>
* <span data-ttu-id="482b4-2416">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2416">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2417">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2417">Az.Resources</span></span>
* <span data-ttu-id="482b4-2418">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="482b4-2418">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2419">Az.Sql</span></span>
* <span data-ttu-id="482b4-2420">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="482b4-2420">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="482b4-2421">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2421">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="482b4-2422">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2422">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="482b4-2423">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="482b4-2423">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="482b4-2424">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2424">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="482b4-2425">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="482b4-2425">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="482b4-2426">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="482b4-2426">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2427">Az.Websites</span></span>
* <span data-ttu-id="482b4-2428">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="482b4-2428">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="482b4-2429">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="482b4-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="482b4-2430">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2430">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="482b4-2431">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="482b4-2431">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="482b4-2432">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2432">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="482b4-2433">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-2433">Highlights since the last major release</span></span>
* <span data-ttu-id="482b4-2434">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2434">General availability of `Az` module</span></span>
* <span data-ttu-id="482b4-2435">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="482b4-2435">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="482b4-2436">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="482b4-2436">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="482b4-2437">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="482b4-2437">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="482b4-2438">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="482b4-2438">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="482b4-2439">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="482b4-2439">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="482b4-2440">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="482b4-2440">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="482b4-2441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2441">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2442">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2442">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="482b4-2443">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2443">Az.AnalysisServices</span></span>
* <span data-ttu-id="482b4-2444">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="482b4-2444">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="482b4-2445">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2445">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-2446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-2446">Az.Automation</span></span>
* <span data-ttu-id="482b4-2447">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="482b4-2447">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="482b4-2448">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="482b4-2448">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="482b4-2449">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2449">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2450">Az.Compute</span></span>
* <span data-ttu-id="482b4-2451">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2451">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="482b4-2452">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2452">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="482b4-2453">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="482b4-2453">Az.ContainerInstance</span></span>
* <span data-ttu-id="482b4-2454">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="482b4-2454">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-2455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-2455">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-2456">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="482b4-2456">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="482b4-2457">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2457">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2458">Az.Resources</span></span>
* <span data-ttu-id="482b4-2459">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="482b4-2459">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="482b4-2460">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-2460">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="482b4-2461">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="482b4-2461">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="482b4-2462">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="482b4-2462">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="482b4-2463">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="482b4-2463">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="482b4-2464">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="482b4-2464">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2465">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2465">Az.Sql</span></span>
* <span data-ttu-id="482b4-2466">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-2466">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2467">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2467">Az.Storage</span></span>
* <span data-ttu-id="482b4-2468">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2468">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="482b4-2469">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="482b4-2469">New-AzStorageContext</span></span>
* <span data-ttu-id="482b4-2470">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="482b4-2470">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="482b4-2471">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-2471">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="482b4-2472">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-2472">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="482b4-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="482b4-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="482b4-2475">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2475">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="482b4-2476">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="482b4-2476">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="482b4-2477">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="482b4-2477">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="482b4-2478">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="482b4-2478">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="482b4-2479">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="482b4-2479">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="482b4-2480">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2480">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="482b4-2481">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="482b4-2481">Highlights since the last major release</span></span>
* <span data-ttu-id="482b4-2482">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2482">General availability of `Az` module</span></span>
* <span data-ttu-id="482b4-2483">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="482b4-2483">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="482b4-2484">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="482b4-2484">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="482b4-2485">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="482b4-2485">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="482b4-2486">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="482b4-2486">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="482b4-2487">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="482b4-2487">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="482b4-2488">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="482b4-2488">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-2489">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-2489">Az.Automation</span></span>
* <span data-ttu-id="482b4-2490">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="482b4-2490">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="482b4-2491">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="482b4-2491">Dynamic grouping</span></span>
    * <span data-ttu-id="482b4-2492">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="482b4-2492">Pre-Post script</span></span>
    * <span data-ttu-id="482b4-2493">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2493">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2494">Az.Compute</span></span>
* <span data-ttu-id="482b4-2495">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="482b4-2495">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="482b4-2496">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2496">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-2497">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-2497">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-2498">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="482b4-2498">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2499">Az.Network</span></span>
* <span data-ttu-id="482b4-2500">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2500">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="482b4-2501">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2501">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2502">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-2503">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="482b4-2503">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="482b4-2504">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="482b4-2504">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2505">Az.Resources</span></span>
* <span data-ttu-id="482b4-2506">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-2506">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="482b4-2507">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="482b4-2507">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2508">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2508">Az.Sql</span></span>
* <span data-ttu-id="482b4-2509">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2509">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2510">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2510">Az.Storage</span></span>
* <span data-ttu-id="482b4-2511">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2511">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="482b4-2512">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-2512">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="482b4-2513">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-2513">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="482b4-2514">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="482b4-2514">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="482b4-2515">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="482b4-2515">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="482b4-2516">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="482b4-2516">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="482b4-2517">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2517">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2518">Az.Websites</span></span>
* <span data-ttu-id="482b4-2519">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="482b4-2519">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="482b4-2520">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2520">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-2521">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2521">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2522">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="482b4-2522">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="482b4-2523">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="482b4-2523">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-2524">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-2524">Az.Automation</span></span>
* <span data-ttu-id="482b4-2525">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2525">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="482b4-2526">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2526">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="482b4-2527">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="482b4-2527">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="482b4-2528">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-2528">Az.Cdn</span></span>
* <span data-ttu-id="482b4-2529">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="482b4-2529">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2530">Az.Compute</span></span>
* <span data-ttu-id="482b4-2531">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="482b4-2531">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-2532">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-2532">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-2533">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="482b4-2533">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="482b4-2534">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="482b4-2534">Az.LogicApp</span></span>
* <span data-ttu-id="482b4-2535">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="482b4-2535">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2536">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2536">Az.Network</span></span>
* <span data-ttu-id="482b4-2537">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="482b4-2537">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2538">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2538">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-2539">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2539">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="482b4-2540">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="482b4-2540">SDK Update</span></span>
* <span data-ttu-id="482b4-2541">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="482b4-2541">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="482b4-2542">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="482b4-2542">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2543">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2543">Az.Resources</span></span>
* <span data-ttu-id="482b4-2544">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="482b4-2544">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="482b4-2545">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="482b4-2545">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="482b4-2546">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2546">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="482b4-2547">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="482b4-2547">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="482b4-2548">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2548">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="482b4-2549">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="482b4-2549">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2550">Az.Sql</span></span>
* <span data-ttu-id="482b4-2551">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="482b4-2551">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="482b4-2552">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="482b4-2552">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2553">Az.Storage</span></span>
* <span data-ttu-id="482b4-2554">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="482b4-2554">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="482b4-2555">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2555">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="482b4-2556">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2556">Az.AnalysisServices</span></span>
* <span data-ttu-id="482b4-2557">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="482b4-2557">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-2558">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-2558">Az.Automation</span></span>
* <span data-ttu-id="482b4-2559">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2559">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="482b4-2560">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2560">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="482b4-2561">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2561">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-2562">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2562">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-2563">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="482b4-2563">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2564">Az.Compute</span></span>
* <span data-ttu-id="482b4-2565">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="482b4-2565">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="482b4-2566">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="482b4-2566">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="482b4-2567">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="482b4-2567">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="482b4-2568">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="482b4-2568">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2569">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2569">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-2570">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="482b4-2570">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="482b4-2571">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="482b4-2571">Az.EventHub</span></span>
* <span data-ttu-id="482b4-2572">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="482b4-2572">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-2573">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-2573">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-2574">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="482b4-2574">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="482b4-2575">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="482b4-2575">Az.LogicApp</span></span>
* <span data-ttu-id="482b4-2576">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="482b4-2576">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="482b4-2577">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2577">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="482b4-2578">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="482b4-2578">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="482b4-2579">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="482b4-2579">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="482b4-2580">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="482b4-2580">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="482b4-2581">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="482b4-2581">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="482b4-2582">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="482b4-2582">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="482b4-2583">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="482b4-2583">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="482b4-2584">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="482b4-2584">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="482b4-2585">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="482b4-2585">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="482b4-2586">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="482b4-2586">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="482b4-2587">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2587">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="482b4-2588">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2588">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="482b4-2589">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-2589">Az.Monitor</span></span>
* <span data-ttu-id="482b4-2590">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="482b4-2590">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2591">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2591">Az.Network</span></span>
* <span data-ttu-id="482b4-2592">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="482b4-2592">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-2593">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-2593">Az.OperationalInsights</span></span>
* <span data-ttu-id="482b4-2594">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="482b4-2594">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="482b4-2595">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="482b4-2595">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="482b4-2596">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="482b4-2596">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2597">Az.Resources</span></span>
* <span data-ttu-id="482b4-2598">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="482b4-2598">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="482b4-2599">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="482b4-2599">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="482b4-2600">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="482b4-2600">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="482b4-2601">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="482b4-2601">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2602">Az.Sql</span></span>
* <span data-ttu-id="482b4-2603">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="482b4-2603">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="482b4-2604">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="482b4-2604">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2605">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2605">Az.Websites</span></span>
* <span data-ttu-id="482b4-2606">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="482b4-2606">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="482b4-2607">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2607">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-2608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2608">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2609">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="482b4-2609">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="482b4-2610">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2610">Az.AnalysisServices</span></span>
<span data-ttu-id="482b4-2611">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="482b4-2611">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2612">Az.Compute</span></span>
* <span data-ttu-id="482b4-2613">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="482b4-2613">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="482b4-2614">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="482b4-2614">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="482b4-2615">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="482b4-2615">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2616">Az.RecoveryServices</span></span>
<span data-ttu-id="482b4-2617">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="482b4-2617">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2618">Az.Resources</span></span>
* <span data-ttu-id="482b4-2619">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2619">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="482b4-2620">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="482b4-2620">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="482b4-2621">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="482b4-2621">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="482b4-2622">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="482b4-2622">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2623">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2623">Az.Sql</span></span>
* <span data-ttu-id="482b4-2624">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="482b4-2624">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="482b4-2625">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2625">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="482b4-2626">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="482b4-2626">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="482b4-2627">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2627">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-2628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2628">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2629">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="482b4-2629">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="482b4-2630">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2630">Az.AnalysisServices</span></span>
* <span data-ttu-id="482b4-2631">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="482b4-2631">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2632">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2632">Az.RecoveryServices</span></span>
* <span data-ttu-id="482b4-2633">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="482b4-2633">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="482b4-2634">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2634">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-2635">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2635">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2636">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="482b4-2636">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="482b4-2637">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2637">Update incorrect online help URLs</span></span>
* <span data-ttu-id="482b4-2638">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="482b4-2638">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="482b4-2639">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="482b4-2639">Az.Aks</span></span>
* <span data-ttu-id="482b4-2640">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2640">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="482b4-2641">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-2641">Az.Automation</span></span>
* <span data-ttu-id="482b4-2642">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="482b4-2642">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="482b4-2643">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2643">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="482b4-2644">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="482b4-2644">Az.Cdn</span></span>
* <span data-ttu-id="482b4-2645">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2645">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2646">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2646">Az.Compute</span></span>
* <span data-ttu-id="482b4-2647">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="482b4-2647">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="482b4-2648">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-2648">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="482b4-2649">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="482b4-2649">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="482b4-2650">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="482b4-2650">Az.ContainerRegistry</span></span>
* <span data-ttu-id="482b4-2651">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2651">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="482b4-2652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="482b4-2652">Az.DataFactory</span></span>
* <span data-ttu-id="482b4-2653">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2653">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2654">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-2655">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="482b4-2655">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="482b4-2656">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="482b4-2656">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="482b4-2657">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2657">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-2658">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-2658">Az.IotHub</span></span>
* <span data-ttu-id="482b4-2659">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="482b4-2659">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="482b4-2660">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-2660">Az.KeyVault</span></span>
* <span data-ttu-id="482b4-2661">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2661">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2662">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2662">Az.Network</span></span>
* <span data-ttu-id="482b4-2663">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2663">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2664">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2664">Az.Resources</span></span>
* <span data-ttu-id="482b4-2665">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="482b4-2665">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="482b4-2666">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2666">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="482b4-2667">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="482b4-2667">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="482b4-2668">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="482b4-2668">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="482b4-2669">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="482b4-2669">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="482b4-2670">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-2670">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="482b4-2671">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="482b4-2671">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-2672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-2672">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-2673">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="482b4-2673">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="482b4-2674">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="482b4-2674">Fix some error messages.</span></span>
* <span data-ttu-id="482b4-2675">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="482b4-2675">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="482b4-2676">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="482b4-2676">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="482b4-2677">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="482b4-2677">Az.SignalR</span></span>
* <span data-ttu-id="482b4-2678">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2678">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2679">Az.Sql</span></span>
* <span data-ttu-id="482b4-2680">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2680">Update incorrect online help URLs</span></span>
* <span data-ttu-id="482b4-2681">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2681">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="482b4-2682">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="482b4-2682">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="482b4-2683">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="482b4-2683">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2684">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2684">Az.Storage</span></span>
* <span data-ttu-id="482b4-2685">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2685">Update incorrect online help URLs</span></span>
* <span data-ttu-id="482b4-2686">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="482b4-2686">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="482b4-2687">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-2687">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="482b4-2688">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="482b4-2688">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="482b4-2689">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="482b4-2689">Az.TrafficManager</span></span>
* <span data-ttu-id="482b4-2690">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2690">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2691">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2691">Az.Websites</span></span>
* <span data-ttu-id="482b4-2692">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2692">Update incorrect online help URLs</span></span>
* <span data-ttu-id="482b4-2693">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="482b4-2693">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="482b4-2694">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="482b4-2694">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="482b4-2695">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2695">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="482b4-2696">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2696">Az.Accounts</span></span>
* <span data-ttu-id="482b4-2697">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="482b4-2697">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2698">Az.Compute</span></span>
* <span data-ttu-id="482b4-2699">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="482b4-2699">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="482b4-2700">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="482b4-2700">Updated the description of ID in help files</span></span>
* <span data-ttu-id="482b4-2701">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="482b4-2701">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2702">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-2703">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="482b4-2703">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="482b4-2704">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2704">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="482b4-2705">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="482b4-2705">Az.EventGrid</span></span>
* <span data-ttu-id="482b4-2706">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-2706">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="482b4-2707">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="482b4-2707">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="482b4-2708">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="482b4-2708">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="482b4-2709">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="482b4-2709">Event Time-To-Live,</span></span>
        - <span data-ttu-id="482b4-2710">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="482b4-2710">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="482b4-2711">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2711">Dead letter endpoint.</span></span>
    - <span data-ttu-id="482b4-2712">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="482b4-2712">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="482b4-2713">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="482b4-2713">Event Time-To-Live,</span></span>
        - <span data-ttu-id="482b4-2714">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="482b4-2714">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="482b4-2715">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2715">Dead letter endpoint.</span></span>
* <span data-ttu-id="482b4-2716">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="482b4-2716">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="482b4-2717">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="482b4-2717">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="482b4-2718">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="482b4-2718">Az.IotHub</span></span>
* <span data-ttu-id="482b4-2719">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="482b4-2719">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="482b4-2720">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="482b4-2720">Az.LogicApp</span></span>
* <span data-ttu-id="482b4-2721">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="482b4-2721">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2722">Az.Resources</span></span>
* <span data-ttu-id="482b4-2723">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="482b4-2723">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="482b4-2724">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="482b4-2724">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="482b4-2725">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="482b4-2725">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="482b4-2726">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="482b4-2726">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="482b4-2727">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="482b4-2727">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="482b4-2728">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="482b4-2728">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="482b4-2729">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="482b4-2729">Az.SignalR</span></span>
* <span data-ttu-id="482b4-2730">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="482b4-2730">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-2731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2731">Az.Sql</span></span>
* <span data-ttu-id="482b4-2732">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="482b4-2732">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="482b4-2733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2733">Az.Storage</span></span>
* <span data-ttu-id="482b4-2734">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="482b4-2734">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="482b4-2735">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="482b4-2735">New-AzStorageContext</span></span>
* <span data-ttu-id="482b4-2736">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="482b4-2736">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="482b4-2737">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="482b4-2737">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2738">Az.Websites</span></span>
* <span data-ttu-id="482b4-2739">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="482b4-2739">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="482b4-2740">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="482b4-2740">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="482b4-2741">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2741">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="482b4-2742">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-2742">General</span></span>

- <span data-ttu-id="482b4-2743">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="482b4-2743">General Availability of Az Module</span></span>
- <span data-ttu-id="482b4-2744">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="482b4-2744">Online help for each module</span></span>
- <span data-ttu-id="482b4-2745">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="482b4-2745">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="482b4-2746">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2746">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="482b4-2747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="482b4-2747">Az.Accounts</span></span>
- <span data-ttu-id="482b4-2748">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="482b4-2748">Changed from Az.Profile</span></span>
- <span data-ttu-id="482b4-2749">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="482b4-2749">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="482b4-2750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-2750">Az.ApiManagement</span></span>
- <span data-ttu-id="482b4-2751">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="482b4-2751">Fixes for #7002</span></span>
- <span data-ttu-id="482b4-2752">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2752">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="482b4-2753">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="482b4-2753">Az.Batch</span></span>
- <span data-ttu-id="482b4-2754">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2754">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="482b4-2755">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2755">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="482b4-2756">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2756">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="482b4-2757">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="482b4-2757">Az.Billing</span></span>
- <span data-ttu-id="482b4-2758">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="482b4-2758">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="482b4-2759">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2759">Az.CognitivServices</span></span>
- <span data-ttu-id="482b4-2760">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="482b4-2760">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="482b4-2761">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="482b4-2761">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="482b4-2762">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="482b4-2762">Az.ContainerInstance</span></span>
- <span data-ttu-id="482b4-2763">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="482b4-2763">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="482b4-2764">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="482b4-2764">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="482b4-2765">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2766">Az.DataLakeStore</span></span>
- <span data-ttu-id="482b4-2767">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="482b4-2768">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="482b4-2768">Az.Monitor</span></span>
- <span data-ttu-id="482b4-2769">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2769">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="482b4-2770">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="482b4-2770">Az.KeyVault</span></span>
- <span data-ttu-id="482b4-2771">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="482b4-2771">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="482b4-2772">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="482b4-2772">Az.MachineLearning</span></span>
- <span data-ttu-id="482b4-2773">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="482b4-2773">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="482b4-2774">Az.Media</span><span class="sxs-lookup"><span data-stu-id="482b4-2774">Az.Media</span></span>
- <span data-ttu-id="482b4-2775">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="482b4-2775">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="482b4-2776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2776">Az.Network</span></span>
<span data-ttu-id="482b4-2777">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="482b4-2777">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="482b4-2778">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-2778">New cmdlets added:</span></span>
        - <span data-ttu-id="482b4-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="482b4-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="482b4-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="482b4-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="482b4-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="482b4-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="482b4-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="482b4-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="482b4-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="482b4-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="482b4-2784">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2784">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="482b4-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="482b4-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="482b4-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="482b4-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="482b4-2787">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="482b4-2787">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="482b4-2788">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="482b4-2788">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="482b4-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="482b4-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="482b4-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="482b4-2791">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-2791">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="482b4-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="482b4-2793">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2793">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="482b4-2794">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="482b4-2794">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="482b4-2795">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="482b4-2795">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="482b4-2796">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="482b4-2796">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="482b4-2797">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="482b4-2797">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="482b4-2798">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="482b4-2798">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="482b4-2799">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2799">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="482b4-2800">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-2800">Az.OperationalInsights</span></span>
- <span data-ttu-id="482b4-2801">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2801">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="482b4-2802">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="482b4-2802">Az.Profile</span></span>
- <span data-ttu-id="482b4-2803">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="482b4-2803">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2804">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2804">Az.RecoveryServices</span></span>
- <span data-ttu-id="482b4-2805">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2805">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="482b4-2806">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2806">Az.Resources</span></span>
- <span data-ttu-id="482b4-2807">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2807">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="482b4-2808">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-2808">Az.ServiceFabric</span></span>
- <span data-ttu-id="482b4-2809">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="482b4-2809">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="482b4-2810">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2810">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="482b4-2811">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="482b4-2811">Az.SIgnalR</span></span>
- <span data-ttu-id="482b4-2812">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="482b4-2812">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="482b4-2813">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2813">Az.Sql</span></span>
- <span data-ttu-id="482b4-2814">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="482b4-2814">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="482b4-2815">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2815">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="482b4-2816">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="482b4-2817">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2817">Az.Storage</span></span>
- <span data-ttu-id="482b4-2818">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2818">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="482b4-2819">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2819">Az.Websites</span></span>
- <span data-ttu-id="482b4-2820">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="482b4-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="482b4-2821">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2821">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="482b4-2822">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-2822">General</span></span>

* <span data-ttu-id="482b4-2823">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="482b4-2823">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="482b4-2824">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2824">Az.Compute</span></span>

* <span data-ttu-id="482b4-2825">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2825">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2826">Az.DataLakeStore</span></span>

* <span data-ttu-id="482b4-2827">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="482b4-2827">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="482b4-2828">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="482b4-2828">Az.FrontDoor</span></span>

* <span data-ttu-id="482b4-2829">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="482b4-2829">Fixed some broken links</span></span>
    - <span data-ttu-id="482b4-2830">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-2830">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="482b4-2831">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="482b4-2831">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="482b4-2832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2832">Az.RecoveryServices</span></span>

* <span data-ttu-id="482b4-2833">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2833">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="482b4-2834">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="482b4-2834">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="482b4-2835">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2835">Az.Resources</span></span>

* <span data-ttu-id="482b4-2836">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="482b4-2836">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="482b4-2837">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2837">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="482b4-2838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2838">Az.Sql</span></span>

* <span data-ttu-id="482b4-2839">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="482b4-2839">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="482b4-2840">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="482b4-2840">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="482b4-2841">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="482b4-2841">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="482b4-2842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="482b4-2842">Az.Storage</span></span>

* <span data-ttu-id="482b4-2843">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2843">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="482b4-2844">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="482b4-2844">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="482b4-2845">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-2845">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="482b4-2846">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="482b4-2846">Support Static Website configuration</span></span>
    - <span data-ttu-id="482b4-2847">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="482b4-2847">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="482b4-2848">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="482b4-2848">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="482b4-2849">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-2849">Az.Websites</span></span>

* <span data-ttu-id="482b4-2850">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="482b4-2850">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="482b4-2851">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="482b4-2851">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="482b4-2852">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2852">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="482b4-2853">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2853">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="482b4-2854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="482b4-2854">Az.ApiManagement</span></span>
* <span data-ttu-id="482b4-2855">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2855">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="482b4-2856">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="482b4-2856">Az.Automation</span></span>
* <span data-ttu-id="482b4-2857">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="482b4-2857">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="482b4-2858">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="482b4-2858">Added Update Management cmdlets</span></span>
* <span data-ttu-id="482b4-2859">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="482b4-2859">Added Source Control cmdlets</span></span>
* <span data-ttu-id="482b4-2860">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="482b4-2860">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="482b4-2861">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="482b4-2861">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="482b4-2862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2862">Az.Compute</span></span>
* <span data-ttu-id="482b4-2863">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="482b4-2863">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="482b4-2864">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2864">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="482b4-2865">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="482b4-2865">Az.ContainerInstance</span></span>
* <span data-ttu-id="482b4-2866">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2866">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="482b4-2867">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="482b4-2867">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="482b4-2868">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="482b4-2868">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="482b4-2869">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2869">Az.Network</span></span>
* <span data-ttu-id="482b4-2870">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="482b4-2870">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="482b4-2871">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2871">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="482b4-2872">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="482b4-2872">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="482b4-2873">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="482b4-2873">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="482b4-2874">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="482b4-2874">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="482b4-2875">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="482b4-2875">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="482b4-2876">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="482b4-2876">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="482b4-2877">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="482b4-2877">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="482b4-2878">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="482b4-2878">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="482b4-2879">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2879">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="482b4-2880">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="482b4-2880">Az.Relay</span></span>
* <span data-ttu-id="482b4-2881">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="482b4-2881">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="482b4-2882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2882">Az.Resources</span></span>
* <span data-ttu-id="482b4-2883">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="482b4-2883">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="482b4-2884">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="482b4-2884">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="482b4-2885">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="482b4-2885">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="482b4-2886">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-2886">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-2887">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="482b4-2887">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="482b4-2888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-2888">Az.Sql</span></span>
* <span data-ttu-id="482b4-2889">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2889">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="482b4-2890">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="482b4-2890">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="482b4-2891">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="482b4-2891">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="482b4-2892">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="482b4-2892">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="482b4-2893">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="482b4-2893">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="482b4-2894">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="482b4-2894">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="482b4-2895">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="482b4-2895">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="482b4-2896">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="482b4-2896">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="482b4-2897">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="482b4-2897">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="482b4-2898">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="482b4-2898">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="482b4-2899">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="482b4-2899">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="482b4-2900">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2900">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="482b4-2901">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="482b4-2901">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="482b4-2902">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="482b4-2902">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="482b4-2903">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="482b4-2903">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="482b4-2904">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="482b4-2904">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="482b4-2905">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="482b4-2905">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="482b4-2906">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2906">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="482b4-2907">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="482b4-2907">General</span></span>
* <span data-ttu-id="482b4-2908">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="482b4-2908">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="482b4-2909">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="482b4-2909">Az.Profile</span></span>
* <span data-ttu-id="482b4-2910">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="482b4-2910">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="482b4-2911">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="482b4-2911">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="482b4-2912">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="482b4-2912">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="482b4-2913">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="482b4-2913">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="482b4-2914">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="482b4-2914">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="482b4-2915">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="482b4-2915">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="482b4-2916">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="482b4-2916">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-2917">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2917">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-2918">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="482b4-2918">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2919">Az.Compute</span></span>
* <span data-ttu-id="482b4-2920">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="482b4-2920">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="482b4-2921">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="482b4-2921">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="482b4-2922">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="482b4-2922">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-2924">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="482b4-2924">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="482b4-2925">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="482b4-2925">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="482b4-2926">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="482b4-2926">Az.Insights</span></span>
* <span data-ttu-id="482b4-2927">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="482b4-2927">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="482b4-2928">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="482b4-2928">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="482b4-2929">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="482b4-2929">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="482b4-2930">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="482b4-2930">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2931">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2931">Az.Network</span></span>
* <span data-ttu-id="482b4-2932">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="482b4-2932">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="482b4-2933">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-2933">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="482b4-2934">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="482b4-2934">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="482b4-2935">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="482b4-2935">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="482b4-2936">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="482b4-2936">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="482b4-2937">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="482b4-2937">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="482b4-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="482b4-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="482b4-2939">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="482b4-2939">Az.PolicyInsights</span></span>
* <span data-ttu-id="482b4-2940">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="482b4-2940">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2941">Az.Resources</span></span>
* <span data-ttu-id="482b4-2942">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="482b4-2942">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="482b4-2943">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="482b4-2943">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="482b4-2944">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="482b4-2944">Az.ServiceBus</span></span>
* <span data-ttu-id="482b4-2945">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="482b4-2945">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="482b4-2946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="482b4-2946">Az.ServiceFabric</span></span>
* <span data-ttu-id="482b4-2947">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="482b4-2947">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="482b4-2948">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="482b4-2948">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="482b4-2949">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="482b4-2949">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="482b4-2950">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="482b4-2950">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="482b4-2951">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="482b4-2951">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="482b4-2952">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2952">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="482b4-2953">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="482b4-2953">Az.Profile</span></span>
* <span data-ttu-id="482b4-2954">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="482b4-2954">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="482b4-2955">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="482b4-2955">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2956">Az.Compute</span></span>
* <span data-ttu-id="482b4-2957">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="482b4-2957">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="482b4-2958">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="482b4-2958">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="482b4-2959">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="482b4-2959">Az.DataLakeStore</span></span>
* <span data-ttu-id="482b4-2960">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="482b4-2960">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="482b4-2961">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="482b4-2961">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="482b4-2962">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="482b4-2962">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="482b4-2963">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="482b4-2963">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="482b4-2964">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="482b4-2964">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2965">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2965">Az.Network</span></span>
* <span data-ttu-id="482b4-2966">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="482b4-2966">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="482b4-2967">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="482b4-2967">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-2968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-2968">Az.Resources</span></span>
* <span data-ttu-id="482b4-2969">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="482b4-2969">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="482b4-2970">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="482b4-2970">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="482b4-2971">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-2971">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="482b4-2972">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="482b4-2972">Azure.Storage</span></span>
* <span data-ttu-id="482b4-2973">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="482b4-2973">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="482b4-2974">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-2974">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="482b4-2975">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="482b4-2975">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="482b4-2976">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="482b4-2976">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="482b4-2977">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="482b4-2977">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="482b4-2978">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="482b4-2978">Az.CognitiveServices</span></span>
* <span data-ttu-id="482b4-2979">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="482b4-2979">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="482b4-2980">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="482b4-2980">Az.Compute</span></span>
* <span data-ttu-id="482b4-2981">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="482b4-2981">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="482b4-2982">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="482b4-2982">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="482b4-2983">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-2983">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="482b4-2984">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="482b4-2984">Az.DataFactoryV2</span></span>
* <span data-ttu-id="482b4-2985">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="482b4-2985">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="482b4-2986">Az.Network</span><span class="sxs-lookup"><span data-stu-id="482b4-2986">Az.Network</span></span>
* <span data-ttu-id="482b4-2987">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="482b4-2987">Added NetworkProfile functionality.</span></span> <span data-ttu-id="482b4-2988">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="482b4-2988">new cmdlets added</span></span>
    - <span data-ttu-id="482b4-2989">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="482b4-2989">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="482b4-2990">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="482b4-2990">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="482b4-2991">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="482b4-2991">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="482b4-2992">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="482b4-2992">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="482b4-2993">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-2993">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="482b4-2994">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-2994">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="482b4-2995">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="482b4-2995">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="482b4-2996">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="482b4-2996">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="482b4-2997">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="482b4-2997">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="482b4-2998">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="482b4-2998">Az.RedisCache</span></span>
* <span data-ttu-id="482b4-2999">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="482b4-2999">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="482b4-3000">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="482b4-3000">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="482b4-3001">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="482b4-3001">Az.Resources</span></span>
* <span data-ttu-id="482b4-3002">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="482b4-3002">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="482b4-3003">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="482b4-3003">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="482b4-3004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="482b4-3004">Az.Sql</span></span>
* <span data-ttu-id="482b4-3005">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="482b4-3005">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="482b4-3006">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="482b4-3006">Az.Websites</span></span>
* <span data-ttu-id="482b4-3007">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="482b4-3007">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="482b4-3008">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="482b4-3008">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="482b4-3009">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="482b4-3009">0.2.0 - September 2018</span></span>
 <span data-ttu-id="482b4-3010">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="482b4-3010">Initial Release</span></span>
