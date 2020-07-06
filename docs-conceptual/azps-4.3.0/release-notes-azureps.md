---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9ec7589ab155553da29612096a607d82a078321
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268367"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="85010-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="85010-103">Azure PowerShell release notes</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="85010-104">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="85010-104">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-105">Az.Accounts</span></span>
* <span data-ttu-id="85010-106">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="85010-106">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="85010-107">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="85010-107">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="85010-108">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="85010-108">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="85010-109">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="85010-109">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="85010-110">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="85010-110">Az.Aks</span></span>
* <span data-ttu-id="85010-111">Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="85010-111">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="85010-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-112">Az.Batch</span></span>
* <span data-ttu-id="85010-113">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="85010-113">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="85010-114">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="85010-114">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-115">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-115">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-116">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="85010-116">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="85010-117">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="85010-117">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-118">Az.Compute</span></span>
* <span data-ttu-id="85010-119">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="85010-119">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="85010-120">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="85010-120">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="85010-121">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="85010-121">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="85010-122">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-122">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="85010-123">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="85010-123">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-124">Az.DataFactory</span></span>
* <span data-ttu-id="85010-125">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="85010-125">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-126">Az.EventHub</span></span>
* <span data-ttu-id="85010-127">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="85010-127">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="85010-128">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="85010-128">Az.Functions</span></span>
* <span data-ttu-id="85010-129">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="85010-129">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-130">Az.HDInsight</span></span>
* <span data-ttu-id="85010-131">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="85010-131">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="85010-132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="85010-132">Az.HealthcareApis</span></span>
* <span data-ttu-id="85010-133">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="85010-133">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="85010-134">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="85010-134">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-135">Az.Monitor</span></span>
* <span data-ttu-id="85010-136">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="85010-136">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="85010-137">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="85010-137">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-138">Az.Network</span></span>
* <span data-ttu-id="85010-139">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-139">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="85010-140">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-140">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="85010-141">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="85010-141">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="85010-142">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="85010-142">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="85010-143">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="85010-143">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="85010-144">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="85010-144">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="85010-145">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85010-145">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="85010-146">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85010-146">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="85010-147">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85010-147">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="85010-148">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85010-148">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="85010-149">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-149">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="85010-150">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-150">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="85010-151">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="85010-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="85010-152">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-152">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="85010-153">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="85010-153">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="85010-154">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="85010-154">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="85010-155">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="85010-155">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="85010-156">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="85010-156">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="85010-157">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="85010-157">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="85010-158">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="85010-158">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="85010-159">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="85010-159">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="85010-160">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="85010-160">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="85010-161">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="85010-161">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="85010-162">[КРИТИЧЕСКОЕ ИЗМЕНЕНИЕ] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="85010-162">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="85010-163">[КРИТИЧЕСКОЕ ИЗМЕНЕНИЕ] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="85010-163">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="85010-164">[КРИТИЧЕСКОЕ ИЗМЕНЕНИЕ] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="85010-164">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="85010-165">[КРИТИЧЕСКОЕ ИЗМЕНЕНИЕ] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="85010-165">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="85010-166">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="85010-166">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="85010-167">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="85010-168">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="85010-169">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="85010-170">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="85010-171">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="85010-172">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="85010-173">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="85010-173">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="85010-174">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="85010-174">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="85010-175">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-175">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="85010-176">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-176">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="85010-177">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-177">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="85010-178">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-178">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="85010-179">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-179">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="85010-180">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="85010-180">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="85010-181">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="85010-181">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="85010-182">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="85010-182">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="85010-183">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="85010-183">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="85010-184">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="85010-184">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="85010-185">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="85010-185">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="85010-186">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="85010-186">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="85010-187">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="85010-187">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-188">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-188">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-189">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="85010-189">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="85010-190">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="85010-190">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="85010-191">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="85010-191">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="85010-192">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="85010-192">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="85010-193">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="85010-193">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-194">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-194">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-195">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="85010-195">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="85010-196">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="85010-196">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-197">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-197">Az.Resources</span></span>
* <span data-ttu-id="85010-198">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="85010-198">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="85010-199">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="85010-199">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="85010-200">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="85010-200">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="85010-201">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-201">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="85010-202">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="85010-202">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="85010-203">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="85010-203">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-204">Az.Sql</span></span>
* <span data-ttu-id="85010-205">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85010-205">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="85010-206">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="85010-206">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="85010-207">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="85010-207">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-208">Az.Storage</span></span>
* <span data-ttu-id="85010-209">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="85010-209">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="85010-210">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-210">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="85010-211">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="85010-211">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-212">Az.Websites</span></span>
* <span data-ttu-id="85010-213">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="85010-213">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="85010-214">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="85010-214">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="85010-215">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="85010-215">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="85010-216">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="85010-216">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="85010-217">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="85010-217">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="85010-218">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85010-218">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="85010-219">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-219">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-220">Az.Accounts</span></span>
* <span data-ttu-id="85010-221">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="85010-221">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="85010-222">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="85010-222">Az.AnalysisServices</span></span>
* <span data-ttu-id="85010-223">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="85010-223">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-224">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-224">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-225">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="85010-225">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="85010-226">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="85010-226">Az.Billing</span></span>
* <span data-ttu-id="85010-227">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="85010-227">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-228">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-229">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="85010-229">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="85010-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-230">Az.DataFactory</span></span>
* <span data-ttu-id="85010-231">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="85010-231">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="85010-232">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="85010-232">Az.DataShare</span></span>
* <span data-ttu-id="85010-233">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="85010-233">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="85010-234">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="85010-234">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="85010-235">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="85010-235">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-236">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-236">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-237">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="85010-237">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="85010-238">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-238">Added optional parameters to</span></span> 
    - <span data-ttu-id="85010-239">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="85010-239">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="85010-240">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="85010-240">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-241">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-241">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-242">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="85010-242">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="85010-243">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="85010-243">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="85010-244">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="85010-244">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="85010-245">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="85010-245">Az.PrivateDns</span></span>
* <span data-ttu-id="85010-246">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="85010-246">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-248">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="85010-248">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="85010-249">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="85010-249">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-250">Az.Resources</span></span>
* <span data-ttu-id="85010-251">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="85010-251">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="85010-252">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="85010-252">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="85010-253">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="85010-253">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="85010-254">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="85010-254">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="85010-255">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="85010-255">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-256">Az.Sql</span></span>
* <span data-ttu-id="85010-257">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="85010-257">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="85010-258">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="85010-258">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="85010-259">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-259">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-260">Az.Storage</span></span>
* <span data-ttu-id="85010-261">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="85010-261">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="85010-262">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-262">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="85010-263">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-263">Highlights since the last release</span></span>
* <span data-ttu-id="85010-264">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="85010-264">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="85010-265">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="85010-265">General availability of Az.Functions</span></span> 
* <span data-ttu-id="85010-266">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="85010-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-267">Az.Accounts</span></span>
* <span data-ttu-id="85010-268">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="85010-268">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="85010-269">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="85010-269">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="85010-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="85010-270">Az.Aks</span></span>
* <span data-ttu-id="85010-271">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="85010-271">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="85010-272">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="85010-272">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="85010-273">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="85010-273">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-274">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-275">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="85010-275">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="85010-276">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="85010-276">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="85010-277">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="85010-277">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="85010-278">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="85010-278">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="85010-279">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="85010-279">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="85010-280">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="85010-280">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="85010-281">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="85010-281">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="85010-282">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="85010-282">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="85010-283">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="85010-283">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="85010-284">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="85010-284">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="85010-285">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="85010-285">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="85010-286">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="85010-286">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="85010-287">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="85010-287">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="85010-288">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="85010-288">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="85010-289">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="85010-289">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="85010-290">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="85010-290">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="85010-291">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="85010-291">Az.ApplicationInsights</span></span>
* <span data-ttu-id="85010-292">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="85010-292">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="85010-293">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="85010-293">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="85010-294">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-294">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="85010-295">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-295">Az.Batch</span></span>
* <span data-ttu-id="85010-296">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="85010-296">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="85010-297">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="85010-297">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="85010-298">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="85010-298">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="85010-299">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="85010-299">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="85010-300">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="85010-300">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="85010-301">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="85010-301">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="85010-302">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-302">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="85010-303">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-303">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="85010-304">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="85010-304">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-305">Az.Compute</span></span>
* <span data-ttu-id="85010-306">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="85010-306">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="85010-307">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="85010-307">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="85010-308">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="85010-308">Breaking changes</span></span>
    - <span data-ttu-id="85010-309">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="85010-309">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="85010-310">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-310">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="85010-311">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="85010-311">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="85010-312">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-312">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="85010-313">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-313">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="85010-314">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="85010-314">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="85010-315">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-315">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="85010-316">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-316">Az.DataFactory</span></span>
* <span data-ttu-id="85010-317">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="85010-317">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="85010-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-318">Az.FrontDoor</span></span>
* <span data-ttu-id="85010-319">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="85010-319">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="85010-320">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="85010-320">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="85010-321">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="85010-321">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="85010-322">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="85010-322">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="85010-323">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="85010-323">Az.Functions</span></span>
* <span data-ttu-id="85010-324">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="85010-324">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-325">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-325">Az.HDInsight</span></span>
* <span data-ttu-id="85010-326">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="85010-326">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="85010-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="85010-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="85010-328">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85010-328">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-329">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-329">Az.IotHub</span></span>
* <span data-ttu-id="85010-330">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="85010-330">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="85010-331">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="85010-331">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="85010-332">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="85010-332">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="85010-333">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="85010-333">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="85010-334">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="85010-334">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="85010-335">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-335">New cmdlets are:</span></span>
    - <span data-ttu-id="85010-336">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="85010-336">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="85010-337">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="85010-337">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="85010-338">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="85010-338">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="85010-339">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-339">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="85010-340">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-340">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="85010-341">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="85010-341">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-342">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-342">Az.KeyVault</span></span>
* <span data-ttu-id="85010-343">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="85010-343">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="85010-344">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85010-344">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="85010-345">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="85010-345">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="85010-346">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="85010-346">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="85010-347">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="85010-347">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="85010-348">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="85010-348">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="85010-349">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="85010-349">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-350">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-350">Az.Monitor</span></span>
* <span data-ttu-id="85010-351">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="85010-351">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="85010-352">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="85010-352">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="85010-353">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="85010-353">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="85010-354">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="85010-354">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="85010-355">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="85010-355">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="85010-356">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="85010-356">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="85010-357">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="85010-357">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-358">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-358">Az.Network</span></span>
* <span data-ttu-id="85010-359">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="85010-359">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="85010-360">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="85010-360">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="85010-361">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="85010-361">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="85010-362">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-362">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="85010-363">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="85010-363">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="85010-364">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-364">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-365">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="85010-365">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="85010-366">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="85010-366">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="85010-367">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="85010-367">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="85010-368">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="85010-368">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="85010-369">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="85010-369">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="85010-370">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="85010-370">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="85010-371">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="85010-371">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="85010-372">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="85010-372">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="85010-373">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="85010-373">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="85010-374">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="85010-374">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="85010-375">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="85010-375">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="85010-376">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="85010-376">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="85010-377">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="85010-377">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="85010-378">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="85010-378">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="85010-379">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-379">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="85010-380">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="85010-380">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="85010-381">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="85010-381">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="85010-382">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="85010-382">Updated cmdlet:</span></span>
        - <span data-ttu-id="85010-383">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="85010-383">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-384">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-384">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-385">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="85010-385">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="85010-386">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-386">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="85010-387">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="85010-387">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="85010-388">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="85010-388">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="85010-389">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="85010-389">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="85010-390">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="85010-390">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="85010-391">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-391">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="85010-392">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="85010-392">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-393">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-393">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-394">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="85010-394">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="85010-395">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="85010-395">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="85010-396">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-396">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="85010-397">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="85010-397">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="85010-398">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="85010-398">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-399">Az.Resources</span></span>
* <span data-ttu-id="85010-400">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="85010-400">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="85010-401">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="85010-401">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="85010-402">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="85010-402">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="85010-403">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="85010-403">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="85010-404">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="85010-404">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="85010-405">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="85010-405">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="85010-406">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="85010-406">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="85010-407">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="85010-407">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="85010-408">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="85010-408">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="85010-409">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="85010-409">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="85010-410">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="85010-410">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="85010-411">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="85010-411">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="85010-412">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="85010-412">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="85010-413">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="85010-413">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="85010-414">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="85010-414">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="85010-415">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="85010-415">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="85010-416">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="85010-416">'New-AzDeployment'</span></span>
    - <span data-ttu-id="85010-417">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="85010-417">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="85010-418">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="85010-418">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="85010-419">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-419">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-421">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="85010-421">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-422">Az.Sql</span></span>
* <span data-ttu-id="85010-423">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="85010-423">Enhance performance of:</span></span>
    - <span data-ttu-id="85010-424">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="85010-424">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="85010-425">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="85010-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="85010-426">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="85010-426">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="85010-427">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="85010-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="85010-428">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="85010-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="85010-429">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="85010-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="85010-430">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="85010-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="85010-431">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="85010-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="85010-432">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-432">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="85010-433">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="85010-433">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-434">Az.Storage</span></span>
* <span data-ttu-id="85010-435">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="85010-435">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="85010-436">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="85010-436">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="85010-437">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-437">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="85010-438">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="85010-438">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="85010-439">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="85010-439">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="85010-440">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="85010-440">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="85010-441">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="85010-441">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="85010-442">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="85010-442">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="85010-443">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="85010-443">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="85010-444">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="85010-444">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="85010-445">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="85010-445">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="85010-446">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="85010-446">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="85010-447">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="85010-447">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="85010-448">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-448">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="85010-449">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-449">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="85010-450">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-450">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="85010-451">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-451">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="85010-452">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="85010-452">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="85010-453">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="85010-453">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="85010-454">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-454">Supported failover Storage account</span></span>
    - <span data-ttu-id="85010-455">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="85010-455">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="85010-456">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="85010-456">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="85010-457">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="85010-457">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="85010-458">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="85010-458">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="85010-459">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85010-459">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="85010-460">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="85010-460">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="85010-461">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="85010-461">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="85010-462">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="85010-462">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="85010-463">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="85010-463">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="85010-464">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="85010-464">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="85010-465">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85010-465">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="85010-466">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="85010-466">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="85010-467">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="85010-467">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="85010-468">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85010-468">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="85010-469">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="85010-469">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="85010-470">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="85010-470">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="85010-471">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="85010-471">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="85010-472">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85010-472">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="85010-473">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="85010-473">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="85010-474">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="85010-474">Az.TrafficManager</span></span>
* <span data-ttu-id="85010-475">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="85010-475">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-476">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-476">Az.Websites</span></span>
* <span data-ttu-id="85010-477">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-477">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="85010-478">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-478">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="85010-479">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-479">Highlights since the last release</span></span>
* <span data-ttu-id="85010-480">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="85010-480">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-481">Az.Accounts</span></span>
* <span data-ttu-id="85010-482">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="85010-482">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-483">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-483">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-484">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="85010-484">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="85010-485">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="85010-485">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="85010-486">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-486">Az.Cdn</span></span>
* <span data-ttu-id="85010-487">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="85010-487">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-488">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-489">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="85010-489">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-490">Az.Compute</span></span>
* <span data-ttu-id="85010-491">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="85010-491">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="85010-492">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="85010-492">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-493">Az.IotHub</span></span>
* <span data-ttu-id="85010-494">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-494">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="85010-495">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="85010-495">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="85010-496">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="85010-496">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="85010-497">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-497">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="85010-498">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-498">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="85010-499">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="85010-499">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="85010-500">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="85010-500">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="85010-501">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="85010-501">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="85010-502">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-502">New cmdlets are:</span></span>
    - <span data-ttu-id="85010-503">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-503">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="85010-504">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-504">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="85010-505">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-505">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="85010-506">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-506">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="85010-507">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-507">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-508">Az.KeyVault</span></span>
* <span data-ttu-id="85010-509">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="85010-509">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="85010-510">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="85010-510">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="85010-511">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="85010-511">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="85010-512">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="85010-512">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="85010-513">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="85010-513">Az.Maintenance</span></span>
* <span data-ttu-id="85010-514">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="85010-514">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-515">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-515">Az.Monitor</span></span>
* <span data-ttu-id="85010-516">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="85010-516">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="85010-517">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="85010-517">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="85010-518">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="85010-518">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="85010-519">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="85010-519">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="85010-520">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="85010-520">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="85010-521">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="85010-521">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="85010-522">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="85010-522">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="85010-523">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="85010-523">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-524">Az.Network</span></span>
* <span data-ttu-id="85010-525">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="85010-525">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="85010-526">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85010-526">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="85010-527">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85010-527">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="85010-528">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="85010-528">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="85010-529">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="85010-529">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="85010-530">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="85010-530">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="85010-531">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85010-531">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="85010-532">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="85010-532">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="85010-533">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="85010-533">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="85010-534">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-534">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="85010-535">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="85010-535">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="85010-536">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-536">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="85010-537">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="85010-537">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="85010-538">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="85010-538">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="85010-539">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="85010-539">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="85010-540">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-540">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-541">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-541">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-542">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="85010-542">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="85010-543">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="85010-543">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-544">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-545">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="85010-545">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-546">Az.Sql</span></span>
* <span data-ttu-id="85010-547">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="85010-547">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="85010-548">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-548">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-549">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-549">Az.Storage</span></span>
* <span data-ttu-id="85010-550">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="85010-550">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="85010-551">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-551">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="85010-552">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-552">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="85010-553">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-553">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="85010-554">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="85010-554">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="85010-555">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="85010-555">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="85010-556">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="85010-556">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="85010-557">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="85010-557">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="85010-558">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="85010-558">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="85010-559">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="85010-559">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="85010-560">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="85010-560">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="85010-561">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="85010-561">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="85010-562">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="85010-562">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="85010-563">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-563">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="85010-564">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-564">General</span></span>
* <span data-ttu-id="85010-565">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="85010-565">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="85010-566">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="85010-566">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="85010-567">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="85010-567">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="85010-568">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="85010-568">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="85010-569">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="85010-569">Az.Billing</span></span>
  - <span data-ttu-id="85010-570">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-570">Az.Compute</span></span>
  - <span data-ttu-id="85010-571">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="85010-571">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="85010-572">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-572">Az.EventHub</span></span>
  - <span data-ttu-id="85010-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-573">Az.IotHub</span></span>
  - <span data-ttu-id="85010-574">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-574">Az.KeyVault</span></span>
  - <span data-ttu-id="85010-575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-575">Az.Monitor</span></span>
  - <span data-ttu-id="85010-576">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-576">Az.Network</span></span>
  - <span data-ttu-id="85010-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-577">Az.Resources</span></span>
  - <span data-ttu-id="85010-578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-578">Az.Storage</span></span>
  - <span data-ttu-id="85010-579">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-579">Az.Websites</span></span>
* <span data-ttu-id="85010-580">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="85010-580">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="85010-581">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="85010-581">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="85010-582">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="85010-582">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="85010-583">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-583">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-584">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-584">Az.Accounts</span></span>
* <span data-ttu-id="85010-585">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="85010-585">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-586">Az.Compute</span></span>
* <span data-ttu-id="85010-587">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="85010-587">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="85010-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="85010-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="85010-589">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="85010-589">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="85010-590">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="85010-590">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="85010-591">[11354]</span><span class="sxs-lookup"><span data-stu-id="85010-591">[#11354]</span></span>
* <span data-ttu-id="85010-592">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="85010-592">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="85010-593">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="85010-593">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="85010-594">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="85010-594">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="85010-595">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="85010-595">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="85010-596">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="85010-596">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="85010-597">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="85010-597">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="85010-598">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85010-598">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="85010-599">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="85010-599">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="85010-600">[11257]</span><span class="sxs-lookup"><span data-stu-id="85010-600">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-601">Az.DataFactory</span></span>
* <span data-ttu-id="85010-602">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="85010-602">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="85010-603">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="85010-603">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-604">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-604">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-605">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="85010-605">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="85010-606">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="85010-606">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-607">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-607">Az.HDInsight</span></span>
* <span data-ttu-id="85010-608">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="85010-608">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-609">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-609">Az.IotHub</span></span>
* <span data-ttu-id="85010-610">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="85010-610">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="85010-611">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="85010-611">New Cmdlets are:</span></span>
    - <span data-ttu-id="85010-612">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="85010-612">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="85010-613">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="85010-613">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-614">Az.KeyVault</span></span>
* <span data-ttu-id="85010-615">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="85010-615">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-616">Az.Monitor</span></span>
* <span data-ttu-id="85010-617">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="85010-617">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-618">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-618">Az.Network</span></span>
* <span data-ttu-id="85010-619">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="85010-619">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="85010-620">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="85010-620">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="85010-621">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="85010-621">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="85010-622">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="85010-622">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="85010-623">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="85010-623">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="85010-624">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="85010-624">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-625">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-625">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-626">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="85010-626">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-627">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-627">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-628">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-628">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="85010-629">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="85010-629">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="85010-630">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="85010-630">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="85010-631">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="85010-631">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="85010-632">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="85010-632">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="85010-633">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="85010-633">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-634">Az.Resources</span></span>
* <span data-ttu-id="85010-635">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="85010-635">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="85010-636">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="85010-636">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="85010-637">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="85010-637">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="85010-638">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="85010-638">Added example.</span></span>
* <span data-ttu-id="85010-639">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="85010-639">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="85010-640">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="85010-640">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-641">Az.Sql</span></span>
* <span data-ttu-id="85010-642">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="85010-642">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="85010-643">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="85010-643">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="85010-644">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="85010-644">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="85010-645">Az.Support</span><span class="sxs-lookup"><span data-stu-id="85010-645">Az.Support</span></span>
* <span data-ttu-id="85010-646">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="85010-646">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-647">Az.Websites</span></span>
* <span data-ttu-id="85010-648">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-648">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="85010-649">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85010-649">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="85010-650">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85010-650">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="85010-651">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85010-651">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="85010-652">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85010-652">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="85010-653">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-653">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-654">Az.Accounts</span></span>
* <span data-ttu-id="85010-655">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="85010-655">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="85010-656">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="85010-656">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="85010-657">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="85010-657">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-658">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-658">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-659">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="85010-659">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="85010-660">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="85010-660">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="85010-661">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="85010-661">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="85010-662">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="85010-662">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-663">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-663">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-664">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="85010-664">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-665">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-665">Az.IotHub</span></span>
* <span data-ttu-id="85010-666">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-666">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="85010-667">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="85010-667">New Cmdlets are:</span></span>
    - <span data-ttu-id="85010-668">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-668">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="85010-669">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-669">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="85010-670">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-670">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="85010-671">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-671">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="85010-672">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-672">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="85010-673">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="85010-673">New Cmdlets are:</span></span>
    - <span data-ttu-id="85010-674">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="85010-674">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="85010-675">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="85010-675">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="85010-676">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="85010-676">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="85010-677">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="85010-677">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="85010-678">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-678">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="85010-679">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-679">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="85010-680">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-680">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="85010-681">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="85010-681">New Cmdlets are:</span></span>
    - <span data-ttu-id="85010-682">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="85010-682">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="85010-683">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="85010-683">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="85010-684">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="85010-684">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-685">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-685">Az.Monitor</span></span>
* <span data-ttu-id="85010-686">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="85010-686">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-687">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-687">Az.Network</span></span>
* <span data-ttu-id="85010-688">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="85010-688">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="85010-689">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="85010-689">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="85010-690">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="85010-690">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="85010-691">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="85010-691">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-692">Az.Resources</span></span>
* <span data-ttu-id="85010-693">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="85010-693">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="85010-694">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="85010-694">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="85010-695">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="85010-695">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="85010-696">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="85010-696">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="85010-697">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="85010-697">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="85010-698">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="85010-698">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="85010-699">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="85010-699">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="85010-700">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="85010-700">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="85010-701">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="85010-701">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="85010-702">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="85010-702">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="85010-703">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="85010-703">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="85010-704">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="85010-704">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="85010-705">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="85010-705">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="85010-706">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="85010-706">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-707">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-707">Az.Sql</span></span>
* <span data-ttu-id="85010-708">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="85010-708">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="85010-709">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="85010-709">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="85010-710">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="85010-710">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="85010-711">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="85010-711">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="85010-712">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="85010-712">Remove an LTR backup</span></span>
    - <span data-ttu-id="85010-713">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="85010-713">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="85010-714">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="85010-714">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="85010-715">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="85010-715">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="85010-716">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="85010-716">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-717">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-717">Az.Storage</span></span>
* <span data-ttu-id="85010-718">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-718">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="85010-719">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="85010-720">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="85010-720">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="85010-721">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="85010-721">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="85010-722">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="85010-722">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-723">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-723">Az.Websites</span></span>
* <span data-ttu-id="85010-724">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="85010-724">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="85010-725">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="85010-725">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="85010-726">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="85010-726">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="85010-727">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85010-727">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="85010-728">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="85010-728">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="85010-729">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-729">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="85010-730">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-730">Highlights since the last major release</span></span>
* <span data-ttu-id="85010-731">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="85010-731">Updated client side telemetry.</span></span>
* <span data-ttu-id="85010-732">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="85010-732">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="85010-733">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="85010-733">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-734">Az.Accounts</span></span>
* <span data-ttu-id="85010-735">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="85010-735">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-736">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-736">Az.Automation</span></span>
* <span data-ttu-id="85010-737">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-737">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-738">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-738">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-739">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="85010-739">Updated SDK to 7.0</span></span>
* <span data-ttu-id="85010-740">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="85010-740">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-741">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-741">Az.Compute</span></span>
* <span data-ttu-id="85010-742">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="85010-742">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="85010-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-743">Az.FrontDoor</span></span>
* <span data-ttu-id="85010-744">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="85010-744">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-745">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-745">Az.IotHub</span></span>
* <span data-ttu-id="85010-746">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="85010-746">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="85010-747">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="85010-747">New Cmdlets are:</span></span>
    - <span data-ttu-id="85010-748">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-748">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="85010-749">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-749">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="85010-750">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-750">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="85010-751">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="85010-751">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-752">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-752">Az.KeyVault</span></span>
* <span data-ttu-id="85010-753">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="85010-753">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-754">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-754">Az.Monitor</span></span>
* <span data-ttu-id="85010-755">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="85010-755">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="85010-756">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="85010-756">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="85010-757">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="85010-757">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-758">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-758">Az.Network</span></span>
* <span data-ttu-id="85010-759">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="85010-759">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="85010-760">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="85010-760">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="85010-761">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="85010-761">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="85010-762">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-762">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="85010-763">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="85010-763">No new cmdlets are added.</span></span> <span data-ttu-id="85010-764">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="85010-764">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-765">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-765">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-766">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="85010-766">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-767">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-767">Az.Resources</span></span>
* <span data-ttu-id="85010-768">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="85010-768">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="85010-769">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-769">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="85010-770">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-770">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="85010-771">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="85010-771">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="85010-772">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-772">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="85010-773">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="85010-773">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="85010-774">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="85010-774">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="85010-775">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="85010-775">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-776">Az.Sql</span></span>
* <span data-ttu-id="85010-777">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="85010-777">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="85010-778">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="85010-778">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="85010-779">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="85010-779">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="85010-780">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="85010-780">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="85010-781">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="85010-781">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="85010-782">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="85010-782">Az.StorageSync</span></span>
* <span data-ttu-id="85010-783">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="85010-783">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="85010-784">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-784">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="85010-785">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-785">Highlights since the last major release</span></span>
* <span data-ttu-id="85010-786">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="85010-786">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="85010-787">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="85010-787">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-788">Az.Accounts</span></span>
* <span data-ttu-id="85010-789">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="85010-789">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="85010-790">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="85010-790">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-791">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-791">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-792">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="85010-792">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="85010-793">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="85010-793">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="85010-794">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="85010-794">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="85010-795">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="85010-795">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-796">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-796">Az.Compute</span></span>
* <span data-ttu-id="85010-797">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85010-797">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="85010-798">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="85010-798">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="85010-799">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-799">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="85010-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="85010-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="85010-801">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-801">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-802">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-802">Az.DataFactory</span></span>
* <span data-ttu-id="85010-803">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="85010-803">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="85010-804">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="85010-804">Az.DeploymentManager</span></span>
* <span data-ttu-id="85010-805">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="85010-805">Adds LIST operations for resources</span></span>
* <span data-ttu-id="85010-806">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="85010-806">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-807">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-807">Az.HDInsight</span></span>
* <span data-ttu-id="85010-808">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="85010-808">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-809">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-809">Az.KeyVault</span></span>
* <span data-ttu-id="85010-810">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="85010-810">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-811">Az.Network</span></span>
* <span data-ttu-id="85010-812">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="85010-812">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="85010-813">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="85010-813">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="85010-814">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="85010-814">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="85010-815">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="85010-815">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="85010-816">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="85010-816">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="85010-817">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="85010-817">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="85010-818">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="85010-818">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="85010-819">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="85010-819">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="85010-820">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-820">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="85010-822">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-822">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="85010-823">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="85010-823">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="85010-824">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="85010-824">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-825">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-825">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-826">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="85010-826">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="85010-827">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="85010-827">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="85010-828">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="85010-828">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="85010-829">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="85010-829">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-830">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-830">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-831">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="85010-831">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="85010-832">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="85010-832">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-833">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-833">Az.Resources</span></span>
* <span data-ttu-id="85010-834">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="85010-834">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="85010-835">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="85010-835">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-836">Az.Sql</span></span>
<span data-ttu-id="85010-837">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="85010-837">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-838">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-838">Az.Storage</span></span>
* <span data-ttu-id="85010-839">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="85010-839">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="85010-840">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-840">New-AzStorageAccount</span></span>
* <span data-ttu-id="85010-841">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="85010-841">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="85010-842">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="85010-842">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-843">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-843">Az.Websites</span></span>
* <span data-ttu-id="85010-844">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="85010-844">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="85010-845">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="85010-845">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="85010-846">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="85010-846">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-847">Az.Accounts</span></span>
* <span data-ttu-id="85010-848">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="85010-848">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="85010-849">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-849">Az.Cdn</span></span>
* <span data-ttu-id="85010-850">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="85010-850">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-851">Az.Compute</span></span>
* <span data-ttu-id="85010-852">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="85010-852">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="85010-853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="85010-853">Az.ContainerInstance</span></span>
* <span data-ttu-id="85010-854">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-854">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="85010-855">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="85010-855">Az.DataBoxEdge</span></span>
* <span data-ttu-id="85010-856">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="85010-856">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="85010-857">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-857">Get the Edge Storage Container</span></span>
* <span data-ttu-id="85010-858">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="85010-858">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="85010-859">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-859">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="85010-860">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="85010-860">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="85010-861">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-861">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="85010-862">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="85010-862">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="85010-863">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-863">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="85010-864">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="85010-864">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="85010-865">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-865">Get the Edge Storage Account</span></span>
* <span data-ttu-id="85010-866">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="85010-866">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="85010-867">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-867">Create new Edge Storage Account</span></span>
* <span data-ttu-id="85010-868">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="85010-868">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="85010-869">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-869">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="85010-870">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="85010-870">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="85010-871">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="85010-871">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="85010-872">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="85010-872">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="85010-873">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="85010-873">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-874">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-874">Az.DataFactory</span></span>
* <span data-ttu-id="85010-875">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="85010-875">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="85010-876">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="85010-876">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="85010-877">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="85010-877">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="85010-878">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="85010-878">Az.DevTestLabs</span></span>
* <span data-ttu-id="85010-879">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="85010-879">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-880">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-880">Az.EventHub</span></span>
* <span data-ttu-id="85010-881">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="85010-881">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-882">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-882">Az.HDInsight</span></span>
* <span data-ttu-id="85010-883">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="85010-883">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="85010-884">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="85010-884">Az.MachineLearning</span></span>
* <span data-ttu-id="85010-885">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-885">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="85010-886">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="85010-886">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="85010-887">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="85010-887">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="85010-888">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="85010-888">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="85010-889">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="85010-889">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="85010-890">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="85010-890">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="85010-891">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="85010-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="85010-892">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="85010-892">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-893">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-893">Az.Network</span></span>
* <span data-ttu-id="85010-894">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="85010-894">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-895">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-896">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-896">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="85010-897">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-897">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="85010-898">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-898">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="85010-899">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-899">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-900">Az.Resources</span></span>
* <span data-ttu-id="85010-901">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="85010-901">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-902">Az.Sql</span></span>
* <span data-ttu-id="85010-903">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="85010-903">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="85010-904">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="85010-904">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="85010-905">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="85010-905">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="85010-906">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="85010-906">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-907">Az.Storage</span></span>
* <span data-ttu-id="85010-908">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="85010-908">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="85010-909">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="85010-909">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="85010-910">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="85010-910">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="85010-911">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="85010-911">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="85010-912">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-912">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="85010-913">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-913">General</span></span>
* <span data-ttu-id="85010-914">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="85010-914">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-915">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-915">Az.Accounts</span></span>
* <span data-ttu-id="85010-916">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="85010-916">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="85010-917">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="85010-917">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="85010-918">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-918">Az.Batch</span></span>
* <span data-ttu-id="85010-919">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="85010-919">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-920">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-920">Az.DataFactory</span></span>
* <span data-ttu-id="85010-921">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="85010-921">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="85010-922">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-922">Az.FrontDoor</span></span>
* <span data-ttu-id="85010-923">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="85010-923">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="85010-924">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="85010-924">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="85010-925">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="85010-925">Az.HealthcareApis</span></span>
* <span data-ttu-id="85010-926">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="85010-926">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-927">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-927">Az.KeyVault</span></span>
* <span data-ttu-id="85010-928">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="85010-928">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="85010-929">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="85010-929">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="85010-930">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="85010-930">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-931">Az.Monitor</span></span>
* <span data-ttu-id="85010-932">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="85010-932">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="85010-933">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="85010-933">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="85010-934">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="85010-934">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-935">Az.Network</span></span>
* <span data-ttu-id="85010-936">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="85010-936">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-937">Az.Resources</span></span>
* <span data-ttu-id="85010-938">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-938">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="85010-939">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="85010-939">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-940">Az.Sql</span></span>
* <span data-ttu-id="85010-941">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="85010-941">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-942">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-942">Az.Storage</span></span>
* <span data-ttu-id="85010-943">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="85010-943">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="85010-944">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="85010-944">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="85010-945">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="85010-945">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="85010-946">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="85010-946">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="85010-947">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="85010-947">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="85010-948">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="85010-948">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="85010-949">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="85010-949">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="85010-950">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="85010-950">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="85010-951">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="85010-951">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="85010-952">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="85010-952">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="85010-953">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="85010-953">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="85010-954">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="85010-954">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="85010-955">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="85010-955">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="85010-956">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-956">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="85010-957">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-957">Highlights since the last major release</span></span>
* <span data-ttu-id="85010-958">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="85010-958">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="85010-959">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="85010-959">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-960">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-960">Az.Compute</span></span>
* <span data-ttu-id="85010-961">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="85010-961">VM Reapply feature</span></span>
    - <span data-ttu-id="85010-962">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-962">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="85010-963">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="85010-963">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="85010-964">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="85010-964">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="85010-965">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-965">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="85010-966">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="85010-966">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="85010-967">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="85010-967">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="85010-968">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="85010-968">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="85010-969">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="85010-969">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="85010-970">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="85010-970">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="85010-971">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="85010-971">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="85010-972">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="85010-972">Az.DataBoxEdge</span></span>
* <span data-ttu-id="85010-973">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="85010-973">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="85010-974">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="85010-974">Get the Order</span></span>
* <span data-ttu-id="85010-975">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="85010-975">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="85010-976">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="85010-976">Create new Order</span></span>
* <span data-ttu-id="85010-977">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="85010-977">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="85010-978">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="85010-978">Remove the Order</span></span>
* <span data-ttu-id="85010-979">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="85010-979">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="85010-980">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="85010-980">Now creates Local Share</span></span>
* <span data-ttu-id="85010-981">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="85010-981">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="85010-982">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="85010-982">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="85010-983">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="85010-983">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="85010-984">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="85010-984">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="85010-985">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="85010-985">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="85010-986">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="85010-986">Gets the information about Triggers</span></span>
* <span data-ttu-id="85010-987">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="85010-987">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="85010-988">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="85010-988">Create new Triggers</span></span>
* <span data-ttu-id="85010-989">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="85010-989">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="85010-990">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="85010-990">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-991">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-991">Az.DataFactory</span></span>
* <span data-ttu-id="85010-992">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="85010-992">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="85010-993">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="85010-993">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-994">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-994">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-995">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="85010-995">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-996">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-996">Az.EventHub</span></span>
* <span data-ttu-id="85010-997">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="85010-997">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="85010-998">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-998">Az.FrontDoor</span></span>
* <span data-ttu-id="85010-999">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="85010-999">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="85010-1000">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="85010-1000">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="85010-1001">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="85010-1001">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="85010-1002">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="85010-1002">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1003">Az.Network</span></span>
* <span data-ttu-id="85010-1004">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1004">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="85010-1005">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="85010-1005">Az.PrivateDns</span></span>
* <span data-ttu-id="85010-1006">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="85010-1006">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1007">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1007">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1008">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="85010-1008">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="85010-1009">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="85010-1009">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="85010-1010">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="85010-1010">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="85010-1011">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="85010-1011">Az.RedisCache</span></span>
* <span data-ttu-id="85010-1012">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="85010-1012">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="85010-1013">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="85010-1013">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="85010-1014">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="85010-1014">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1015">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1015">Az.Resources</span></span>
- <span data-ttu-id="85010-1016">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="85010-1016">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="85010-1017">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="85010-1017">Updated create policy definition help example</span></span>
- <span data-ttu-id="85010-1018">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="85010-1018">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="85010-1019">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="85010-1019">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="85010-1020">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="85010-1020">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1021">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1021">Az.Sql</span></span>
* <span data-ttu-id="85010-1022">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="85010-1022">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="85010-1023">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="85010-1023">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="85010-1024">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1024">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="85010-1025">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-1025">General</span></span>
* <span data-ttu-id="85010-1026">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="85010-1026">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-1027">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-1027">Az.Accounts</span></span>
* <span data-ttu-id="85010-1028">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="85010-1028">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="85010-1029">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="85010-1029">Az.Advisor</span></span>
* <span data-ttu-id="85010-1030">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="85010-1030">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="85010-1031">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-1031">Az.Batch</span></span>
* <span data-ttu-id="85010-1032">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="85010-1032">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="85010-1033">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="85010-1033">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="85010-1034">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="85010-1034">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="85010-1035">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="85010-1035">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="85010-1036">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="85010-1036">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="85010-1037">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="85010-1037">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="85010-1038">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="85010-1038">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="85010-1039">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="85010-1039">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="85010-1040">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="85010-1040">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="85010-1041">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="85010-1041">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="85010-1042">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="85010-1042">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="85010-1043">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="85010-1043">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="85010-1044">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="85010-1044">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="85010-1045">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="85010-1045">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="85010-1046">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="85010-1046">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="85010-1047">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="85010-1047">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="85010-1048">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="85010-1048">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="85010-1049">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="85010-1049">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="85010-1050">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="85010-1050">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="85010-1051">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="85010-1051">This operation is no longer supported.</span></span>
* <span data-ttu-id="85010-1052">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="85010-1052">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="85010-1053">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="85010-1053">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="85010-1054">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="85010-1054">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="85010-1055">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="85010-1055">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="85010-1056">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="85010-1056">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="85010-1057">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="85010-1057">New non-verified images are also now returned.</span></span> <span data-ttu-id="85010-1058">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="85010-1058">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="85010-1059">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="85010-1059">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="85010-1060">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="85010-1060">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="85010-1061">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="85010-1061">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="85010-1062">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="85010-1062">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="85010-1063">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="85010-1063">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="85010-1064">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="85010-1064">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="85010-1065">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="85010-1065">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="85010-1066">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="85010-1066">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="85010-1067">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="85010-1067">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="85010-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-1068">Az.Cdn</span></span>
* <span data-ttu-id="85010-1069">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="85010-1069">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="85010-1070">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="85010-1070">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1071">Az.Compute</span></span>
* <span data-ttu-id="85010-1072">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="85010-1072">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="85010-1073">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="85010-1073">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="85010-1074">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="85010-1074">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="85010-1075">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="85010-1075">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="85010-1076">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="85010-1076">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="85010-1077">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="85010-1077">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="85010-1078">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="85010-1078">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="85010-1079">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="85010-1079">Breaking changes</span></span>
    - <span data-ttu-id="85010-1080">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="85010-1080">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="85010-1081">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="85010-1081">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-1082">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-1082">Az.DataFactory</span></span>
* <span data-ttu-id="85010-1083">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1083">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-1084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-1084">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-1085">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="85010-1085">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="85010-1086">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="85010-1086">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="85010-1087">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="85010-1087">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="85010-1088">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="85010-1088">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="85010-1089">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="85010-1089">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="85010-1090">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="85010-1090">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="85010-1091">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-1091">Az.FrontDoor</span></span>
* <span data-ttu-id="85010-1092">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="85010-1092">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-1093">Az.HDInsight</span></span>
* <span data-ttu-id="85010-1094">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="85010-1094">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="85010-1095">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="85010-1095">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="85010-1096">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="85010-1096">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="85010-1097">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="85010-1097">Removed five cmdlets:</span></span>
    - <span data-ttu-id="85010-1098">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="85010-1098">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="85010-1099">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="85010-1099">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="85010-1100">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="85010-1100">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="85010-1101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="85010-1101">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="85010-1102">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="85010-1102">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="85010-1103">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="85010-1103">Added three cmdlets:</span></span>
    - <span data-ttu-id="85010-1104">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="85010-1104">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="85010-1105">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="85010-1105">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="85010-1106">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="85010-1106">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="85010-1107">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="85010-1107">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="85010-1108">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="85010-1108">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="85010-1109">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="85010-1109">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="85010-1110">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="85010-1110">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="85010-1111">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="85010-1111">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="85010-1112">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="85010-1112">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="85010-1113">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="85010-1113">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="85010-1114">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="85010-1114">Added some scenario test cases.</span></span>
* <span data-ttu-id="85010-1115">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="85010-1115">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-1116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-1116">Az.IotHub</span></span>
* <span data-ttu-id="85010-1117">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="85010-1117">Breaking changes:</span></span>
    - <span data-ttu-id="85010-1118">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-1118">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="85010-1119">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-1119">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="85010-1120">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-1120">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="85010-1121">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-1121">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="85010-1122">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="85010-1122">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="85010-1123">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="85010-1123">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="85010-1124">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="85010-1124">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="85010-1125">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="85010-1125">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="85010-1126">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-1126">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="85010-1127">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-1127">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="85010-1128">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-1128">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="85010-1129">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="85010-1129">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1130">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1130">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1131">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1131">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="85010-1132">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1132">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="85010-1133">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1133">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="85010-1134">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1134">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="85010-1135">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1135">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="85010-1136">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1136">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="85010-1137">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1137">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="85010-1138">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1138">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="85010-1139">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="85010-1139">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1140">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1140">Az.Resources</span></span>
* <span data-ttu-id="85010-1141">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="85010-1141">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1142">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1142">Az.Network</span></span>
* <span data-ttu-id="85010-1143">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="85010-1143">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="85010-1144">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="85010-1144">Updated cmdlet:</span></span>
        - <span data-ttu-id="85010-1145">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1145">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1146">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1146">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1147">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1147">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1148">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1148">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="85010-1149">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="85010-1150">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="85010-1150">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="85010-1151">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="85010-1151">New cmdlet:</span></span>
        - <span data-ttu-id="85010-1152">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="85010-1152">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="85010-1153">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="85010-1153">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="85010-1154">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85010-1154">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="85010-1155">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="85010-1155">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="85010-1156">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="85010-1156">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="85010-1157">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="85010-1157">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="85010-1158">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="85010-1158">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="85010-1159">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="85010-1159">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="85010-1160">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1160">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-1161">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="85010-1161">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="85010-1162">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-1162">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="85010-1163">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-1163">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="85010-1164">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-1164">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="85010-1165">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="85010-1165">Set-AzVirtualHub</span></span>
* <span data-ttu-id="85010-1166">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="85010-1166">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="85010-1167">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="85010-1167">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="85010-1168">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="85010-1168">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="85010-1169">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="85010-1169">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="85010-1170">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="85010-1170">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="85010-1171">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="85010-1171">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="85010-1172">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="85010-1172">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="85010-1173">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1173">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-1174">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="85010-1174">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="85010-1175">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="85010-1175">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="85010-1176">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="85010-1176">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="85010-1177">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="85010-1177">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="85010-1178">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="85010-1178">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="85010-1179">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="85010-1179">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="85010-1180">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="85010-1180">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="85010-1181">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="85010-1181">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="85010-1182">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1182">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-1183">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="85010-1183">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="85010-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="85010-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="85010-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="85010-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="85010-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="85010-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="85010-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="85010-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="85010-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="85010-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="85010-1189">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="85010-1189">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="85010-1190">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="85010-1190">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="85010-1191">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="85010-1191">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="85010-1192">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="85010-1192">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="85010-1193">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="85010-1193">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="85010-1194">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="85010-1194">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="85010-1195">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="85010-1195">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="85010-1196">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="85010-1196">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="85010-1197">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="85010-1197">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="85010-1198">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="85010-1198">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="85010-1199">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="85010-1199">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="85010-1200">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1200">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-1201">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="85010-1201">New-AzIpGroup</span></span>
        - <span data-ttu-id="85010-1202">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="85010-1202">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="85010-1203">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="85010-1203">Get-AzIpGroup</span></span>
        - <span data-ttu-id="85010-1204">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="85010-1204">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-1206">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="85010-1206">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1207">Az.Sql</span></span>
* <span data-ttu-id="85010-1208">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="85010-1208">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="85010-1209">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="85010-1209">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="85010-1210">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="85010-1210">Removed deprecated aliases:</span></span>
* <span data-ttu-id="85010-1211">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="85010-1211">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="85010-1212">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="85010-1212">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="85010-1213">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-1213">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="85010-1214">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="85010-1214">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="85010-1215">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="85010-1215">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="85010-1216">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="85010-1216">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1217">Az.Storage</span></span>
* <span data-ttu-id="85010-1218">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="85010-1218">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="85010-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1219">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="85010-1220">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1220">Set-AzStorageAccount</span></span>
* <span data-ttu-id="85010-1221">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="85010-1221">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="85010-1222">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="85010-1222">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="85010-1223">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="85010-1223">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="85010-1224">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1224">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="85010-1225">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-1225">General</span></span>
* <span data-ttu-id="85010-1226">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="85010-1226">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-1227">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-1227">Az.Accounts</span></span>
* <span data-ttu-id="85010-1228">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="85010-1228">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-1229">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-1229">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-1230">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="85010-1230">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="85010-1231">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="85010-1231">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-1232">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-1232">Az.Automation</span></span>
* <span data-ttu-id="85010-1233">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="85010-1233">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="85010-1234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-1234">Az.Batch</span></span>
* <span data-ttu-id="85010-1235">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1235">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1236">Az.Compute</span></span>
* <span data-ttu-id="85010-1237">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="85010-1237">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="85010-1238">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="85010-1238">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="85010-1239">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="85010-1239">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="85010-1240">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="85010-1240">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-1241">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-1241">Az.DataFactory</span></span>
* <span data-ttu-id="85010-1242">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="85010-1242">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="85010-1243">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="85010-1243">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="85010-1244">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1244">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-1246">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="85010-1246">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="85010-1247">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="85010-1247">Az.HealthcareApis</span></span>
* <span data-ttu-id="85010-1248">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1248">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="85010-1249">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="85010-1249">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="85010-1250">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="85010-1250">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="85010-1251">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="85010-1251">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-1252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-1252">Az.IotHub</span></span>
* <span data-ttu-id="85010-1253">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="85010-1253">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="85010-1254">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="85010-1254">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-1255">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-1255">Az.Monitor</span></span>
* <span data-ttu-id="85010-1256">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="85010-1256">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="85010-1257">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="85010-1257">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="85010-1258">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="85010-1258">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="85010-1259">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="85010-1259">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1260">Az.Network</span></span>
* <span data-ttu-id="85010-1261">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="85010-1261">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="85010-1262">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="85010-1262">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="85010-1263">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1263">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-1264">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-1264">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="85010-1265">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1265">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="85010-1266">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="85010-1266">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="85010-1267">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1267">Updated cmdlets:</span></span>
        - <span data-ttu-id="85010-1268">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1268">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="85010-1269">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1269">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="85010-1270">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1270">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="85010-1271">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="85010-1271">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="85010-1272">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="85010-1272">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="85010-1273">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="85010-1273">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="85010-1274">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="85010-1274">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="85010-1275">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="85010-1275">Az.RedisCache</span></span>
* <span data-ttu-id="85010-1276">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="85010-1276">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1277">Az.Sql</span></span>
* <span data-ttu-id="85010-1278">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="85010-1278">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1279">Az.Storage</span></span>
* <span data-ttu-id="85010-1280">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1280">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="85010-1281">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="85010-1281">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="85010-1282">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="85010-1282">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="85010-1283">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="85010-1283">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="85010-1284">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1284">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="85010-1285">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="85010-1285">Az.StorageSync</span></span>
* <span data-ttu-id="85010-1286">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="85010-1286">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-1287">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-1287">Az.Websites</span></span>
* <span data-ttu-id="85010-1288">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="85010-1288">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="85010-1289">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1289">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="85010-1290">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-1290">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-1291">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="85010-1291">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="85010-1292">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-1292">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="85010-1293">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="85010-1293">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-1294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-1294">Az.Automation</span></span>
* <span data-ttu-id="85010-1295">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="85010-1295">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="85010-1296">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="85010-1296">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="85010-1297">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="85010-1297">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1298">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1298">Az.Compute</span></span>
* <span data-ttu-id="85010-1299">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1299">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="85010-1300">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1300">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="85010-1301">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="85010-1301">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="85010-1302">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="85010-1302">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="85010-1303">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="85010-1303">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="85010-1304">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="85010-1304">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="85010-1305">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="85010-1305">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="85010-1306">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="85010-1306">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="85010-1307">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-1307">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-1308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-1308">Az.DataFactory</span></span>
* <span data-ttu-id="85010-1309">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="85010-1309">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="85010-1310">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="85010-1310">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-1311">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-1311">Az.HDInsight</span></span>
* <span data-ttu-id="85010-1312">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="85010-1312">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-1313">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-1313">Az.IotHub</span></span>
* <span data-ttu-id="85010-1314">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="85010-1314">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="85010-1315">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="85010-1315">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="85010-1316">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1316">New cmdlets are:</span></span>
    - <span data-ttu-id="85010-1317">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="85010-1317">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="85010-1318">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="85010-1318">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="85010-1319">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="85010-1319">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="85010-1320">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="85010-1320">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-1321">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-1321">Az.Monitor</span></span>
* <span data-ttu-id="85010-1322">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="85010-1322">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="85010-1323">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="85010-1323">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="85010-1324">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="85010-1324">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="85010-1325">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="85010-1325">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="85010-1326">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="85010-1326">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="85010-1327">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="85010-1327">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="85010-1328">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="85010-1328">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="85010-1329">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="85010-1329">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="85010-1330">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="85010-1330">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="85010-1331">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="85010-1331">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="85010-1332">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="85010-1332">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="85010-1333">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="85010-1333">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="85010-1334">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="85010-1334">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="85010-1335">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="85010-1335">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="85010-1336">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="85010-1336">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="85010-1337">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="85010-1337">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="85010-1338">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="85010-1338">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="85010-1339">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="85010-1339">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="85010-1340">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-1340">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="85010-1341">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="85010-1341">Overall improved help files</span></span>
* <span data-ttu-id="85010-1342">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="85010-1342">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1343">Az.Network</span></span>
* <span data-ttu-id="85010-1344">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="85010-1344">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="85010-1345">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="85010-1345">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="85010-1346">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="85010-1346">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="85010-1347">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="85010-1347">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="85010-1348">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="85010-1348">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="85010-1349">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="85010-1349">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="85010-1350">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="85010-1350">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="85010-1351">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="85010-1351">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="85010-1352">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="85010-1352">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="85010-1353">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="85010-1353">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="85010-1354">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1354">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="85010-1355">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="85010-1355">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="85010-1356">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1356">New cmdlets</span></span>
        - <span data-ttu-id="85010-1357">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="85010-1357">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="85010-1358">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="85010-1358">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="85010-1359">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="85010-1359">Updated cmdlet:</span></span>
        - <span data-ttu-id="85010-1360">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="85010-1360">New-VpnSite</span></span>
        - <span data-ttu-id="85010-1361">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="85010-1361">Update-VpnSite</span></span>
        - <span data-ttu-id="85010-1362">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="85010-1362">New-VpnConnection</span></span>
        - <span data-ttu-id="85010-1363">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1363">Update-VpnConnection</span></span>
* <span data-ttu-id="85010-1364">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="85010-1364">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1365">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1365">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1366">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="85010-1366">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="85010-1367">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-1367">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1368">Az.Resources</span></span>
* <span data-ttu-id="85010-1369">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="85010-1369">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-1370">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-1370">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-1371">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="85010-1371">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="85010-1372">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="85010-1372">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="85010-1373">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="85010-1373">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="85010-1374">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="85010-1374">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="85010-1375">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="85010-1375">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="85010-1376">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="85010-1376">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="85010-1377">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="85010-1377">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="85010-1378">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="85010-1378">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="85010-1379">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="85010-1379">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="85010-1380">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="85010-1380">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="85010-1381">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="85010-1381">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="85010-1382">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="85010-1382">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="85010-1383">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="85010-1383">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="85010-1384">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="85010-1384">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="85010-1385">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="85010-1385">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="85010-1386">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="85010-1386">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="85010-1387">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="85010-1387">Az.SignalR</span></span>
* <span data-ttu-id="85010-1388">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="85010-1388">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1389">Az.Sql</span></span>
* <span data-ttu-id="85010-1390">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="85010-1390">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="85010-1391">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="85010-1391">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="85010-1392">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-1392">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="85010-1393">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="85010-1393">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="85010-1394">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="85010-1394">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1395">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1395">Az.Storage</span></span>
* <span data-ttu-id="85010-1396">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="85010-1396">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="85010-1397">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="85010-1397">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="85010-1398">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="85010-1398">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="85010-1399">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="85010-1399">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="85010-1400">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-1400">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="85010-1401">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="85010-1401">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="85010-1402">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="85010-1402">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="85010-1403">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="85010-1403">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="85010-1404">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="85010-1404">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="85010-1405">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="85010-1405">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="85010-1406">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="85010-1406">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-1407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-1407">Az.Websites</span></span>
* <span data-ttu-id="85010-1408">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="85010-1408">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="85010-1409">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="85010-1409">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="85010-1410">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="85010-1410">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="85010-1411">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1411">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="85010-1412">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-1412">General</span></span>
* <span data-ttu-id="85010-1413">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="85010-1413">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-1414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-1414">Az.Accounts</span></span>
* <span data-ttu-id="85010-1415">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="85010-1415">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="85010-1416">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="85010-1416">Az.Aks</span></span>
* <span data-ttu-id="85010-1417">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="85010-1417">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="85010-1418">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="85010-1418">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-1419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-1419">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-1420">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="85010-1420">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="85010-1421">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="85010-1421">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="85010-1422">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="85010-1422">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="85010-1423">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="85010-1423">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="85010-1424">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="85010-1424">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="85010-1425">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-1425">Az.Batch</span></span>
* <span data-ttu-id="85010-1426">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="85010-1426">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="85010-1427">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-1427">Az.Cdn</span></span>
* <span data-ttu-id="85010-1428">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="85010-1428">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1429">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1429">Az.Compute</span></span>
* <span data-ttu-id="85010-1430">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1430">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="85010-1431">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="85010-1431">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="85010-1432">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85010-1432">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="85010-1433">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-1433">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="85010-1434">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="85010-1434">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="85010-1435">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-1435">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="85010-1436">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-1436">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="85010-1437">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="85010-1437">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-1438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-1438">Az.DataFactory</span></span>
* <span data-ttu-id="85010-1439">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="85010-1439">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="85010-1440">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="85010-1440">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="85010-1441">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="85010-1441">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="85010-1442">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="85010-1442">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-1444">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="85010-1444">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-1445">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-1445">Az.EventHub</span></span>
* <span data-ttu-id="85010-1446">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="85010-1446">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="85010-1447">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="85010-1447">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="85010-1448">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="85010-1448">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="85010-1449">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="85010-1449">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="85010-1450">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="85010-1450">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="85010-1451">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="85010-1451">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-1452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-1452">Az.Monitor</span></span>
* <span data-ttu-id="85010-1453">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="85010-1453">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1454">Az.Network</span></span>
* <span data-ttu-id="85010-1455">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1455">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="85010-1456">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="85010-1456">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="85010-1457">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="85010-1457">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="85010-1458">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="85010-1458">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="85010-1459">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="85010-1459">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="85010-1460">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="85010-1460">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="85010-1461">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="85010-1461">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-1462">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1462">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-1463">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="85010-1463">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="85010-1464">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="85010-1464">Added example</span></span>
    - <span data-ttu-id="85010-1465">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="85010-1465">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="85010-1466">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="85010-1466">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="85010-1467">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="85010-1467">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1468">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1469">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1469">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1470">Az.Resources</span></span>
* <span data-ttu-id="85010-1471">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="85010-1471">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="85010-1472">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="85010-1472">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="85010-1473">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="85010-1473">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="85010-1474">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="85010-1474">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="85010-1475">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="85010-1475">Az.ServiceBus</span></span>
* <span data-ttu-id="85010-1476">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="85010-1476">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="85010-1477">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="85010-1477">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="85010-1478">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="85010-1478">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-1479">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-1479">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-1480">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="85010-1480">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="85010-1481">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="85010-1481">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="85010-1482">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="85010-1482">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="85010-1483">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="85010-1483">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="85010-1484">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="85010-1484">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="85010-1485">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="85010-1485">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1486">Az.Sql</span></span>
* <span data-ttu-id="85010-1487">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="85010-1487">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1488">Az.Storage</span></span>
* <span data-ttu-id="85010-1489">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="85010-1489">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="85010-1490">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="85010-1490">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="85010-1491">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="85010-1491">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="85010-1492">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="85010-1492">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="85010-1493">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="85010-1493">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="85010-1494">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="85010-1494">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-1495">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-1495">Az.Websites</span></span>
* <span data-ttu-id="85010-1496">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="85010-1496">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="85010-1497">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1497">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-1498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-1498">Az.Accounts</span></span>
* <span data-ttu-id="85010-1499">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="85010-1499">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="85010-1500">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1500">Az.ApplicationInsights</span></span>
* <span data-ttu-id="85010-1501">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="85010-1501">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-1502">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-1502">Az.Automation</span></span>
* <span data-ttu-id="85010-1503">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="85010-1503">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-1504">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-1504">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-1505">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="85010-1505">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1506">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1506">Az.Compute</span></span>
* <span data-ttu-id="85010-1507">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85010-1507">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="85010-1508">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="85010-1508">Az.ContainerRegistry</span></span>
* <span data-ttu-id="85010-1509">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="85010-1509">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="85010-1510">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="85010-1510">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-1511">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-1511">Az.DataFactory</span></span>
* <span data-ttu-id="85010-1512">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1512">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="85010-1513">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="85010-1513">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-1514">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-1514">Az.EventHub</span></span>
* <span data-ttu-id="85010-1515">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="85010-1515">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="85010-1516">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="85010-1516">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-1517">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-1517">Az.KeyVault</span></span>
* <span data-ttu-id="85010-1518">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="85010-1518">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="85010-1519">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="85010-1519">Az.LogicApp</span></span>
* <span data-ttu-id="85010-1520">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="85010-1520">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="85010-1521">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="85010-1521">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="85010-1522">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="85010-1522">Az.ManagedServices</span></span>
* <span data-ttu-id="85010-1523">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="85010-1523">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1524">Az.Network</span></span>
* <span data-ttu-id="85010-1525">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="85010-1525">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="85010-1526">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1526">New cmdlets</span></span>
        - <span data-ttu-id="85010-1527">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="85010-1527">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="85010-1528">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="85010-1528">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="85010-1529">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1529">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1530">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1530">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1531">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1531">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1532">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1532">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="85010-1533">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="85010-1533">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="85010-1534">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="85010-1534">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="85010-1535">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-1535">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="85010-1536">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1536">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="85010-1537">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="85010-1537">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="85010-1538">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="85010-1538">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="85010-1539">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="85010-1539">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="85010-1540">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="85010-1540">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="85010-1541">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1541">Updated cmdlets</span></span>
        - <span data-ttu-id="85010-1542">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1542">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="85010-1543">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1543">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="85010-1544">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1544">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="85010-1545">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="85010-1545">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="85010-1546">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-1546">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="85010-1547">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="85010-1547">Updated cmdlet:</span></span>
        - <span data-ttu-id="85010-1548">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1548">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="85010-1549">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1549">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="85010-1550">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="85010-1550">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="85010-1551">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="85010-1551">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="85010-1552">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="85010-1552">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="85010-1553">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="85010-1553">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-1554">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1554">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-1555">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="85010-1555">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="85010-1556">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="85010-1556">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1557">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1558">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1558">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="85010-1559">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1559">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="85010-1560">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1560">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="85010-1561">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1561">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="85010-1562">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1562">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="85010-1563">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1563">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="85010-1564">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1564">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="85010-1565">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1565">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="85010-1566">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1566">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="85010-1567">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="85010-1567">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1568">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1568">Az.Resources</span></span>
- <span data-ttu-id="85010-1569">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-1569">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="85010-1570">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="85010-1570">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="85010-1571">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="85010-1571">Az.ServiceBus</span></span>
* <span data-ttu-id="85010-1572">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="85010-1572">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="85010-1573">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="85010-1573">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1574">Az.Sql</span></span>
* <span data-ttu-id="85010-1575">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="85010-1575">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="85010-1576">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="85010-1576">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="85010-1577">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="85010-1577">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1578">Az.Storage</span></span>
* <span data-ttu-id="85010-1579">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-1579">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="85010-1580">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="85010-1580">Az.StorageSync</span></span>
* <span data-ttu-id="85010-1581">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="85010-1581">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="85010-1582">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="85010-1582">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-1583">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-1583">Az.Websites</span></span>
* <span data-ttu-id="85010-1584">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="85010-1584">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="85010-1585">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="85010-1585">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="85010-1586">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="85010-1586">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="85010-1587">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1587">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-1588">Az.Accounts</span></span>
* <span data-ttu-id="85010-1589">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="85010-1589">Add support for profile cmdlets</span></span>
* <span data-ttu-id="85010-1590">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="85010-1590">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="85010-1591">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="85010-1591">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="85010-1592">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="85010-1592">Az.Advisor</span></span>
* <span data-ttu-id="85010-1593">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="85010-1593">GA release of Az.Advisor</span></span>
* <span data-ttu-id="85010-1594">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="85010-1594">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="85010-1595">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-1595">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-1596">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="85010-1596">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="85010-1597">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="85010-1597">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="85010-1598">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="85010-1598">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="85010-1599">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="85010-1599">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="85010-1600">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="85010-1600">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="85010-1601">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="85010-1601">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="85010-1602">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="85010-1602">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-1603">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-1603">Az.Automation</span></span>
* <span data-ttu-id="85010-1604">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="85010-1604">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1605">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1605">Az.Compute</span></span>
* <span data-ttu-id="85010-1606">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="85010-1606">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-1607">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-1607">Az.DataFactory</span></span>
* <span data-ttu-id="85010-1608">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="85010-1608">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="85010-1609">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="85010-1609">Az.EventGrid</span></span>
* <span data-ttu-id="85010-1610">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="85010-1610">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-1611">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-1611">Az.IotHub</span></span>
* <span data-ttu-id="85010-1612">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="85010-1612">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1613">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1613">Az.Network</span></span>
* <span data-ttu-id="85010-1614">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="85010-1614">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="85010-1615">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="85010-1615">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-1616">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1616">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-1617">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="85010-1617">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="85010-1618">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="85010-1618">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-1620">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="85010-1620">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1621">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1621">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1622">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="85010-1622">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1623">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1623">Az.Resources</span></span>
    - <span data-ttu-id="85010-1624">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="85010-1624">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="85010-1625">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="85010-1625">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="85010-1626">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="85010-1626">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="85010-1627">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="85010-1627">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="85010-1628">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="85010-1628">Az.ServiceBus</span></span>
* <span data-ttu-id="85010-1629">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="85010-1629">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1630">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1630">Az.Sql</span></span>
* <span data-ttu-id="85010-1631">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="85010-1631">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="85010-1632">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="85010-1632">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="85010-1633">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="85010-1633">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="85010-1634">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="85010-1634">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="85010-1635">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="85010-1635">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="85010-1636">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="85010-1636">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="85010-1637">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="85010-1637">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="85010-1638">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="85010-1638">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="85010-1639">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="85010-1639">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1640">Az.Storage</span></span>
* <span data-ttu-id="85010-1641">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="85010-1641">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="85010-1642">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="85010-1642">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="85010-1643">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="85010-1643">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="85010-1644">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="85010-1644">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="85010-1645">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="85010-1645">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="85010-1646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1646">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="85010-1647">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1647">Set-AzStorageAccount</span></span>
* <span data-ttu-id="85010-1648">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="85010-1648">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="85010-1649">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="85010-1649">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="85010-1650">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="85010-1650">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="85010-1651">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="85010-1651">Az.StorageSync</span></span>
* <span data-ttu-id="85010-1652">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="85010-1652">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="85010-1653">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1653">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-1654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-1654">Az.Accounts</span></span>
* <span data-ttu-id="85010-1655">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="85010-1655">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="85010-1656">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="85010-1656">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="85010-1657">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="85010-1657">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="85010-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="85010-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="85010-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="85010-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1660">Az.Compute</span></span>
* <span data-ttu-id="85010-1661">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-1661">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="85010-1662">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-1662">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="85010-1663">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="85010-1663">Az.Dns</span></span>
* <span data-ttu-id="85010-1664">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="85010-1664">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="85010-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="85010-1665">Az.EventGrid</span></span>
* <span data-ttu-id="85010-1666">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="85010-1666">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="85010-1667">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1667">New cmdlets:</span></span>
    - <span data-ttu-id="85010-1668">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="85010-1668">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="85010-1669">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1669">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="85010-1670">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="85010-1670">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="85010-1671">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1671">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="85010-1672">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="85010-1672">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="85010-1673">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1673">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="85010-1674">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="85010-1674">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="85010-1675">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1675">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="85010-1676">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="85010-1676">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="85010-1677">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="85010-1677">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="85010-1678">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="85010-1678">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="85010-1679">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1679">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="85010-1680">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="85010-1680">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="85010-1681">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1681">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="85010-1682">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="85010-1682">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="85010-1683">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1683">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="85010-1684">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-1684">Updated cmdlets:</span></span>
    - <span data-ttu-id="85010-1685">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="85010-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="85010-1686">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="85010-1686">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="85010-1687">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="85010-1687">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="85010-1688">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="85010-1688">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="85010-1689">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="85010-1689">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="85010-1690">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="85010-1690">Event subscription expiration date,</span></span>
            - <span data-ttu-id="85010-1691">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="85010-1691">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="85010-1692">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="85010-1692">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="85010-1693">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="85010-1693">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="85010-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="85010-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="85010-1695">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="85010-1695">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="85010-1696">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="85010-1696">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="85010-1697">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="85010-1697">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="85010-1698">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="85010-1698">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="85010-1699">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-1699">Az.FrontDoor</span></span>
* <span data-ttu-id="85010-1700">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="85010-1700">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="85010-1701">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="85010-1701">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="85010-1702">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="85010-1702">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="85010-1703">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="85010-1703">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1704">Az.Network</span></span>
* <span data-ttu-id="85010-1705">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-1705">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="85010-1706">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1706">New cmdlets</span></span>
        - <span data-ttu-id="85010-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="85010-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="85010-1708">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="85010-1708">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="85010-1709">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1709">New cmdlets</span></span>
        - <span data-ttu-id="85010-1710">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="85010-1710">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="85010-1711">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="85010-1711">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="85010-1712">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1712">New cmdlets</span></span>
        - <span data-ttu-id="85010-1713">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85010-1713">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="85010-1714">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85010-1714">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="85010-1715">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85010-1715">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="85010-1716">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="85010-1716">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="85010-1717">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="85010-1717">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="85010-1718">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="85010-1718">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="85010-1719">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1719">New cmdlets</span></span>
        - <span data-ttu-id="85010-1720">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="85010-1720">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="85010-1721">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="85010-1721">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="85010-1722">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="85010-1722">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="85010-1723">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="85010-1723">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="85010-1724">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="85010-1724">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="85010-1725">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="85010-1725">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="85010-1726">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="85010-1726">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="85010-1727">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="85010-1727">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="85010-1728">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="85010-1728">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="85010-1729">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="85010-1729">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="85010-1730">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-1730">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="85010-1731">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="85010-1731">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="85010-1732">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-1732">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="85010-1733">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="85010-1733">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="85010-1734">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="85010-1734">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="85010-1735">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="85010-1735">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="85010-1736">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="85010-1736">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="85010-1737">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1737">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="85010-1738">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="85010-1738">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="85010-1739">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="85010-1739">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="85010-1740">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-1740">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="85010-1741">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="85010-1741">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="85010-1742">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="85010-1742">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="85010-1743">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-1743">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="85010-1744">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="85010-1744">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="85010-1745">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="85010-1745">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="85010-1746">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="85010-1746">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-1747">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1747">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-1748">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="85010-1748">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1749">Az.Resources</span></span>
* <span data-ttu-id="85010-1750">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="85010-1750">Support for additional Template Export options</span></span>
    - <span data-ttu-id="85010-1751">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="85010-1751">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="85010-1752">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="85010-1752">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="85010-1753">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85010-1753">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-1754">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-1754">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-1755">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="85010-1755">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1756">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1756">Az.Sql</span></span>
* <span data-ttu-id="85010-1757">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="85010-1757">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="85010-1758">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="85010-1758">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="85010-1759">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="85010-1759">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="85010-1760">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85010-1760">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="85010-1761">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85010-1761">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="85010-1762">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85010-1762">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="85010-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="85010-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="85010-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="85010-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1765">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1765">Az.Storage</span></span>
* <span data-ttu-id="85010-1766">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-1766">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="85010-1767">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1767">New-AzStorageAccount</span></span>
* <span data-ttu-id="85010-1768">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="85010-1768">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="85010-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-1770">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-1770">Az.Websites</span></span>
* <span data-ttu-id="85010-1771">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="85010-1771">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="85010-1772">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="85010-1772">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="85010-1773">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1773">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="85010-1774">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-1774">Az.Cdn</span></span>
* <span data-ttu-id="85010-1775">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="85010-1775">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1776">Az.Compute</span></span>
* <span data-ttu-id="85010-1777">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="85010-1777">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="85010-1778">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-1778">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-1779">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-1779">Az.EventHub</span></span>
* <span data-ttu-id="85010-1780">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="85010-1780">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="85010-1781">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="85010-1781">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1782">Az.Network</span></span>
* <span data-ttu-id="85010-1783">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="85010-1783">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="85010-1784">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="85010-1784">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-1785">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1785">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-1786">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="85010-1786">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1787">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1787">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1788">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="85010-1788">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="85010-1789">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="85010-1789">Az.ServiceBus</span></span>
* <span data-ttu-id="85010-1790">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="85010-1790">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-1791">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-1791">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-1792">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="85010-1792">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="85010-1793">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="85010-1793">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1794">Az.Sql</span></span>
* <span data-ttu-id="85010-1795">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="85010-1795">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="85010-1796">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="85010-1796">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="85010-1797">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="85010-1797">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="85010-1798">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="85010-1798">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-1799">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-1799">Az.Websites</span></span>
* <span data-ttu-id="85010-1800">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="85010-1800">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="85010-1801">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1801">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="85010-1802">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-1802">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-1803">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="85010-1803">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="85010-1804">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="85010-1804">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="85010-1805">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="85010-1805">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="85010-1806">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="85010-1806">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="85010-1807">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="85010-1807">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="85010-1808">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="85010-1808">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="85010-1809">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="85010-1809">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="85010-1810">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="85010-1810">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="85010-1811">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="85010-1811">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="85010-1812">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="85010-1812">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="85010-1813">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-1813">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="85010-1814">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="85010-1814">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="85010-1815">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="85010-1815">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="85010-1816">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="85010-1816">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="85010-1817">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="85010-1817">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="85010-1818">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="85010-1818">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="85010-1819">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="85010-1819">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="85010-1820">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="85010-1820">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="85010-1821">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="85010-1821">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="85010-1822">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="85010-1822">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="85010-1823">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="85010-1823">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="85010-1824">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="85010-1824">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="85010-1825">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="85010-1825">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="85010-1826">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="85010-1826">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="85010-1827">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="85010-1827">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="85010-1828">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="85010-1828">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="85010-1829">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="85010-1829">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="85010-1830">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="85010-1830">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="85010-1831">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="85010-1831">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="85010-1832">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="85010-1832">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="85010-1833">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="85010-1833">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="85010-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="85010-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="85010-1835">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1835">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="85010-1836">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="85010-1836">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="85010-1837">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="85010-1837">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="85010-1838">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="85010-1838">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="85010-1839">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="85010-1839">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="85010-1840">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="85010-1840">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="85010-1841">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="85010-1841">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="85010-1842">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="85010-1842">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="85010-1843">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="85010-1843">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="85010-1844">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="85010-1844">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="85010-1845">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="85010-1845">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="85010-1846">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="85010-1846">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="85010-1847">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="85010-1847">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="85010-1848">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="85010-1848">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="85010-1849">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="85010-1849">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="85010-1850">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="85010-1850">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="85010-1851">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="85010-1851">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="85010-1852">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="85010-1852">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="85010-1853">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="85010-1853">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="85010-1854">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="85010-1854">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="85010-1855">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="85010-1855">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="85010-1856">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="85010-1856">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="85010-1857">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="85010-1857">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="85010-1858">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-1858">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="85010-1859">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="85010-1859">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="85010-1860">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="85010-1860">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="85010-1861">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="85010-1861">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="85010-1862">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="85010-1862">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="85010-1863">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="85010-1863">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="85010-1864">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="85010-1864">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="85010-1865">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="85010-1865">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="85010-1866">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="85010-1866">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="85010-1867">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="85010-1867">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="85010-1868">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="85010-1868">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="85010-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="85010-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="85010-1870">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="85010-1870">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="85010-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="85010-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="85010-1872">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="85010-1872">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="85010-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="85010-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="85010-1874">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="85010-1874">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="85010-1875">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="85010-1875">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="85010-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="85010-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="85010-1877">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="85010-1877">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="85010-1878">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="85010-1878">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="85010-1879">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="85010-1879">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-1880">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-1880">Az.Automation</span></span>
* <span data-ttu-id="85010-1881">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="85010-1881">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="85010-1882">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="85010-1882">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="85010-1883">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="85010-1883">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="85010-1884">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="85010-1884">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="85010-1885">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="85010-1885">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="85010-1886">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="85010-1886">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="85010-1887">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="85010-1887">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1888">Az.Compute</span></span>
* <span data-ttu-id="85010-1889">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="85010-1889">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="85010-1890">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="85010-1890">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-1891">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-1891">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-1892">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="85010-1892">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-1893">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-1893">Az.Monitor</span></span>
* <span data-ttu-id="85010-1894">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="85010-1894">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1895">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1895">Az.Network</span></span>
* <span data-ttu-id="85010-1896">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="85010-1896">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="85010-1897">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="85010-1897">Updated cmdlet:</span></span>
        - <span data-ttu-id="85010-1898">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="85010-1898">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="85010-1899">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="85010-1899">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-1900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-1900">Az.Resources</span></span>
* <span data-ttu-id="85010-1901">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="85010-1901">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-1902">Az.Sql</span></span>
* <span data-ttu-id="85010-1903">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85010-1903">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="85010-1904">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1904">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-1905">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-1905">Az.Accounts</span></span>
* <span data-ttu-id="85010-1906">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="85010-1906">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-1907">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-1907">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-1908">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="85010-1908">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="85010-1909">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="85010-1909">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-1910">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-1910">Az.Compute</span></span>
* <span data-ttu-id="85010-1911">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="85010-1911">Proximity placement group feature.</span></span>
    - <span data-ttu-id="85010-1912">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="85010-1912">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="85010-1913">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="85010-1913">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="85010-1914">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="85010-1914">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="85010-1915">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="85010-1915">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="85010-1916">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="85010-1916">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="85010-1917">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="85010-1917">Breaking changes</span></span>
    - <span data-ttu-id="85010-1918">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="85010-1918">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="85010-1919">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="85010-1919">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="85010-1920">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="85010-1920">Az.DeploymentManager</span></span>
* <span data-ttu-id="85010-1921">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="85010-1921">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="85010-1922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="85010-1922">Az.Dns</span></span>
* <span data-ttu-id="85010-1923">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="85010-1923">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="85010-1924">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="85010-1924">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="85010-1925">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="85010-1925">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="85010-1926">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-1926">Az.FrontDoor</span></span>
* <span data-ttu-id="85010-1927">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="85010-1927">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="85010-1928">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="85010-1928">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="85010-1929">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-1929">Az.HDInsight</span></span>
* <span data-ttu-id="85010-1930">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="85010-1930">Removed two cmdlets:</span></span>
    - <span data-ttu-id="85010-1931">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="85010-1931">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="85010-1932">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="85010-1932">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="85010-1933">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="85010-1933">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="85010-1934">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="85010-1934">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="85010-1935">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="85010-1935">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="85010-1936">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="85010-1936">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-1937">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-1937">Az.Monitor</span></span>
* <span data-ttu-id="85010-1938">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="85010-1938">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="85010-1939">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="85010-1939">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="85010-1940">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="85010-1940">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="85010-1941">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="85010-1941">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="85010-1942">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="85010-1942">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="85010-1943">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="85010-1943">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="85010-1944">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="85010-1944">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="85010-1945">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="85010-1945">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="85010-1946">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="85010-1946">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="85010-1947">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="85010-1947">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="85010-1948">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="85010-1948">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="85010-1949">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="85010-1949">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="85010-1950">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="85010-1950">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="85010-1951">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="85010-1951">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-1952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-1952">Az.Network</span></span>
* <span data-ttu-id="85010-1953">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="85010-1953">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="85010-1954">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1954">New cmdlets</span></span>
        - <span data-ttu-id="85010-1955">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="85010-1955">New-AzNatGateway</span></span>
        - <span data-ttu-id="85010-1956">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="85010-1956">Get-AzNatGateway</span></span>
        - <span data-ttu-id="85010-1957">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="85010-1957">Set-AzNatGateway</span></span>
        - <span data-ttu-id="85010-1958">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="85010-1958">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="85010-1959">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="85010-1959">Updated cmdlets</span></span>
        - <span data-ttu-id="85010-1960">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="85010-1960">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="85010-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="85010-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="85010-1962">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="85010-1962">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="85010-1963">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="85010-1963">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="85010-1964">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="85010-1964">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-1965">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-1965">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-1966">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="85010-1966">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="85010-1967">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="85010-1967">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="85010-1968">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="85010-1968">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-1969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-1969">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-1970">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="85010-1970">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="85010-1971">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="85010-1971">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="85010-1972">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="85010-1972">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="85010-1973">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="85010-1973">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="85010-1974">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="85010-1974">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="85010-1975">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="85010-1975">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="85010-1976">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="85010-1976">Az.Relay</span></span>
* <span data-ttu-id="85010-1977">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="85010-1977">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="85010-1978">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="85010-1978">Az.ServiceBus</span></span>
* <span data-ttu-id="85010-1979">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="85010-1979">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-1980">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-1980">Az.Storage</span></span>
* <span data-ttu-id="85010-1981">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="85010-1981">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="85010-1982">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="85010-1982">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="85010-1983">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="85010-1983">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="85010-1984">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1984">New-AzStorageAccount</span></span>
* <span data-ttu-id="85010-1985">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="85010-1985">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="85010-1986">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1986">New-AzStorageAccount</span></span>
    - <span data-ttu-id="85010-1987">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1987">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="85010-1988">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-1988">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-1989">Az.Websites</span></span>
* <span data-ttu-id="85010-1990">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="85010-1990">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="85010-1991">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="85010-1991">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="85010-1992">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-1992">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="85010-1993">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-1993">Highlights since the last major release</span></span>
* <span data-ttu-id="85010-1994">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="85010-1994">General availability of `Az` module</span></span>
* <span data-ttu-id="85010-1995">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="85010-1995">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="85010-1996">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="85010-1996">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="85010-1997">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="85010-1997">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="85010-1998">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="85010-1998">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="85010-1999">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="85010-1999">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="85010-2000">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="85010-2000">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-2001">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2001">Az.Accounts</span></span>
* <span data-ttu-id="85010-2002">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="85010-2002">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="85010-2003">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-2003">Az.Batch</span></span>
* <span data-ttu-id="85010-2004">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2004">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="85010-2005">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-2005">Az.Cdn</span></span>
* <span data-ttu-id="85010-2006">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2006">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-2008">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2008">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2009">Az.Compute</span></span>
* <span data-ttu-id="85010-2010">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="85010-2010">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="85010-2011">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="85010-2012">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="85010-2012">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-2013">Az.DataFactory</span></span>
* <span data-ttu-id="85010-2014">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="85010-2014">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-2015">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2015">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-2016">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="85010-2017">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="85010-2017">Az.EventGrid</span></span>
* <span data-ttu-id="85010-2018">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="85010-2018">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-2019">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-2019">Az.EventHub</span></span>
* <span data-ttu-id="85010-2020">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="85010-2020">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="85010-2021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="85010-2021">Az.HDInsight</span></span>
* <span data-ttu-id="85010-2022">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2022">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-2023">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-2023">Az.IotHub</span></span>
* <span data-ttu-id="85010-2024">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2024">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-2025">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-2025">Az.KeyVault</span></span>
* <span data-ttu-id="85010-2026">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="85010-2027">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="85010-2027">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="85010-2028">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="85010-2028">Az.MachineLearning</span></span>
* <span data-ttu-id="85010-2029">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="85010-2030">Az.Media</span><span class="sxs-lookup"><span data-stu-id="85010-2030">Az.Media</span></span>
* <span data-ttu-id="85010-2031">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-2032">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-2032">Az.Monitor</span></span>
  * <span data-ttu-id="85010-2033">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="85010-2033">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="85010-2034">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="85010-2034">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="85010-2035">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="85010-2035">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="85010-2036">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="85010-2036">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="85010-2037">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="85010-2037">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="85010-2038">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="85010-2038">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="85010-2039">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="85010-2039">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2040">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2040">Az.Network</span></span>
* <span data-ttu-id="85010-2041">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2041">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="85010-2042">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="85010-2042">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="85010-2043">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="85010-2043">Az.NotificationHubs</span></span>
* <span data-ttu-id="85010-2044">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2044">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-2045">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-2045">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-2046">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2046">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="85010-2047">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="85010-2047">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="85010-2048">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2048">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-2050">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2050">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="85010-2051">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2051">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="85010-2052">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2052">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="85010-2053">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="85010-2053">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="85010-2054">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="85010-2054">Az.RedisCache</span></span>
* <span data-ttu-id="85010-2055">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2055">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2056">Az.Resources</span></span>
* <span data-ttu-id="85010-2057">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="85010-2057">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2058">Az.Sql</span></span>
* <span data-ttu-id="85010-2059">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="85010-2059">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="85010-2060">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2060">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="85010-2061">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="85010-2061">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="85010-2062">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="85010-2062">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="85010-2063">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="85010-2063">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="85010-2064">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="85010-2064">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="85010-2065">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="85010-2065">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-2066">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2066">Az.Websites</span></span>
* <span data-ttu-id="85010-2067">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="85010-2067">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="85010-2068">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="85010-2068">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="85010-2069">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="85010-2069">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="85010-2070">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="85010-2070">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="85010-2071">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2071">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="85010-2072">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-2072">Highlights since the last major release</span></span>
* <span data-ttu-id="85010-2073">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="85010-2073">General availability of `Az` module</span></span>
* <span data-ttu-id="85010-2074">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="85010-2074">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="85010-2075">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="85010-2075">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="85010-2076">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="85010-2076">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="85010-2077">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="85010-2077">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="85010-2078">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="85010-2078">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="85010-2079">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="85010-2079">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="85010-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2080">Az.Accounts</span></span>
* <span data-ttu-id="85010-2081">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="85010-2081">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="85010-2082">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="85010-2082">Az.AnalysisServices</span></span>
* <span data-ttu-id="85010-2083">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="85010-2083">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="85010-2084">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="85010-2084">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-2085">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-2085">Az.Automation</span></span>
* <span data-ttu-id="85010-2086">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="85010-2086">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="85010-2087">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="85010-2087">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="85010-2088">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2088">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2089">Az.Compute</span></span>
* <span data-ttu-id="85010-2090">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="85010-2090">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="85010-2091">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="85010-2091">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="85010-2092">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="85010-2092">Az.ContainerInstance</span></span>
* <span data-ttu-id="85010-2093">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="85010-2093">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-2094">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-2094">Az.DataFactory</span></span>
* <span data-ttu-id="85010-2095">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="85010-2095">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="85010-2096">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-2096">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2097">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2097">Az.Resources</span></span>
* <span data-ttu-id="85010-2098">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="85010-2098">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="85010-2099">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-2099">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="85010-2100">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="85010-2100">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="85010-2101">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="85010-2101">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="85010-2102">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="85010-2102">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="85010-2103">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="85010-2103">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2104">Az.Sql</span></span>
* <span data-ttu-id="85010-2105">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="85010-2105">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-2106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-2106">Az.Storage</span></span>
* <span data-ttu-id="85010-2107">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2107">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="85010-2108">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="85010-2108">New-AzStorageContext</span></span>
* <span data-ttu-id="85010-2109">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="85010-2109">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="85010-2110">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="85010-2110">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="85010-2111">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="85010-2111">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="85010-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="85010-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="85010-2114">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="85010-2114">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="85010-2115">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="85010-2115">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="85010-2116">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="85010-2116">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="85010-2117">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="85010-2117">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="85010-2118">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="85010-2118">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="85010-2119">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2119">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="85010-2120">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="85010-2120">Highlights since the last major release</span></span>
* <span data-ttu-id="85010-2121">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="85010-2121">General availability of `Az` module</span></span>
* <span data-ttu-id="85010-2122">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="85010-2122">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="85010-2123">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="85010-2123">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="85010-2124">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="85010-2124">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="85010-2125">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="85010-2125">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="85010-2126">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="85010-2126">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="85010-2127">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="85010-2127">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-2128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-2128">Az.Automation</span></span>
* <span data-ttu-id="85010-2129">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="85010-2129">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="85010-2130">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="85010-2130">Dynamic grouping</span></span>
    * <span data-ttu-id="85010-2131">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="85010-2131">Pre-Post script</span></span>
    * <span data-ttu-id="85010-2132">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="85010-2132">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2133">Az.Compute</span></span>
* <span data-ttu-id="85010-2134">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="85010-2134">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="85010-2135">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="85010-2135">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-2136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-2136">Az.KeyVault</span></span>
* <span data-ttu-id="85010-2137">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="85010-2137">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2138">Az.Network</span></span>
* <span data-ttu-id="85010-2139">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2139">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="85010-2140">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="85010-2140">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-2141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-2141">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-2142">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="85010-2142">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="85010-2143">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="85010-2143">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2144">Az.Resources</span></span>
* <span data-ttu-id="85010-2145">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-2145">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="85010-2146">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="85010-2146">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2147">Az.Sql</span></span>
* <span data-ttu-id="85010-2148">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="85010-2148">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-2149">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-2149">Az.Storage</span></span>
* <span data-ttu-id="85010-2150">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-2150">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="85010-2151">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-2151">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="85010-2152">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-2152">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="85010-2153">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="85010-2153">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="85010-2154">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="85010-2154">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="85010-2155">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="85010-2155">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="85010-2156">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="85010-2156">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-2157">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2157">Az.Websites</span></span>
* <span data-ttu-id="85010-2158">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="85010-2158">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="85010-2159">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2159">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-2160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2160">Az.Accounts</span></span>
* <span data-ttu-id="85010-2161">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="85010-2161">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="85010-2162">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="85010-2162">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-2163">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-2163">Az.Automation</span></span>
* <span data-ttu-id="85010-2164">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2164">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="85010-2165">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="85010-2165">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="85010-2166">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="85010-2166">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="85010-2167">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-2167">Az.Cdn</span></span>
* <span data-ttu-id="85010-2168">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="85010-2168">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2169">Az.Compute</span></span>
* <span data-ttu-id="85010-2170">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="85010-2170">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-2171">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-2171">Az.DataFactory</span></span>
* <span data-ttu-id="85010-2172">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="85010-2172">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="85010-2173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="85010-2173">Az.LogicApp</span></span>
* <span data-ttu-id="85010-2174">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="85010-2174">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2175">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2175">Az.Network</span></span>
* <span data-ttu-id="85010-2176">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="85010-2176">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-2178">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2178">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="85010-2179">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="85010-2179">SDK Update</span></span>
* <span data-ttu-id="85010-2180">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="85010-2180">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="85010-2181">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="85010-2181">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2182">Az.Resources</span></span>
* <span data-ttu-id="85010-2183">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="85010-2183">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="85010-2184">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="85010-2184">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="85010-2185">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="85010-2185">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="85010-2186">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="85010-2186">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="85010-2187">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="85010-2187">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="85010-2188">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="85010-2188">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2189">Az.Sql</span></span>
* <span data-ttu-id="85010-2190">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="85010-2190">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="85010-2191">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="85010-2191">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-2192">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-2192">Az.Storage</span></span>
* <span data-ttu-id="85010-2193">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="85010-2193">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="85010-2194">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2194">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="85010-2195">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="85010-2195">Az.AnalysisServices</span></span>
* <span data-ttu-id="85010-2196">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="85010-2196">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-2197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-2197">Az.Automation</span></span>
* <span data-ttu-id="85010-2198">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-2198">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="85010-2199">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-2199">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="85010-2200">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-2200">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-2201">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-2201">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-2202">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="85010-2202">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2203">Az.Compute</span></span>
* <span data-ttu-id="85010-2204">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="85010-2204">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="85010-2205">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="85010-2205">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="85010-2206">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="85010-2206">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="85010-2207">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="85010-2207">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-2208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2208">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-2209">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="85010-2209">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="85010-2210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="85010-2210">Az.EventHub</span></span>
* <span data-ttu-id="85010-2211">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="85010-2211">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-2212">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-2212">Az.KeyVault</span></span>
* <span data-ttu-id="85010-2213">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="85010-2213">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="85010-2214">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="85010-2214">Az.LogicApp</span></span>
* <span data-ttu-id="85010-2215">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="85010-2215">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="85010-2216">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="85010-2216">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="85010-2217">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="85010-2217">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="85010-2218">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="85010-2218">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="85010-2219">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="85010-2219">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="85010-2220">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="85010-2220">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="85010-2221">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="85010-2221">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="85010-2222">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="85010-2222">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="85010-2223">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="85010-2223">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="85010-2224">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="85010-2224">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="85010-2225">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="85010-2225">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="85010-2226">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85010-2226">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="85010-2227">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="85010-2227">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="85010-2228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-2228">Az.Monitor</span></span>
* <span data-ttu-id="85010-2229">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="85010-2229">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2230">Az.Network</span></span>
* <span data-ttu-id="85010-2231">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="85010-2231">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="85010-2232">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-2232">Az.OperationalInsights</span></span>
* <span data-ttu-id="85010-2233">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="85010-2233">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="85010-2234">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="85010-2234">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="85010-2235">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="85010-2235">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2236">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2236">Az.Resources</span></span>
* <span data-ttu-id="85010-2237">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="85010-2237">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="85010-2238">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="85010-2238">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="85010-2239">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="85010-2239">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="85010-2240">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="85010-2240">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2241">Az.Sql</span></span>
* <span data-ttu-id="85010-2242">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="85010-2242">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="85010-2243">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="85010-2243">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-2244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2244">Az.Websites</span></span>
* <span data-ttu-id="85010-2245">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="85010-2245">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="85010-2246">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2246">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-2247">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2247">Az.Accounts</span></span>
* <span data-ttu-id="85010-2248">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="85010-2248">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="85010-2249">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="85010-2249">Az.AnalysisServices</span></span>
<span data-ttu-id="85010-2250">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="85010-2250">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2251">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2251">Az.Compute</span></span>
* <span data-ttu-id="85010-2252">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="85010-2252">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="85010-2253">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="85010-2253">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="85010-2254">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="85010-2254">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-2255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-2255">Az.RecoveryServices</span></span>
<span data-ttu-id="85010-2256">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="85010-2256">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2257">Az.Resources</span></span>
* <span data-ttu-id="85010-2258">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85010-2258">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="85010-2259">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="85010-2259">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="85010-2260">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="85010-2260">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="85010-2261">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="85010-2261">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2262">Az.Sql</span></span>
* <span data-ttu-id="85010-2263">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="85010-2263">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="85010-2264">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2264">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="85010-2265">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="85010-2265">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="85010-2266">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2266">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-2267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2267">Az.Accounts</span></span>
* <span data-ttu-id="85010-2268">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="85010-2268">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="85010-2269">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="85010-2269">Az.AnalysisServices</span></span>
* <span data-ttu-id="85010-2270">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="85010-2270">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="85010-2271">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-2271">Az.RecoveryServices</span></span>
* <span data-ttu-id="85010-2272">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="85010-2272">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="85010-2273">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2273">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-2274">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2274">Az.Accounts</span></span>
* <span data-ttu-id="85010-2275">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="85010-2275">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="85010-2276">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2276">Update incorrect online help URLs</span></span>
* <span data-ttu-id="85010-2277">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="85010-2277">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="85010-2278">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="85010-2278">Az.Aks</span></span>
* <span data-ttu-id="85010-2279">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2279">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="85010-2280">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-2280">Az.Automation</span></span>
* <span data-ttu-id="85010-2281">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="85010-2281">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="85010-2282">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2282">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="85010-2283">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="85010-2283">Az.Cdn</span></span>
* <span data-ttu-id="85010-2284">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2284">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2285">Az.Compute</span></span>
* <span data-ttu-id="85010-2286">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="85010-2286">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="85010-2287">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="85010-2287">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="85010-2288">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85010-2288">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="85010-2289">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="85010-2289">Az.ContainerRegistry</span></span>
* <span data-ttu-id="85010-2290">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2290">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="85010-2291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85010-2291">Az.DataFactory</span></span>
* <span data-ttu-id="85010-2292">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="85010-2292">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-2293">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2293">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-2294">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="85010-2294">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="85010-2295">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="85010-2295">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="85010-2296">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2296">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-2297">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-2297">Az.IotHub</span></span>
* <span data-ttu-id="85010-2298">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="85010-2298">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="85010-2299">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-2299">Az.KeyVault</span></span>
* <span data-ttu-id="85010-2300">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2300">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2301">Az.Network</span></span>
* <span data-ttu-id="85010-2302">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2302">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2303">Az.Resources</span></span>
* <span data-ttu-id="85010-2304">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="85010-2304">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="85010-2305">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85010-2305">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="85010-2306">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="85010-2306">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="85010-2307">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="85010-2307">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="85010-2308">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="85010-2308">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="85010-2309">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-2309">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="85010-2310">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="85010-2310">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-2311">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-2311">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-2312">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="85010-2312">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="85010-2313">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="85010-2313">Fix some error messages.</span></span>
* <span data-ttu-id="85010-2314">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="85010-2314">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="85010-2315">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="85010-2315">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="85010-2316">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="85010-2316">Az.SignalR</span></span>
* <span data-ttu-id="85010-2317">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2317">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2318">Az.Sql</span></span>
* <span data-ttu-id="85010-2319">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2319">Update incorrect online help URLs</span></span>
* <span data-ttu-id="85010-2320">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="85010-2320">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="85010-2321">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="85010-2321">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="85010-2322">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="85010-2322">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-2323">Az.Storage</span></span>
* <span data-ttu-id="85010-2324">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2324">Update incorrect online help URLs</span></span>
* <span data-ttu-id="85010-2325">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="85010-2325">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="85010-2326">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="85010-2326">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="85010-2327">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="85010-2327">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="85010-2328">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="85010-2328">Az.TrafficManager</span></span>
* <span data-ttu-id="85010-2329">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2329">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2330">Az.Websites</span></span>
* <span data-ttu-id="85010-2331">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2331">Update incorrect online help URLs</span></span>
* <span data-ttu-id="85010-2332">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="85010-2332">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="85010-2333">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="85010-2333">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="85010-2334">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2334">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="85010-2335">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2335">Az.Accounts</span></span>
* <span data-ttu-id="85010-2336">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="85010-2336">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2337">Az.Compute</span></span>
* <span data-ttu-id="85010-2338">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="85010-2338">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="85010-2339">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="85010-2339">Updated the description of ID in help files</span></span>
* <span data-ttu-id="85010-2340">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="85010-2340">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-2341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2341">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-2342">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="85010-2342">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="85010-2343">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="85010-2343">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="85010-2344">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="85010-2344">Az.EventGrid</span></span>
* <span data-ttu-id="85010-2345">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="85010-2345">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="85010-2346">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="85010-2346">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="85010-2347">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="85010-2347">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="85010-2348">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="85010-2348">Event Time-To-Live,</span></span>
        - <span data-ttu-id="85010-2349">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="85010-2349">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="85010-2350">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="85010-2350">Dead letter endpoint.</span></span>
    - <span data-ttu-id="85010-2351">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="85010-2351">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="85010-2352">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="85010-2352">Event Time-To-Live,</span></span>
        - <span data-ttu-id="85010-2353">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="85010-2353">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="85010-2354">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="85010-2354">Dead letter endpoint.</span></span>
* <span data-ttu-id="85010-2355">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="85010-2355">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="85010-2356">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="85010-2356">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="85010-2357">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="85010-2357">Az.IotHub</span></span>
* <span data-ttu-id="85010-2358">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="85010-2358">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="85010-2359">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="85010-2359">Az.LogicApp</span></span>
* <span data-ttu-id="85010-2360">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="85010-2360">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2361">Az.Resources</span></span>
* <span data-ttu-id="85010-2362">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="85010-2362">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="85010-2363">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="85010-2363">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="85010-2364">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="85010-2364">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="85010-2365">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="85010-2365">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="85010-2366">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="85010-2366">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="85010-2367">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="85010-2367">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="85010-2368">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="85010-2368">Az.SignalR</span></span>
* <span data-ttu-id="85010-2369">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="85010-2369">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2370">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2370">Az.Sql</span></span>
* <span data-ttu-id="85010-2371">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="85010-2371">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="85010-2372">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-2372">Az.Storage</span></span>
* <span data-ttu-id="85010-2373">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="85010-2373">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="85010-2374">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="85010-2374">New-AzStorageContext</span></span>
* <span data-ttu-id="85010-2375">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="85010-2375">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="85010-2376">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="85010-2376">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-2377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2377">Az.Websites</span></span>
* <span data-ttu-id="85010-2378">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="85010-2378">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="85010-2379">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="85010-2379">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="85010-2380">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2380">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="85010-2381">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-2381">General</span></span>

- <span data-ttu-id="85010-2382">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="85010-2382">General Availability of Az Module</span></span>
- <span data-ttu-id="85010-2383">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="85010-2383">Online help for each module</span></span>
- <span data-ttu-id="85010-2384">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="85010-2384">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="85010-2385">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2385">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="85010-2386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85010-2386">Az.Accounts</span></span>
- <span data-ttu-id="85010-2387">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="85010-2387">Changed from Az.Profile</span></span>
- <span data-ttu-id="85010-2388">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="85010-2388">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="85010-2389">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-2389">Az.ApiManagement</span></span>
- <span data-ttu-id="85010-2390">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="85010-2390">Fixes for #7002</span></span>
- <span data-ttu-id="85010-2391">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="85010-2392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="85010-2392">Az.Batch</span></span>
- <span data-ttu-id="85010-2393">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="85010-2393">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="85010-2394">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="85010-2394">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="85010-2395">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2395">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="85010-2396">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="85010-2396">Az.Billing</span></span>
- <span data-ttu-id="85010-2397">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="85010-2397">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="85010-2398">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="85010-2398">Az.CognitivServices</span></span>
- <span data-ttu-id="85010-2399">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="85010-2399">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="85010-2400">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="85010-2400">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="85010-2401">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="85010-2401">Az.ContainerInstance</span></span>
- <span data-ttu-id="85010-2402">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="85010-2402">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="85010-2403">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="85010-2403">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="85010-2404">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2404">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="85010-2405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2405">Az.DataLakeStore</span></span>
- <span data-ttu-id="85010-2406">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2406">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="85010-2407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85010-2407">Az.Monitor</span></span>
- <span data-ttu-id="85010-2408">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2408">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="85010-2409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="85010-2409">Az.KeyVault</span></span>
- <span data-ttu-id="85010-2410">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="85010-2410">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="85010-2411">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="85010-2411">Az.MachineLearning</span></span>
- <span data-ttu-id="85010-2412">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="85010-2412">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="85010-2413">Az.Media</span><span class="sxs-lookup"><span data-stu-id="85010-2413">Az.Media</span></span>
- <span data-ttu-id="85010-2414">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="85010-2414">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="85010-2415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2415">Az.Network</span></span>
<span data-ttu-id="85010-2416">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="85010-2416">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="85010-2417">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-2417">New cmdlets added:</span></span>
        - <span data-ttu-id="85010-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85010-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="85010-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85010-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="85010-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85010-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="85010-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85010-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="85010-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85010-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="85010-2423">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="85010-2423">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="85010-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="85010-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="85010-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="85010-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="85010-2426">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85010-2426">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="85010-2427">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85010-2427">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="85010-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85010-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="85010-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85010-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="85010-2430">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="85010-2430">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="85010-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="85010-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="85010-2432">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="85010-2432">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="85010-2433">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="85010-2433">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="85010-2434">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="85010-2434">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="85010-2435">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="85010-2435">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="85010-2436">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="85010-2436">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="85010-2437">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="85010-2437">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="85010-2438">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2438">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="85010-2439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="85010-2439">Az.OperationalInsights</span></span>
- <span data-ttu-id="85010-2440">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="85010-2441">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="85010-2441">Az.Profile</span></span>
- <span data-ttu-id="85010-2442">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="85010-2442">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="85010-2443">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-2443">Az.RecoveryServices</span></span>
- <span data-ttu-id="85010-2444">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="85010-2445">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2445">Az.Resources</span></span>
- <span data-ttu-id="85010-2446">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2446">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="85010-2447">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-2447">Az.ServiceFabric</span></span>
- <span data-ttu-id="85010-2448">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="85010-2448">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="85010-2449">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2449">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="85010-2450">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="85010-2450">Az.SIgnalR</span></span>
- <span data-ttu-id="85010-2451">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="85010-2451">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="85010-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2452">Az.Sql</span></span>
- <span data-ttu-id="85010-2453">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="85010-2453">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="85010-2454">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2454">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="85010-2455">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2455">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="85010-2456">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-2456">Az.Storage</span></span>
- <span data-ttu-id="85010-2457">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2457">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="85010-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2458">Az.Websites</span></span>
- <span data-ttu-id="85010-2459">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="85010-2459">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="85010-2460">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2460">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="85010-2461">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-2461">General</span></span>

* <span data-ttu-id="85010-2462">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="85010-2462">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="85010-2463">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2463">Az.Compute</span></span>

* <span data-ttu-id="85010-2464">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="85010-2464">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="85010-2465">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2465">Az.DataLakeStore</span></span>

* <span data-ttu-id="85010-2466">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="85010-2466">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="85010-2467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="85010-2467">Az.FrontDoor</span></span>

* <span data-ttu-id="85010-2468">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="85010-2468">Fixed some broken links</span></span>
    - <span data-ttu-id="85010-2469">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="85010-2469">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="85010-2470">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="85010-2470">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="85010-2471">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85010-2471">Az.RecoveryServices</span></span>

* <span data-ttu-id="85010-2472">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2472">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="85010-2473">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="85010-2473">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="85010-2474">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2474">Az.Resources</span></span>

* <span data-ttu-id="85010-2475">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="85010-2475">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="85010-2476">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="85010-2476">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="85010-2477">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2477">Az.Sql</span></span>

* <span data-ttu-id="85010-2478">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="85010-2478">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="85010-2479">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="85010-2479">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="85010-2480">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="85010-2480">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="85010-2481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85010-2481">Az.Storage</span></span>

* <span data-ttu-id="85010-2482">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85010-2482">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="85010-2483">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="85010-2483">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="85010-2484">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="85010-2484">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="85010-2485">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="85010-2485">Support Static Website configuration</span></span>
    - <span data-ttu-id="85010-2486">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="85010-2486">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="85010-2487">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="85010-2487">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="85010-2488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2488">Az.Websites</span></span>

* <span data-ttu-id="85010-2489">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="85010-2489">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="85010-2490">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="85010-2490">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="85010-2491">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2491">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="85010-2492">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2492">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="85010-2493">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="85010-2493">Az.ApiManagement</span></span>
* <span data-ttu-id="85010-2494">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="85010-2494">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="85010-2495">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="85010-2495">Az.Automation</span></span>
* <span data-ttu-id="85010-2496">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="85010-2496">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="85010-2497">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="85010-2497">Added Update Management cmdlets</span></span>
* <span data-ttu-id="85010-2498">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="85010-2498">Added Source Control cmdlets</span></span>
* <span data-ttu-id="85010-2499">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="85010-2499">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="85010-2500">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="85010-2500">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="85010-2501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2501">Az.Compute</span></span>
* <span data-ttu-id="85010-2502">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="85010-2502">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="85010-2503">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="85010-2503">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="85010-2504">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="85010-2504">Az.ContainerInstance</span></span>
* <span data-ttu-id="85010-2505">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="85010-2505">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="85010-2506">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="85010-2506">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="85010-2507">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="85010-2507">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="85010-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2508">Az.Network</span></span>
* <span data-ttu-id="85010-2509">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="85010-2509">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="85010-2510">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2510">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="85010-2511">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="85010-2511">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="85010-2512">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85010-2512">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="85010-2513">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="85010-2513">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="85010-2514">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="85010-2514">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="85010-2515">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="85010-2515">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="85010-2516">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="85010-2516">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="85010-2517">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="85010-2517">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="85010-2518">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="85010-2518">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="85010-2519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="85010-2519">Az.Relay</span></span>
* <span data-ttu-id="85010-2520">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="85010-2520">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="85010-2521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2521">Az.Resources</span></span>
* <span data-ttu-id="85010-2522">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="85010-2522">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="85010-2523">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="85010-2523">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="85010-2524">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="85010-2524">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="85010-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-2526">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="85010-2526">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="85010-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2527">Az.Sql</span></span>
* <span data-ttu-id="85010-2528">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2528">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="85010-2529">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="85010-2529">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="85010-2530">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="85010-2530">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="85010-2531">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="85010-2531">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="85010-2532">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="85010-2532">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="85010-2533">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="85010-2533">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="85010-2534">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="85010-2534">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="85010-2535">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="85010-2535">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="85010-2536">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="85010-2536">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="85010-2537">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="85010-2537">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="85010-2538">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="85010-2538">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="85010-2539">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="85010-2539">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="85010-2540">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="85010-2540">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="85010-2541">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="85010-2541">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="85010-2542">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="85010-2542">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="85010-2543">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="85010-2543">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="85010-2544">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="85010-2544">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="85010-2545">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2545">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="85010-2546">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="85010-2546">General</span></span>
* <span data-ttu-id="85010-2547">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="85010-2547">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="85010-2548">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="85010-2548">Az.Profile</span></span>
* <span data-ttu-id="85010-2549">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="85010-2549">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="85010-2550">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="85010-2550">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="85010-2551">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="85010-2551">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="85010-2552">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="85010-2552">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="85010-2553">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="85010-2553">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="85010-2554">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="85010-2554">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="85010-2555">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="85010-2555">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-2556">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-2556">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-2557">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="85010-2557">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2558">Az.Compute</span></span>
* <span data-ttu-id="85010-2559">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="85010-2559">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="85010-2560">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="85010-2560">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="85010-2561">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="85010-2561">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2562">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-2563">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="85010-2563">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="85010-2564">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="85010-2564">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="85010-2565">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="85010-2565">Az.Insights</span></span>
* <span data-ttu-id="85010-2566">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="85010-2566">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="85010-2567">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="85010-2567">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="85010-2568">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="85010-2568">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="85010-2569">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="85010-2569">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2570">Az.Network</span></span>
* <span data-ttu-id="85010-2571">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="85010-2571">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="85010-2572">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-2572">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="85010-2573">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="85010-2573">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="85010-2574">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="85010-2574">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="85010-2575">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="85010-2575">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="85010-2576">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="85010-2576">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="85010-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="85010-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="85010-2578">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="85010-2578">Az.PolicyInsights</span></span>
* <span data-ttu-id="85010-2579">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="85010-2579">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2580">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2580">Az.Resources</span></span>
* <span data-ttu-id="85010-2581">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="85010-2581">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="85010-2582">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="85010-2582">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="85010-2583">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="85010-2583">Az.ServiceBus</span></span>
* <span data-ttu-id="85010-2584">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="85010-2584">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="85010-2585">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="85010-2585">Az.ServiceFabric</span></span>
* <span data-ttu-id="85010-2586">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="85010-2586">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="85010-2587">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="85010-2587">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="85010-2588">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="85010-2588">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="85010-2589">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="85010-2589">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="85010-2590">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="85010-2590">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="85010-2591">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2591">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="85010-2592">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="85010-2592">Az.Profile</span></span>
* <span data-ttu-id="85010-2593">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="85010-2593">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="85010-2594">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="85010-2594">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2595">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2595">Az.Compute</span></span>
* <span data-ttu-id="85010-2596">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="85010-2596">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="85010-2597">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="85010-2597">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="85010-2598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="85010-2598">Az.DataLakeStore</span></span>
* <span data-ttu-id="85010-2599">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="85010-2599">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="85010-2600">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="85010-2600">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="85010-2601">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="85010-2601">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="85010-2602">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="85010-2602">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="85010-2603">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="85010-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2604">Az.Network</span></span>
* <span data-ttu-id="85010-2605">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="85010-2605">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="85010-2606">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="85010-2606">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2607">Az.Resources</span></span>
* <span data-ttu-id="85010-2608">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="85010-2608">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="85010-2609">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="85010-2609">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="85010-2610">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2610">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="85010-2611">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="85010-2611">Azure.Storage</span></span>
* <span data-ttu-id="85010-2612">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="85010-2612">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="85010-2613">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="85010-2613">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="85010-2614">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="85010-2614">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="85010-2615">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="85010-2615">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="85010-2616">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="85010-2616">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="85010-2617">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="85010-2617">Az.CognitiveServices</span></span>
* <span data-ttu-id="85010-2618">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="85010-2618">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="85010-2619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="85010-2619">Az.Compute</span></span>
* <span data-ttu-id="85010-2620">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="85010-2620">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="85010-2621">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="85010-2621">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="85010-2622">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2622">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="85010-2623">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="85010-2623">Az.DataFactoryV2</span></span>
* <span data-ttu-id="85010-2624">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="85010-2624">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="85010-2625">Az.Network</span><span class="sxs-lookup"><span data-stu-id="85010-2625">Az.Network</span></span>
* <span data-ttu-id="85010-2626">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="85010-2626">Added NetworkProfile functionality.</span></span> <span data-ttu-id="85010-2627">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="85010-2627">new cmdlets added</span></span>
    - <span data-ttu-id="85010-2628">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="85010-2628">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="85010-2629">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="85010-2629">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="85010-2630">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="85010-2630">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="85010-2631">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="85010-2631">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="85010-2632">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="85010-2632">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="85010-2633">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="85010-2633">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="85010-2634">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="85010-2634">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="85010-2635">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="85010-2635">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="85010-2636">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="85010-2636">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="85010-2637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="85010-2637">Az.RedisCache</span></span>
* <span data-ttu-id="85010-2638">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="85010-2638">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="85010-2639">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="85010-2639">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="85010-2640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85010-2640">Az.Resources</span></span>
* <span data-ttu-id="85010-2641">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="85010-2641">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="85010-2642">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="85010-2642">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="85010-2643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="85010-2643">Az.Sql</span></span>
* <span data-ttu-id="85010-2644">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="85010-2644">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="85010-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="85010-2645">Az.Websites</span></span>
* <span data-ttu-id="85010-2646">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="85010-2646">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="85010-2647">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="85010-2647">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="85010-2648">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="85010-2648">0.2.0 - September 2018</span></span>
 <span data-ttu-id="85010-2649">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="85010-2649">Initial Release</span></span>
