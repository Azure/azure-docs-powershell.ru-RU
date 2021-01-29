---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5310923995ad8c950183a1fbf97c01530cac734c
ms.sourcegitcommit: 8f997856c29db6b969893d5c570215d9ab2f2bfb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98685860"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="2d993-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d993-103">Azure PowerShell release notes</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="2d993-104">5.4.0 — январь 2021 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-104">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-105">Az.Accounts</span></span>
* <span data-ttu-id="2d993-106">Отображение правильного идентификатора запроса клиента в сообщении отладки [№ 13745].</span><span class="sxs-lookup"><span data-stu-id="2d993-106">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="2d993-107">Добавлен общий тип исключений Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2d993-107">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="2d993-108">Поддерживаемый API хранилища 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-108">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-109">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-109">Az.Automation</span></span>
* <span data-ttu-id="2d993-110">Исправлена проблема, из-за которой описание не было заполнено для расписаний управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="2d993-110">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="2d993-111">Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2d993-111">Az.CosmosDB</span></span>
* <span data-ttu-id="2d993-112">Выпущена общедоступная версия модуля Az.CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2d993-112">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="2d993-113">Ограничено действие командлета New-AzCosmosDBAccount, чтобы выполнять вызовы обновления к существующим учетным записям базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-113">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="2d993-114">Реализация AnalyticalStorageTTL в SqlContainer.</span><span class="sxs-lookup"><span data-stu-id="2d993-114">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-115">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-115">Az.IotHub</span></span>
* <span data-ttu-id="2d993-116">Исправлена регрессия, связанная с созданием маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="2d993-116">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-117">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-117">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-118">Исправлена проблема в модуле управления секретами.</span><span class="sxs-lookup"><span data-stu-id="2d993-118">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d993-119">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d993-119">Az.LogicApp</span></span>
* <span data-ttu-id="2d993-120">Исправлена проблема, из-за которой Get-AzLogicAppTriggerHistory и Get-AzLogicAppRunAction получали только первую страницу результатов [№ 9141].</span><span class="sxs-lookup"><span data-stu-id="2d993-120">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-121">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-121">Az.Monitor</span></span>
* <span data-ttu-id="2d993-122">Добавлены командлеты для правил сбора данных:</span><span class="sxs-lookup"><span data-stu-id="2d993-122">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="2d993-123">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="2d993-123">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="2d993-124">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="2d993-124">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="2d993-125">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="2d993-125">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="2d993-126">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="2d993-126">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="2d993-127">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="2d993-127">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="2d993-128">Добавлены командлеты для связей правил сбора данных:</span><span class="sxs-lookup"><span data-stu-id="2d993-128">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="2d993-129">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="2d993-129">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="2d993-130">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="2d993-130">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="2d993-131">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="2d993-131">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-132">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-132">Az.Network</span></span>
* <span data-ttu-id="2d993-133">Добавлены новые командлеты для CRUD VpnGatewayNATRule:</span><span class="sxs-lookup"><span data-stu-id="2d993-133">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="2d993-134">New-AzVpnGatewayNatRule;</span><span class="sxs-lookup"><span data-stu-id="2d993-134">'New-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="2d993-135">Update-AzVpnGatewayNatRule;</span><span class="sxs-lookup"><span data-stu-id="2d993-135">'Update-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="2d993-136">Get-AzVpnGatewayNatRule;</span><span class="sxs-lookup"><span data-stu-id="2d993-136">'Get-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="2d993-137">Remove-AzVpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="2d993-137">'Remove-AzVpnGatewayNatRule'</span></span>  
* <span data-ttu-id="2d993-138">Обновлены командлеты, чтобы задать правило NATRule для ресурса VpnGateway и связать его с ресурсом VpnSiteLinkConnection:</span><span class="sxs-lookup"><span data-stu-id="2d993-138">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="2d993-139">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-139">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="2d993-140">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-140">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="2d993-141">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-141">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="2d993-142">Обновлены командлеты для включения ConnectionMode в подключениях шлюзов виртуальных сетей:</span><span class="sxs-lookup"><span data-stu-id="2d993-142">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="2d993-143">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-143">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="2d993-144">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-144">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="2d993-145">Обновлен командлет New-AzFirewallPolicyApplicationRule:</span><span class="sxs-lookup"><span data-stu-id="2d993-145">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="2d993-146">добавлен параметр TargetUrl;</span><span class="sxs-lookup"><span data-stu-id="2d993-146">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="2d993-147">добавлен параметр TerminateTLS.</span><span class="sxs-lookup"><span data-stu-id="2d993-147">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="2d993-148">Добавлены новые командлеты для расширенных функций Брандмауэра Azure:</span><span class="sxs-lookup"><span data-stu-id="2d993-148">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="2d993-149">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="2d993-149">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="2d993-150">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="2d993-150">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="2d993-151">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="2d993-151">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="2d993-152">Обновлен командлет New-AzFirewallPolicy:</span><span class="sxs-lookup"><span data-stu-id="2d993-152">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="2d993-153">добавлен параметр -SkuTier;</span><span class="sxs-lookup"><span data-stu-id="2d993-153">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="2d993-154">добавлен параметр -Identity;</span><span class="sxs-lookup"><span data-stu-id="2d993-154">Added parameter -Identity</span></span>
    - <span data-ttu-id="2d993-155">добавлен параметр -UserAssignedIdentityId;</span><span class="sxs-lookup"><span data-stu-id="2d993-155">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="2d993-156">добавлен параметр -IntrusionDetection;</span><span class="sxs-lookup"><span data-stu-id="2d993-156">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="2d993-157">добавлен параметр -TransportSecurityName;</span><span class="sxs-lookup"><span data-stu-id="2d993-157">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="2d993-158">добавлен параметр -TransportSecurityKeyVaultSecretId.</span><span class="sxs-lookup"><span data-stu-id="2d993-158">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="2d993-159">Добавлен новый командлет для сбора данных о сопоставлениях безопасности IKE для подключений шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="2d993-159">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="2d993-160">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="2d993-160">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="2d993-161">Добавлена поддержка множественной проверки подлинности для p2sVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-161">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="2d993-162">Обновлены командлеты New-AzVpnServerConfiguration и Update-AzVpnServerConfiguration, разрешающие настройку нескольких параметров проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2d993-162">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="2d993-163">Обновлены командлеты New-AzVpnGateway и New-AzP2sVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="2d993-163">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="2d993-164">добавлен параметр EnableRoutingPreferenceInternetFlag.</span><span class="sxs-lookup"><span data-stu-id="2d993-164">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-166">Добавлена функция восстановления между регионами.</span><span class="sxs-lookup"><span data-stu-id="2d993-166">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="2d993-167">Заблокировано получение конфигурации рабочей нагрузки, когда целевой элемент является группой доступности.</span><span class="sxs-lookup"><span data-stu-id="2d993-167">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-168">Az.Resources</span></span>
* <span data-ttu-id="2d993-169">Включена поддержка параметра -QueryString в командлетах New-Az\*Deployments.</span><span class="sxs-lookup"><span data-stu-id="2d993-169">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-170">Az.Sql</span></span>
* <span data-ttu-id="2d993-171">Командлет Start-AzSqlInstanceDatabaseLogReplay сделан синхронным и добавлен флаг -AsJob.</span><span class="sxs-lookup"><span data-stu-id="2d993-171">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-172">Az.Storage</span></span>
* <span data-ttu-id="2d993-173">Исправлена проблема, из-за которой ContinuationToken никогда не имеет значение NULL при использовании большого двоичного объекта списка с параметром -IncludeVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-173">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="2d993-174">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2d993-174">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-175">Az.Websites</span></span>
* <span data-ttu-id="2d993-176">Включена поддержка управляемых сертификатов Службы приложений:</span><span class="sxs-lookup"><span data-stu-id="2d993-176">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="2d993-177">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-177">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="2d993-178">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-178">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="2d993-179">Исправлена проблема, из-за которой пароль Docker удалялся из appsettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="2d993-179">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d993-180">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="2d993-180">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d993-181">Иван Акчеуров (Ivan Akcheurov) (@ivanakcheurov), обновление Set-AzSecurityWorkspaceSetting.md (№ 13877).</span><span class="sxs-lookup"><span data-stu-id="2d993-181">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="2d993-182">@javiermarasco, пример обновления (№ 13837).</span><span class="sxs-lookup"><span data-stu-id="2d993-182">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="2d993-183">@jhaprakash26, обновление Set-AzVirtualNetwork.md (№ 13857).</span><span class="sxs-lookup"><span data-stu-id="2d993-183">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="2d993-184">Майкл Холмс (Michael Holmes) (@MichaelHolmesWP), обновление New-AzStorageTableStoredAccessPolicy.md (№ 13871).</span><span class="sxs-lookup"><span data-stu-id="2d993-184">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="2d993-185">Майкл Джеймс (Michael James) (@mikejwhat), настройка Get-AzLogicAppTriggerHistory и Get-AzLogicAppRunAction на возвращение более 30 результатов (№ 13846).</span><span class="sxs-lookup"><span data-stu-id="2d993-185">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="2d993-186">@Willem-J-an, исправление проблемы, из-за которой пароль Docker удалялся из appsettings в Set-AzWebApp(Slot) (№ 13866).</span><span class="sxs-lookup"><span data-stu-id="2d993-186">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="2d993-187">5.3.0 — декабрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-187">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-188">Az.Accounts</span></span>
* <span data-ttu-id="2d993-189">Исправлена проблема, из-за которой прокси-сервер HTTP не учитывался в Windows PowerShell [№ 13647].</span><span class="sxs-lookup"><span data-stu-id="2d993-189">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="2d993-190">Улучшен журнал отладки для длительных операций в созданных модулях.</span><span class="sxs-lookup"><span data-stu-id="2d993-190">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-191">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-191">Az.Automation</span></span>
* <span data-ttu-id="2d993-192">Исправлена проблема, из-за которой упакованную строку PSObject не удавалось преобразовать в строку JSON с помощью параметров Start-AzAutomationRunbook [№ 13240].</span><span class="sxs-lookup"><span data-stu-id="2d993-192">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="2d993-193">Исправлено средство заполнения расположения для командлета New-AzAutomationUpdateManagementAzureQuery.</span><span class="sxs-lookup"><span data-stu-id="2d993-193">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-194">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-194">Az.Compute</span></span>
* <span data-ttu-id="2d993-195">В командлеты Get-AzVMDscExtensionStatus и Get-AzVMDscExtension добавлен новый параметр VM в новом наборе параметров VMParameterSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-195">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="2d993-196">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="2d993-196">Az.Databricks</span></span>
* <span data-ttu-id="2d993-197">Исправлена проблема, из-за которой иногда возвращался результат New-AzDatabricksVNetPeering перед полной подготовкой (https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="2d993-197">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-198">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-199">Исправлена команда Invoke-AzDataFactoryV2Pipeline для устранения проблемы с SupportsShouldProcess.</span><span class="sxs-lookup"><span data-stu-id="2d993-199">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="2d993-200">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="2d993-200">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="2d993-201">В пул узлов добавлено свойство StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="2d993-201">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-202">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-203">В класс AzureHDInsightHostInfo добавлены свойства Fqdn и EffectiveDiskEncryptionKeyUrl.</span><span class="sxs-lookup"><span data-stu-id="2d993-203">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-204">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-204">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-205">В Get-AzKeyVaultSecret добавлен новый параметр -AsPlainText для прямого возврата секрета в виде обычного текста [№ 13630].</span><span class="sxs-lookup"><span data-stu-id="2d993-205">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="2d993-206">Поддерживается выборочное восстановление ключа из управляемой полной резервной копии HSM [№ 13526].</span><span class="sxs-lookup"><span data-stu-id="2d993-206">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="2d993-207">Устранены некоторые незначительные проблемы [№ 13583] [№ 13584].</span><span class="sxs-lookup"><span data-stu-id="2d993-207">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="2d993-208">В модуль SecretManagement добавлены отсутствующие возвращаемые объекты Get-Secret.</span><span class="sxs-lookup"><span data-stu-id="2d993-208">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="2d993-209">Исправлена проблема, из-за которой хранилище иногда создавалось без политики доступа по умолчанию [№ 13687].</span><span class="sxs-lookup"><span data-stu-id="2d993-209">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="2d993-210">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="2d993-210">Az.Kusto</span></span>
* <span data-ttu-id="2d993-211">Версия API обновлена до 2020-09-18.</span><span class="sxs-lookup"><span data-stu-id="2d993-211">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-212">Az.Network</span></span>
* <span data-ttu-id="2d993-213">Исправлена проблема с удалением пиринга и командлетом подключения для сценария ExpressRouteCircuit:</span><span class="sxs-lookup"><span data-stu-id="2d993-213">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="2d993-214">Remove-AzExpressRouteCircuitPeeringConfig и Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-214">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-215">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-215">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-216">Добавлена поддержка возврата страничных результатов для Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2d993-216">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-217">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-217">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-218">Включена функция обратимого удаления для SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-218">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="2d993-219">Исправлена проблема с восстановлением групп доступности AG и удалена проверка имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="2d993-219">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="2d993-220">Изменен формат имени контейнера для элемента резервного копирования Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-220">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="2d993-221">Добавлена поддержка функции CMK для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d993-221">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-222">Az.Resources</span></span>
* <span data-ttu-id="2d993-223">Устранена проблема с исключением NullRef в New-AzureManagedApplication и Set-AzureManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="2d993-223">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="2d993-224">Обновлен пакет SDK Azure Resource Manager для использования последней общедоступной версии API DeploymentScripts: 2020-10-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-224">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-225">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-225">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-226">Внесены исправления в Add-AzServiceFabricNodeType.</span><span class="sxs-lookup"><span data-stu-id="2d993-226">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="2d993-227">Добавлен тип узла, который можно использовать для кластера Service Fabric перед созданием масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2d993-227">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-228">Az.Sql</span></span>
* <span data-ttu-id="2d993-229">Исправлено описание параметра для команды InstanceFailoverGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-229">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="2d993-230">Обновлена логика, согласно которой данные типа schemaName, tableName и columnName извлекались из идентификатора команд классификации данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-230">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="2d993-231">Исправлены поля Status и StatusMessage в Get-AzSqlDatabaseImportExportStatus, чтобы обеспечить соответствие документации.</span><span class="sxs-lookup"><span data-stu-id="2d993-231">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="2d993-232">Добавлены командлеты аудита для операций поддержки Майкрософт (DevOps): Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit.</span><span class="sxs-lookup"><span data-stu-id="2d993-232">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-233">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-233">Az.Storage</span></span>
* <span data-ttu-id="2d993-234">Поддерживаемые операции создания, обновления, получения и перечисления EncryptionScope учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="2d993-234">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="2d993-235">New-AzStorageEncryptionScope;</span><span class="sxs-lookup"><span data-stu-id="2d993-235">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="2d993-236">Update-AzStorageEncryptionScope;</span><span class="sxs-lookup"><span data-stu-id="2d993-236">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="2d993-237">Get-AzStorageEncryptionScope.</span><span class="sxs-lookup"><span data-stu-id="2d993-237">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="2d993-238">Поддерживаемые операции создания контейнера и отправки большого двоичного объекта с параметром области шифрования:</span><span class="sxs-lookup"><span data-stu-id="2d993-238">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="2d993-239">New-AzRmStorageContainer;</span><span class="sxs-lookup"><span data-stu-id="2d993-239">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="2d993-240">New-AzStorageContainer;</span><span class="sxs-lookup"><span data-stu-id="2d993-240">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="2d993-241">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-241">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d993-242">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="2d993-242">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d993-243">Андреас Уолтер (Andreas Wolter) (@AndreasWolter), удален маркетинговый стиль, улучшен пример фильтра (№ 13671).</span><span class="sxs-lookup"><span data-stu-id="2d993-243">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="2d993-244">Тиджани Белмансаур (Tidjani Belmansour) (@BelRarr), обновлен файл Get-AzBillingInvoice.md (№ 13634).</span><span class="sxs-lookup"><span data-stu-id="2d993-244">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="2d993-245">Дэвид Клемпфнер (David Klempfner) (@DavidKlempfner):</span><span class="sxs-lookup"><span data-stu-id="2d993-245">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="2d993-246">исправлена орфографическая ошибка (№ 13677);</span><span class="sxs-lookup"><span data-stu-id="2d993-246">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="2d993-247">обновлен файл PSMetricNoDetails.cs (№ 13676).</span><span class="sxs-lookup"><span data-stu-id="2d993-247">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="2d993-248">@kilobyte97, исправлена ошибка командлета для удаления конфигурации (№ 13655).</span><span class="sxs-lookup"><span data-stu-id="2d993-248">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="2d993-249">@kongou-ae, обновлен файл Set-AzFirewall.md (№ 13727).</span><span class="sxs-lookup"><span data-stu-id="2d993-249">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="2d993-250">@MasterKuat, исправлено переключение между заголовком и кодом в документации (№ 13666).</span><span class="sxs-lookup"><span data-stu-id="2d993-250">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="2d993-251">NickT (@nukeulis), обновлен файл Set-AzContext.md (№ 13702).</span><span class="sxs-lookup"><span data-stu-id="2d993-251">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="2d993-252">@PaulHCode, обновлен файл Start-AzJitNetworkAccessPolicy.md: исправлен пример для отображения правильного демонстрируемого командлета (№ 13713).</span><span class="sxs-lookup"><span data-stu-id="2d993-252">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="2d993-253">Райан Борстельманн (Ryan Borstelmann) (@ryanborMSFT), удален идентификатор подписки (№ 13715).</span><span class="sxs-lookup"><span data-stu-id="2d993-253">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="2d993-254">Шашикант Шакья (Shashikant Shakya) (@shshakya), обновлен файл Set-AzSqlDatabase.md (№ 13674).</span><span class="sxs-lookup"><span data-stu-id="2d993-254">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="2d993-255">Себастиан Олсен (Sebastian Olsen) (@Spacebjorn),обновлен файл Get-AzRecoveryServicesBackupItem.md (№ 13719).</span><span class="sxs-lookup"><span data-stu-id="2d993-255">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="2d993-256">5.2.0 — декабрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-256">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-257">Az.Accounts</span></span>
* <span data-ttu-id="2d993-258">Теперь выполняется анализ времени ExpiresOn из необработанного токена, если не удается получить эти данные из базовой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="2d993-258">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="2d993-259">Улучшено сообщение с предупреждением, если недоступна интерактивная аутентификация.</span><span class="sxs-lookup"><span data-stu-id="2d993-259">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-260">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-261">[Критическое изменение] New-AzApiManagementProduct по умолчанию не имеет ограничения на подписку.</span><span class="sxs-lookup"><span data-stu-id="2d993-261">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-262">Az.Compute</span></span>
* <span data-ttu-id="2d993-263">Изменен командлет Get-AzVm для фильтрации по параметру -Name до проверки регулирования вследствие большого числа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-263">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="2d993-264">Добавлен новый командлет Start-AzVmssRollingExtensionUpgrade.</span><span class="sxs-lookup"><span data-stu-id="2d993-264">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d993-265">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d993-265">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d993-266">Реализована поддержка параметра Name для Get-AzContainerRegistryUsage и значение из входных данных конвейера для этого командлета. [13605]</span><span class="sxs-lookup"><span data-stu-id="2d993-266">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="2d993-267">Улучшены исключения для Connect-AzContainerRegistry.</span><span class="sxs-lookup"><span data-stu-id="2d993-267">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-268">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-269">Пакет SDK ADF для .NET обновлен до версии 4.13.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-269">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d993-270">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d993-270">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d993-271">Добавлена поддержка ключей, управляемых клиентом.</span><span class="sxs-lookup"><span data-stu-id="2d993-271">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-272">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-272">Az.IotHub</span></span>
* <span data-ttu-id="2d993-273">Исправлена ошибка маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="2d993-273">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-274">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-274">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-275">Добавлена поддержка all в качестве параметра при настройке политик доступа для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="2d993-275">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="2d993-276">Реализована поддержка новой версии модуля SecretManagement [13366].</span><span class="sxs-lookup"><span data-stu-id="2d993-276">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="2d993-277">Реализована поддержка ByteArray, String, PSCredential и Hashtable для SecretValue в SecretManagementModule [12190].</span><span class="sxs-lookup"><span data-stu-id="2d993-277">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="2d993-278">[Критическое изменение] Перепроектирована контактная зона API командлетов, связанных с управляемым устройством HSM.</span><span class="sxs-lookup"><span data-stu-id="2d993-278">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-279">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-279">Az.Monitor</span></span>
* <span data-ttu-id="2d993-280">Изменен параметр Rule командлета New-AzAutoscaleProfile для приема пустого списка.</span><span class="sxs-lookup"><span data-stu-id="2d993-280">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="2d993-281">[12903]</span><span class="sxs-lookup"><span data-stu-id="2d993-281">[#12903]</span></span>
* <span data-ttu-id="2d993-282">Добавлены новые командлеты для более гибкой поддержки создания диагностических параметров:</span><span class="sxs-lookup"><span data-stu-id="2d993-282">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="2d993-283">Get-AzDiagnosticSettingCategory;</span><span class="sxs-lookup"><span data-stu-id="2d993-283">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="2d993-284">New-AzDiagnosticSetting;</span><span class="sxs-lookup"><span data-stu-id="2d993-284">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="2d993-285">New-AzDiagnosticDetailSetting.</span><span class="sxs-lookup"><span data-stu-id="2d993-285">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-287">Внесены изменения в текст справки и названия набора параметров для командлета Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="2d993-287">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-288">Az.Resources</span></span>
* <span data-ttu-id="2d993-289">Добавлена поддержка параметра -Tag в командлеты Set-AzTemplateSpec и New-AzTemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="2d993-289">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="2d993-290">Добавлена поддержка отображения тегов в форматировщик по умолчанию для функции "Спецификации шаблонов".</span><span class="sxs-lookup"><span data-stu-id="2d993-290">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-292">Добавлен пример в командлет Set-AzServiceFabricSetting с параметром SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="2d993-292">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="2d993-293">Обновлены связанные с приложениями командлеты для отображения сведений о том, что поддержка доступна только для ресурсов, развернутых через ARM.</span><span class="sxs-lookup"><span data-stu-id="2d993-293">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="2d993-294">Помечены нерекомендуемыми командлеты сертификации кластера Add-AzureRmServiceFabricClusterCertificate и Remove-AzureRmServiceFabricClusterCertificate.</span><span class="sxs-lookup"><span data-stu-id="2d993-294">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-295">Az.Sql</span></span>
* <span data-ttu-id="2d993-296">Добавлен тип SecondaryType к следующим командлетам:</span><span class="sxs-lookup"><span data-stu-id="2d993-296">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="2d993-297">New-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="2d993-297">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="2d993-298">Set-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="2d993-298">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="2d993-299">New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="2d993-299">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="2d993-300">Добавлен параметр HighAvailabilityReplicaCount к следующим командлетам:</span><span class="sxs-lookup"><span data-stu-id="2d993-300">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="2d993-301">New-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="2d993-301">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="2d993-302">Set-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-302">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="2d993-303">ReadReplicaCount теперь является псевдонимом HighAvailabilityReplicaCount для таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-303">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="2d993-304">New-AzSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="2d993-304">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="2d993-305">Set-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-305">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-306">Az.Storage</span></span>
* <span data-ttu-id="2d993-307">Реализована поддержка для отправки файла Azure размером до 4 TиБ.</span><span class="sxs-lookup"><span data-stu-id="2d993-307">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="2d993-308">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="2d993-308">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="2d993-309">Версия Azure.Storage.Blobs обновлена до 12.7.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-309">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="2d993-310">Версия Azure.Storage.Files.Shares обновлена до 12.5.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-310">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="2d993-311">Версия Azure.Storage.Files.DataLake обновлена до 12.5.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-311">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d993-312">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d993-312">Az.StorageSync</span></span>
* <span data-ttu-id="2d993-313">Добавлена функция политики распределения по уровням в службе "Синхронизация файлов" с политикой скачивания и режимом локального кэша.</span><span class="sxs-lookup"><span data-stu-id="2d993-313">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-314">Az.Websites</span></span>
* <span data-ttu-id="2d993-315">Теперь предотвращается создание дубликатов для правил ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="2d993-315">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d993-316">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="2d993-316">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d993-317">Эндрю Доусона (Andrew Dawson) (@dawsonar802) за обновление Get-AzKeyVaultCertificate.md (получение сертификата и его сохранение в виде раздела pfx для работы с PowerShell Core) (13557).</span><span class="sxs-lookup"><span data-stu-id="2d993-317">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="2d993-318">@iviark за обновление BYOK Powershell в API для здравоохранения (13518).</span><span class="sxs-lookup"><span data-stu-id="2d993-318">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="2d993-319">Джона Дакмантона (John Duckmanton) (@johnduckmanton) за исправление написания TagPatchOperation (13508).</span><span class="sxs-lookup"><span data-stu-id="2d993-319">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="2d993-320">Майкла Джеймса (Michael James) (@mikejwhat):</span><span class="sxs-lookup"><span data-stu-id="2d993-320">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="2d993-321">за корректировку справки по Get-AzLogicAppRunHistory (13513).</span><span class="sxs-lookup"><span data-stu-id="2d993-321">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="2d993-322">Ричарда де Цварта (Richard de Zwart) (@mountain65):</span><span class="sxs-lookup"><span data-stu-id="2d993-322">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="2d993-323">за обновление Update-AzAppConfigurationStore.md (13485);</span><span class="sxs-lookup"><span data-stu-id="2d993-323">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="2d993-324">за обновление Update New-AzCosmosDBAccount.md (13490).</span><span class="sxs-lookup"><span data-stu-id="2d993-324">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="2d993-325">@SteppingRazor, New-AzApiManagementProduct: за изменение значения по умолчанию для параметра SubscriptionsLimit на None (13457).</span><span class="sxs-lookup"><span data-stu-id="2d993-325">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="2d993-326">Стива Баркетта (Steve Burkett) (@SteveBurkettNZ) за исправление ошибки для параметра WorkspaceResourceId в примере (13589).</span><span class="sxs-lookup"><span data-stu-id="2d993-326">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="2d993-327">5.1.0 — ноябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-327">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-328">Az.Accounts</span></span>
* <span data-ttu-id="2d993-329">Исправлена проблема, из-за которой TenantId может не учитываться при использовании Connect-AzAccount -DeviceCode [№13477].</span><span class="sxs-lookup"><span data-stu-id="2d993-329">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="2d993-330">Добавлен новый командлет Get-AzAccessToken.</span><span class="sxs-lookup"><span data-stu-id="2d993-330">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="2d993-331">Исправлена проблема, которая возникает, если путь к профилю пользователя недоступен.</span><span class="sxs-lookup"><span data-stu-id="2d993-331">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="2d993-332">Исправлена проблема, вызывающая ошибку записи объекта при использовании Connect-AzAccount [№13419].</span><span class="sxs-lookup"><span data-stu-id="2d993-332">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="2d993-333">Добавлен параметр ContainerRegistryEndpointSuffix в Add-AzEnvironment и Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="2d993-333">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="2d993-334">Поддерживается прерывание входа при нажатии клавиш <kbd>CTRL</kbd>+<kbd>C</kbd>.</span><span class="sxs-lookup"><span data-stu-id="2d993-334">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="2d993-335">Исправлена проблема, из-за которой командлет Connect-AzAccount -KeyVaultAccessToken не работает [№13127].</span><span class="sxs-lookup"><span data-stu-id="2d993-335">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="2d993-336">Исправлена пустая ссылка и обработка метода без учета регистра в Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="2d993-336">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-337">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-337">Az.Aks</span></span>
* <span data-ttu-id="2d993-338">Исправлена проблема, из-за которой пользователь не может использовать субъект-службу для создания нового кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2d993-338">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="2d993-339">[№13012]</span><span class="sxs-lookup"><span data-stu-id="2d993-339">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="2d993-340">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-340">Az.AppConfiguration</span></span>
* <span data-ttu-id="2d993-341">Вышла общедоступная версия модуля Az.AppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-341">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-342">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-342">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-343">Улучшено сообщение об ошибке для команды New-AzDataFactoryV2LinkedServiceEncryptedCredential.</span><span class="sxs-lookup"><span data-stu-id="2d993-343">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-344">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-345">Обновлен отдельный пакет SDK ADLS до версии 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="2d993-345">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="2d993-346">Изменения: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="2d993-346">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="2d993-347">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="2d993-347">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="2d993-348">Добавлены новые командлеты пакета MSIX и обновлены командлеты приложений.</span><span class="sxs-lookup"><span data-stu-id="2d993-348">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-349">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-349">Az.EventHub</span></span>
* <span data-ttu-id="2d993-350">Исправлены команды кластера для кластера EventHub без тегов.</span><span class="sxs-lookup"><span data-stu-id="2d993-350">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="2d993-351">Обновлен текст справки для PartnerNamespace команд AzEventHubGeoDRConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-351">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-352">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-353">Добавлены параметры ResourceProviderConnection и PrivateLink в командлет New-AzHDInsightCluster для включения поддержки исходящих подключений ретранслятора и приватного канала.</span><span class="sxs-lookup"><span data-stu-id="2d993-353">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="2d993-354">В командлет New-AzHDInsightCluster добавлен параметр AmbariDatabase для включения поддержки пользовательской базы данных Ambari.</span><span class="sxs-lookup"><span data-stu-id="2d993-354">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="2d993-355">В параметр MetastoreType командлета Add-AzHDInsightMetastore добавлено значение AmbariDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-355">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-356">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-356">Az.IotHub</span></span>
* <span data-ttu-id="2d993-357">Разрешены теги в командлете для создания Центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-357">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-358">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-358">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-359">Поддерживается обновление тега хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="2d993-359">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d993-360">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d993-360">Az.LogicApp</span></span>
* <span data-ttu-id="2d993-361">Исправлена проблема, из-за которой командлет Get-AzLogicAppRunHistory получал только первую страницу результатов.</span><span class="sxs-lookup"><span data-stu-id="2d993-361">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-362">Az.Network</span></span>
* <span data-ttu-id="2d993-363">Обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-363">Updated below cmdlet</span></span> 
    - <span data-ttu-id="2d993-364">New-AzLoadBalancerFrontendIpConfigCommand, Set-AzLoadBalancerFrontendIpConfigCommand, Add-AzLoadBalancerFrontendIpConfigCommand:</span><span class="sxs-lookup"><span data-stu-id="2d993-364">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="2d993-365">добавлено свойство PublicIpAddressPrefix;</span><span class="sxs-lookup"><span data-stu-id="2d993-365">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="2d993-366">добавлено свойство PublicIpAddressPrefixId.</span><span class="sxs-lookup"><span data-stu-id="2d993-366">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="2d993-367">Добавлены новые свойства в следующие командлеты для включения глобальной балансировки нагрузки:</span><span class="sxs-lookup"><span data-stu-id="2d993-367">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="2d993-368">New-AzLoadBalancer:</span><span class="sxs-lookup"><span data-stu-id="2d993-368">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="2d993-369">добавлено свойство уровня SKU.</span><span class="sxs-lookup"><span data-stu-id="2d993-369">Added Sku Tier property</span></span>
    - <span data-ttu-id="2d993-370">New-AzPuplicIpAddress:</span><span class="sxs-lookup"><span data-stu-id="2d993-370">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="2d993-371">добавлено свойство уровня SKU.</span><span class="sxs-lookup"><span data-stu-id="2d993-371">Added Sku Tier property</span></span>
    - <span data-ttu-id="2d993-372">New-AzPublicIpPrefix:</span><span class="sxs-lookup"><span data-stu-id="2d993-372">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="2d993-373">добавлено свойство уровня SKU.</span><span class="sxs-lookup"><span data-stu-id="2d993-373">Added Sku Tier property</span></span>
    - <span data-ttu-id="2d993-374">New-AzLoadBalancerBackendAddressConfig:</span><span class="sxs-lookup"><span data-stu-id="2d993-374">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="2d993-375">добавлено свойство LoadBalancerFrontendIPConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="2d993-375">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="2d993-376">Обновлены планы по включению сообщений о прекращении поддержки для следующих командлетов:   -New-AzVirtualHubRoute   -New-AzVirtualHubRouteTable   -Add-AzVirtualHubRoute   -Add-AzVirtualHubRouteTable   -Get-AzVirtualHubRouteTable   -Remove-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="2d993-376">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="2d993-377">Обновлены планы по включению сообщений о прекращении поддержки для аргумента RouteTable для следующих командлетов:   -New-AzVirtualHub   -Set-AzVirtualHub   -Update-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="2d993-377">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="2d993-378">Аргументы -MinScaleUnits и -MaxScaleUnits в Set-AzExpressRouteGateway сделаны необязательными.</span><span class="sxs-lookup"><span data-stu-id="2d993-378">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="2d993-379">Добавлены новые командлеты для включения взаимной проверки подлинности и профилей SSL в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="2d993-379">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="2d993-380">Get-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2d993-380">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="2d993-381">New-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2d993-381">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="2d993-382">Remove-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2d993-382">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="2d993-383">Set-AzApplicationGatewayClientAuthConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2d993-383">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="2d993-384">Add-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="2d993-384">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="2d993-385">Get-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="2d993-385">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="2d993-386">New-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="2d993-386">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="2d993-387">Remove-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="2d993-387">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="2d993-388">Set-AzApplicationGatewayTrustedClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="2d993-388">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="2d993-389">Add-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="2d993-389">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="2d993-390">Get-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="2d993-390">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="2d993-391">New-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="2d993-391">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="2d993-392">Remove-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="2d993-392">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="2d993-393">Set-AzApplicationGatewaySslProfile;</span><span class="sxs-lookup"><span data-stu-id="2d993-393">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="2d993-394">Get-AzApplicationGatewaySslProfilePolicy;</span><span class="sxs-lookup"><span data-stu-id="2d993-394">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="2d993-395">Remove-AzApplicationGatewaySslProfilePolicy;</span><span class="sxs-lookup"><span data-stu-id="2d993-395">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="2d993-396">Set-AzApplicationGatewaySslProfilePolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-396">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-397">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-397">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-398">Указано время в формате UTC для BackupTime политики.</span><span class="sxs-lookup"><span data-stu-id="2d993-398">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="2d993-399">Изменено предупреждение о критическом изменении в командлете Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="2d993-399">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="2d993-400">Обновлен примера текста справки для командлета Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-400">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-401">Az.Resources</span></span>
* <span data-ttu-id="2d993-402">Исправлена проблема, из-за которой при использовании What-If отображаются две области группы ресурсов с разными регистрами.</span><span class="sxs-lookup"><span data-stu-id="2d993-402">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="2d993-403">Обновлен командлет Export-AzResourceGroup для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-403">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="2d993-404">Добавлены сведения о языке и региональных параметрах для методов синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="2d993-404">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-405">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-405">Az.Sql</span></span>
* <span data-ttu-id="2d993-406">Исправлены проблемы, из-за которых командлет Set-AzSqlDatabaseAudit не поддерживал базу данных уровня "Гипермасштабирование" и не удавалось определить выпуск базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-406">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="2d993-407">В New-AzSqlInstance и Set-AzSqlInstance добавлен параметр MaintenanceConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="2d993-407">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="2d993-408">Исправлена ошибка в GetAzureSqlDatabaseReplicationLink.cs, где параметр PartnerServerName проверялся по значению, а не по ключу.</span><span class="sxs-lookup"><span data-stu-id="2d993-408">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-409">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-409">Az.Websites</span></span>
* <span data-ttu-id="2d993-410">Включена поддержка новых возможностей ограничения доступа: ServiceTag, multi-ip и http-headers.</span><span class="sxs-lookup"><span data-stu-id="2d993-410">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d993-411">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="2d993-411">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d993-412">Джон К. Мартин (John Q. Martin) (@johnmart82), добавление сведений о предварительных требованиях для брандмауэра (№13385).</span><span class="sxs-lookup"><span data-stu-id="2d993-412">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="2d993-413">Маникандан Дураисами (Manikandan Duraisamy) (@madurais-msft), исправление аргумента PublicSubnetName (№13417).</span><span class="sxs-lookup"><span data-stu-id="2d993-413">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="2d993-414">@mahortas, обновление значений параметров для параметра -HostName (№13349).</span><span class="sxs-lookup"><span data-stu-id="2d993-414">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="2d993-415">@MariachiForHire, добавлены поддерживаемые значения TrafficAnalyticsInterval (№13304).</span><span class="sxs-lookup"><span data-stu-id="2d993-415">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="2d993-416">Майкл Джеймс (Michael James) (@mikejwhat), включена поддержка Get-AzLogicAppRunHistory для получения более 30 записей (№13393).</span><span class="sxs-lookup"><span data-stu-id="2d993-416">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="2d993-417">Шашикант Шакья (Shashikant Shakya) (@shshakya), обновление файла Restore-AzSqlInstanceDatabase.md (№13404).</span><span class="sxs-lookup"><span data-stu-id="2d993-417">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="2d993-418">5.0.0 — октябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-418">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-419">Az.Accounts</span></span>
* <span data-ttu-id="2d993-420">[Критическое изменение] Удалены командлеты Get-AzProfile и Select-AzProfile.</span><span class="sxs-lookup"><span data-stu-id="2d993-420">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="2d993-421">Библиотека проверки подлинности Azure Active Directory заменена библиотекой проверки подлинности Microsoft (MSAL).</span><span class="sxs-lookup"><span data-stu-id="2d993-421">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-422">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-422">Az.Aks</span></span>
* <span data-ttu-id="2d993-423">[Критическое изменение] Удален псевдоним параметра ClientIdAndSecret в командлетах New-AzAksCluster и Set-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-423">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="2d993-424">[Критическое изменение] Изменено значение по умолчанию NodeVmSetType в New-AzAksCluster с AvailabilitySet на VirtualMachineScaleSets.</span><span class="sxs-lookup"><span data-stu-id="2d993-424">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="2d993-425">[Критическое изменение] Изменено значение по умолчанию NetworkPlugin в New-AzAksCluster с None на azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-425">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="2d993-426">[Критическое изменение] Удален параметр NodeOsType в New-AzAksCluster, так как поддерживается только одно значение Linux.</span><span class="sxs-lookup"><span data-stu-id="2d993-426">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="2d993-427">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d993-427">Az.Billing</span></span>
* <span data-ttu-id="2d993-428">Добавлен командлет Get-AzBillingAccount.</span><span class="sxs-lookup"><span data-stu-id="2d993-428">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="2d993-429">Добавлен командлет Get-AzBillingProfile.</span><span class="sxs-lookup"><span data-stu-id="2d993-429">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="2d993-430">Добавлен командлет Get-AzInvoiceSection.</span><span class="sxs-lookup"><span data-stu-id="2d993-430">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="2d993-431">Добавлены новые параметры в командлет Get-AzBillingInvoice.</span><span class="sxs-lookup"><span data-stu-id="2d993-431">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="2d993-432">Удалены свойства DownloadUrlExpiry, Type и BillingPeriodNames из ответа командлета Get-AzBillingInvoice.</span><span class="sxs-lookup"><span data-stu-id="2d993-432">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-433">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-433">Az.Cdn</span></span>
* <span data-ttu-id="2d993-434">Добавлены командлеты для включения функций с поддержкой нескольких источников и приватных каналов.</span><span class="sxs-lookup"><span data-stu-id="2d993-434">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-435">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-436">Обновлен пакет SDK до версии 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="2d993-436">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-437">Az.Compute</span></span>
* <span data-ttu-id="2d993-438">Добавлен параметр -VmssId в командлет New-AzVm.</span><span class="sxs-lookup"><span data-stu-id="2d993-438">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="2d993-439">Добавлен параметр PlatformFaultDomainCount в командлет New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-439">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="2d993-440">Добавлен новый командлет Get-AzDiskEncryptionSetAssociatedResource.</span><span class="sxs-lookup"><span data-stu-id="2d993-440">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="2d993-441">Добавлены необязательные параметры Tier и LogicalSectorSize в командлет New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-441">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="2d993-442">Добавлены необязательные параметры Tier, MaxSharesCount, DiskIOPSReadOnly и DiskMBpsReadOnly в командлет New-AzDiskUpdateConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-442">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d993-443">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d993-443">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d993-444">[Критическое изменение] Обновлена версия API до 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-444">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="2d993-445">[Критическое изменение] Удалены номер SKU "Классический" и параметр StorageAccountName из командлета New-AzContainerRegistry.</span><span class="sxs-lookup"><span data-stu-id="2d993-445">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="2d993-446">Добавлены новые командлеты: Connect-AzContainerRegistry, Import-AzContainerRegistry, Get-AzContainerRegistryUsage, New-AzContainerRegistryNetworkRule, Set-AzContainerRegistryNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="2d993-446">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="2d993-447">Добавлен новый параметр NetworkRuleSet в командлет Update-AzContainerRegistry.</span><span class="sxs-lookup"><span data-stu-id="2d993-447">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="2d993-448">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="2d993-448">Az.Databricks</span></span>
* <span data-ttu-id="2d993-449">Исправлена ошибка, которая может вызвать сбой при обновлении рабочей области Databricks без `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="2d993-449">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-450">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-450">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-451">Пакет SDK ADF для .NET обновлен до версии 4.12.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-451">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="2d993-452">Пакет SDK клиента шифрования ADF обновлен до версии 4.14.7587.7.</span><span class="sxs-lookup"><span data-stu-id="2d993-452">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="2d993-453">Добавлены команды Stop-AzDataFactoryV2TriggerRun и Invoke-AzDataFactoryV2TriggerRun.</span><span class="sxs-lookup"><span data-stu-id="2d993-453">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="2d993-454">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="2d993-454">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="2d993-455">Требуется свойство Location для создания объектов ARM верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2d993-455">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="2d993-456">\*`ApplicationGroupType` требуется для `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="2d993-456">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="2d993-457">\*`HostPoolArmPath` требуется для `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="2d993-457">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="2d993-458">\*Добавлен параметр `PreferredAppGroupType` для `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="2d993-458">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d993-459">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d993-459">Az.Functions</span></span>
* <span data-ttu-id="2d993-460">[Критическое изменение] Удален параметр-переключатель IncludeSlot из всех наборов параметров Get-AzFunctionApp, кроме одного.</span><span class="sxs-lookup"><span data-stu-id="2d993-460">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="2d993-461">Командлет теперь поддерживает получение слотов развертывания в результатах, если указать IncludeSlot.</span><span class="sxs-lookup"><span data-stu-id="2d993-461">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="2d993-462">Обновлен командлет New-AzFunctionApp:</span><span class="sxs-lookup"><span data-stu-id="2d993-462">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="2d993-463">исправлена проблема с -DisableApplicationInsights, чтобы при указании этого параметра не создавался проект Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2d993-463">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="2d993-464">[№12728]</span><span class="sxs-lookup"><span data-stu-id="2d993-464">[#12728]</span></span>
  - <span data-ttu-id="2d993-465">[Критическое изменение] Отключена поддержка создания приложений-функций PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="2d993-465">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="2d993-466">[Критическое изменение] Изменена версия среды выполнения по умолчанию (с версии 6.2 на 7.0) в Функциях версии 3 в Windows для приложений-функций PowerShell, если не указать параметр RuntimeVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-466">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="2d993-467">[Критическое изменение] Изменена версия среды выполнения по умолчанию (с версии 10 на 12) в Функциях версии 3 в Windows и Linux для приложений-функций Node, если не указать параметр RuntimeVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-467">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="2d993-468">[Критическое изменение] Изменена версия среды выполнения по умолчанию (с версии 3.7 на 3.8) в Функциях версии 3 в Linux для приложений-функций Python, если не указать параметр RuntimeVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-468">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-469">Az.HDInsight</span></span>
 * <span data-ttu-id="2d993-470">Для командлета New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="2d993-470">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="2d993-471">заменен параметр DefaultStorageAccountName на StorageAccountResourceId;</span><span class="sxs-lookup"><span data-stu-id="2d993-471">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="2d993-472">заменен параметр DefaultStorageAccountKey на StorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="2d993-472">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="2d993-473">заменен параметр DefaultStorageAccountType на StorageAccountType;</span><span class="sxs-lookup"><span data-stu-id="2d993-473">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="2d993-474">удален параметр PublicNetworkAccessType;</span><span class="sxs-lookup"><span data-stu-id="2d993-474">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="2d993-475">удален параметр OutboundPublicNetworkAccessType.</span><span class="sxs-lookup"><span data-stu-id="2d993-475">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="2d993-476">Добавлены новые параметры: StorageFileSystem и StorageAccountManagedIdentity для включения поддержки ADLS 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="2d993-476">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="2d993-477">Добавлен новый параметр EnableIDBroker для включения поддержки брокера удостоверений HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d993-477">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="2d993-478">Добавлены новые параметры: KafkaClientGroupId, KafkaClientGroupName и KafkaManagementNodeSize для включения поддержки прокси-сервера REST для Kafka.</span><span class="sxs-lookup"><span data-stu-id="2d993-478">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="2d993-479">Для командлета New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="2d993-479">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="2d993-480">заменен параметр DefaultStorageAccountName на StorageAccountResourceId;</span><span class="sxs-lookup"><span data-stu-id="2d993-480">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="2d993-481">заменен параметр DefaultStorageAccountKey на StorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="2d993-481">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="2d993-482">заменен параметр DefaultStorageAccountType на StorageAccountType;</span><span class="sxs-lookup"><span data-stu-id="2d993-482">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="2d993-483">удален параметр PublicNetworkAccessType;</span><span class="sxs-lookup"><span data-stu-id="2d993-483">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="2d993-484">удален параметр OutboundPublicNetworkAccessType.</span><span class="sxs-lookup"><span data-stu-id="2d993-484">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="2d993-485">Для командлета Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="2d993-485">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="2d993-486">заменен параметр StorageAccountName на StorageAccountResourceId.</span><span class="sxs-lookup"><span data-stu-id="2d993-486">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="2d993-487">Для командлета Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="2d993-487">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="2d993-488">заменен параметр Domain на DomainResourceId;</span><span class="sxs-lookup"><span data-stu-id="2d993-488">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="2d993-489">удалено обязательное требование использовать параметр OrganizationalUnitDN.</span><span class="sxs-lookup"><span data-stu-id="2d993-489">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-490">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-491">[Критическое изменение] Не рекомендуется использовать параметр DisableSoftDelete в командлете New-AzKeyVault и параметр EnableSoftDelete в командлете Update-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d993-491">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="2d993-492">[Критическое изменение] Удален атрибут SecretValueText, чтобы значение SecretValue не отображалось напрямую [№12266].</span><span class="sxs-lookup"><span data-stu-id="2d993-492">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="2d993-493">Включена поддержка нового типа ресурса: управляемое устройство HSM.</span><span class="sxs-lookup"><span data-stu-id="2d993-493">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="2d993-494">CRUD управляемого устройства HSM и командлеты для работы с ключами на управляемом устройстве HSM.</span><span class="sxs-lookup"><span data-stu-id="2d993-494">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="2d993-495">Полное резервное копирование и восстановление HSM, создание ключа AES, резервное копирование и восстановление домена безопасности, RBAC.</span><span class="sxs-lookup"><span data-stu-id="2d993-495">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d993-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d993-496">Az.ManagedServices</span></span>
* <span data-ttu-id="2d993-497">[Критическое изменение] Обновлены соглашения об именовании параметров и связанные примеры.</span><span class="sxs-lookup"><span data-stu-id="2d993-497">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-498">Az.Network</span></span>
* <span data-ttu-id="2d993-499">[Критическое изменение] Удален параметр HostedSubnet и вместо него добавлен параметр Subnet.</span><span class="sxs-lookup"><span data-stu-id="2d993-499">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="2d993-500">Добавлены новые командлеты для маршрутов пиринга виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="2d993-500">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="2d993-501">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="2d993-501">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="2d993-502">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="2d993-502">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="2d993-503">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2d993-503">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="2d993-504">добавлен параметр -SkuTier;</span><span class="sxs-lookup"><span data-stu-id="2d993-504">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="2d993-505">добавлен параметр -SkuName и номер SKU в качестве псевдонима;</span><span class="sxs-lookup"><span data-stu-id="2d993-505">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="2d993-506">удален параметр -Sku.</span><span class="sxs-lookup"><span data-stu-id="2d993-506">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="2d993-507">[Критическое изменение] Сделан обязательным аргумент Connectionlink в командлетах Start-AzVpnConnectionPacketCapture и Stop-AzVpnConnectionPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="2d993-507">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="2d993-508">[Критическое изменение] В командлете New-AzNetworkWatcherConnectionMonitorEndPointObject удален параметр -Filter.</span><span class="sxs-lookup"><span data-stu-id="2d993-508">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="2d993-509">[Критическое изменение] Заменен командлет New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject на New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-509">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="2d993-510">Обновлен командлет New-AzNetworkWatcherConnectionMonitorEndPointObject:</span><span class="sxs-lookup"><span data-stu-id="2d993-510">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="2d993-511">добавлен параметр -Type;</span><span class="sxs-lookup"><span data-stu-id="2d993-511">Added parameter '-Type'</span></span>
    - <span data-ttu-id="2d993-512">добавлен параметр -CoverageLevel;</span><span class="sxs-lookup"><span data-stu-id="2d993-512">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="2d993-513">добавлен параметр -Scope.</span><span class="sxs-lookup"><span data-stu-id="2d993-513">Added parameter '-Scope'</span></span>
* <span data-ttu-id="2d993-514">В командлет New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject добавлен новый параметр -DestinationPortBehavior.</span><span class="sxs-lookup"><span data-stu-id="2d993-514">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-515">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-515">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-516">Исправлена проблема с восстановлением рабочей нагрузки для разрешений участника.</span><span class="sxs-lookup"><span data-stu-id="2d993-516">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="2d993-517">Добавлены новые наборы параметров и проверки для командлета Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="2d993-517">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-518">Az.Resources</span></span>
* <span data-ttu-id="2d993-519">Исправлена ошибка синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="2d993-519">Fixed parsing bug</span></span>
* <span data-ttu-id="2d993-520">Обновлены командлеты What-If шаблона ARM для удаления сообщения о предварительной версии из результатов.</span><span class="sxs-lookup"><span data-stu-id="2d993-520">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="2d993-521">Исправлена ошибка, из-за которой командлеты развертывания шаблонов завершаются сбоем, если для параметра -WhatIf задана более высокая область [№13038].</span><span class="sxs-lookup"><span data-stu-id="2d993-521">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="2d993-522">Исправлена ошибка, из-за которой командлеты развертывания шаблона не сохраняют регистр для параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d993-522">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="2d993-523">Добавлена версия API по умолчанию для использования в командлете Export-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-523">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="2d993-524">Добавлены командлеты для Спецификаций шаблонов (Get-AzTemplateSpec, Set-AzTemplateSpec, New-AzTemplateSpec, Remove-AzTemplateSpec, Export-AzTemplateSpec).</span><span class="sxs-lookup"><span data-stu-id="2d993-524">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="2d993-525">Включена поддержка развертывания Спецификаций шаблонов с помощью существующих командлетов развертывания (с использованием нового параметра -TemplateSpecId).</span><span class="sxs-lookup"><span data-stu-id="2d993-525">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="2d993-526">Включена возможность использовать SDK в командлете Get-AzResourceGroupDeploymentOperation.</span><span class="sxs-lookup"><span data-stu-id="2d993-526">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="2d993-527">Удален параметр -ApiVersion из командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-527">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-528">Az.Sql</span></span>
* <span data-ttu-id="2d993-529">Исправлена ошибка, из-за которой выполнение командлета New-AzSqlDatabaseExport завершается сбоем, если не указать networkIsolation [№13097].</span><span class="sxs-lookup"><span data-stu-id="2d993-529">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="2d993-530">Исправлена ошибка, из-за которой командлеты New-AzSqlDatabaseExport и New-AzSqlDatabaseImport не возвращали OperationStatusLink в результирующем объекте [№13097].</span><span class="sxs-lookup"><span data-stu-id="2d993-530">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="2d993-531">Обновлены URL-адреса парных регионов Azure в предупреждениях об избыточности хранилища резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2d993-531">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="2d993-532">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-532">Az.Storage</span></span>
* <span data-ttu-id="2d993-533">Удалено устаревшее свойство RestorePolicy.LastEnabledTime.</span><span class="sxs-lookup"><span data-stu-id="2d993-533">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="2d993-534">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-534">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d993-535">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-535">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d993-536">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-536">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="2d993-537">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-537">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="2d993-538">Изменен тип DaysAfterModificationGreaterThan с целочисленного на целочисленный?</span><span class="sxs-lookup"><span data-stu-id="2d993-538">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="2d993-539">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-539">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d993-540">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-540">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d993-541">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2d993-541">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="2d993-542">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2d993-542">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="2d993-543">Поддерживается создание или обновление общей папки с уровнем доступа.</span><span class="sxs-lookup"><span data-stu-id="2d993-543">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="2d993-544">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d993-544">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="2d993-545">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d993-545">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="2d993-546">Поддерживается установка, обновление и удаление ACL рекурсивно для элемента Datalake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="2d993-546">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="2d993-547">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="2d993-547">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="2d993-548">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="2d993-548">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="2d993-549">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="2d993-549">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="2d993-550">Включена поддержка политики доступа контейнеров с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="2d993-550">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="2d993-551">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-551">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="2d993-552">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-552">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="2d993-553">Изменены выходные данные командлета политики доступа контейнера get/set путем изменения типа разрешения дочернего свойства с enum на string.</span><span class="sxs-lookup"><span data-stu-id="2d993-553">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="2d993-554">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-554">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="2d993-555">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-555">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="2d993-556">Исправлена проблема с примером скрипта для политики управления наборами с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="2d993-556">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="2d993-557">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-557">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-558">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-558">Az.Websites</span></span>
* <span data-ttu-id="2d993-559">Включена поддержка ценовой категории "Премиум" версии 3.</span><span class="sxs-lookup"><span data-stu-id="2d993-559">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="2d993-560">Пакет SDK для веб-сайтов обновлен до версии 3.1.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-560">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d993-561">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="2d993-561">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d993-562">@atul-ram, обновление Get-AzDelegation.md (№13176).</span><span class="sxs-lookup"><span data-stu-id="2d993-562">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="2d993-563">@dineshreddy007, правильное назначение ролей приложения в случае регистрации Stack HCI с использованием токена WAC.</span><span class="sxs-lookup"><span data-stu-id="2d993-563">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="2d993-564">(№13249).</span><span class="sxs-lookup"><span data-stu-id="2d993-564">(#13249)</span></span>
* <span data-ttu-id="2d993-565">@kongou-ae, обновление New-AzOffice365PolicyProperty.md (№13217).</span><span class="sxs-lookup"><span data-stu-id="2d993-565">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="2d993-566">Lohith Chowdary Chilukuri (@Lochiluk), обновление Set-AzApplicationGateway.md (№13150).</span><span class="sxs-lookup"><span data-stu-id="2d993-566">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="2d993-567">Matthew Burleigh (@mburleigh):</span><span class="sxs-lookup"><span data-stu-id="2d993-567">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="2d993-568">добавление ссылок на командлеты PowerShell, указанные в документации (№13203);</span><span class="sxs-lookup"><span data-stu-id="2d993-568">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="2d993-569">добавление ссылок на командлеты PowerShell, указанные в документации (№13190);</span><span class="sxs-lookup"><span data-stu-id="2d993-569">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="2d993-570">добавление ссылок на командлеты PowerShell, указанные в документации (№13189);</span><span class="sxs-lookup"><span data-stu-id="2d993-570">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="2d993-571">добавление ссылок на указанные командлеты (№13137);</span><span class="sxs-lookup"><span data-stu-id="2d993-571">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="2d993-572">добавление ссылок на командлеты PowerShell, указанные в документации (№13204);</span><span class="sxs-lookup"><span data-stu-id="2d993-572">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="2d993-573">добавление ссылок на командлеты PowerShell, указанные в документации (№13205).</span><span class="sxs-lookup"><span data-stu-id="2d993-573">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="2d993-574">4.8.0 — октябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-574">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-575">Az.Accounts</span></span>
* <span data-ttu-id="2d993-576">Исправлена проблема с анализом фиксированных дат DateTime в общих библиотеках [№ 13045]</span><span class="sxs-lookup"><span data-stu-id="2d993-576">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-577">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-578">Добавлен командлет New-AzCognitiveServicesAccountApiProperty.</span><span class="sxs-lookup"><span data-stu-id="2d993-578">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="2d993-579">Добавлена поддержка параметра ApiProperty для New-AzCognitiveServicesAccount и Set-AzCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="2d993-579">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-580">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-580">Az.Compute</span></span>
* <span data-ttu-id="2d993-581">Исправлена проблема в Update-ASRRecoveryPlan путем заполнения FailoverTypes.</span><span class="sxs-lookup"><span data-stu-id="2d993-581">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="2d993-582">В командлет Get-AzVmImage добавлены необязательные параметры -Top и -OrderBy.</span><span class="sxs-lookup"><span data-stu-id="2d993-582">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="2d993-583">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="2d993-583">Az.Databricks</span></span>
* <span data-ttu-id="2d993-584">Вышла общедоступная версия модуля Az.Databricks.</span><span class="sxs-lookup"><span data-stu-id="2d993-584">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="2d993-585">Добавлена поддержка пиринга между виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="2d993-585">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-586">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-587">Исправлена опечатка в выходных сообщениях</span><span class="sxs-lookup"><span data-stu-id="2d993-587">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-588">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-588">Az.EventHub</span></span>
* <span data-ttu-id="2d993-589">Добавлен необязательный параметр-переключатель TrustedServiceAccessEnabled в командлет Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-589">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-590">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-590">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-591">Добавлено предупреждающее сообщение о том, что планируется прекращение поддержки параметров PublicNetworkAccessType и OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="2d993-591">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="2d993-592">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountName на StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2d993-592">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="2d993-593">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountKey на StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2d993-593">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="2d993-594">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountType на StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2d993-594">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="2d993-595">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageContainer на StorageContainer</span><span class="sxs-lookup"><span data-stu-id="2d993-595">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="2d993-596">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageRootPath на StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="2d993-596">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-597">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-597">Az.IotHub</span></span>
* <span data-ttu-id="2d993-598">Обновлен пакет SDK для устройств.</span><span class="sxs-lookup"><span data-stu-id="2d993-598">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-599">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-600">Указана точная дата удаления свойства SecretValueText</span><span class="sxs-lookup"><span data-stu-id="2d993-600">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d993-601">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d993-601">Az.ManagedServices</span></span>
* <span data-ttu-id="2d993-602">Изменены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="2d993-602">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-603">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-603">Az.Monitor</span></span>
* <span data-ttu-id="2d993-604">Исправлена ошибка, не позволявшая подавить предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="2d993-604">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="2d993-605">[№ 12889]</span><span class="sxs-lookup"><span data-stu-id="2d993-605">[#12889]</span></span>
* <span data-ttu-id="2d993-606">Добавлена поддержка параметра SkipMetricValidation в критериях правила генерации оповещений.</span><span class="sxs-lookup"><span data-stu-id="2d993-606">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="2d993-607">Это позволяет создать правило генерации оповещений для пользовательской метрики, которая еще не создана, настроив пропуск проверки этой метрики.</span><span class="sxs-lookup"><span data-stu-id="2d993-607">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-608">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-608">Az.Network</span></span>
* <span data-ttu-id="2d993-609">Добавлена политика Office365 в ресурс VPNSite</span><span class="sxs-lookup"><span data-stu-id="2d993-609">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="2d993-610">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-610">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-612">Добавлена проверка имени контейнера для резервного копирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d993-612">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d993-613">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d993-613">Az.RedisCache</span></span>
* <span data-ttu-id="2d993-614">Устранен сбой командлетов New-AzRedisCache и Set-AzRedisCache из-за проблемы с разрешениями, связанной с регистрацией поставщика ресурсов Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="2d993-614">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-615">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-615">Az.Sql</span></span>
* <span data-ttu-id="2d993-616">Добавлен параметр BackupStorageRedundancy к следующим командлетам:</span><span class="sxs-lookup"><span data-stu-id="2d993-616">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="2d993-617">Restore-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="2d993-617">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="2d993-618">New-AzSqlDatabaseCopy;</span><span class="sxs-lookup"><span data-stu-id="2d993-618">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="2d993-619">New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="2d993-619">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="2d993-620">Удален учет регистра для параметра BackupStorageRedundancy во всех ссылках на базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="2d993-620">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="2d993-621">Обновлены имена в предупреждающем сообщении BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="2d993-621">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-622">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-622">Az.Storage</span></span>
* <span data-ttu-id="2d993-623">Добавлена поддержка включения, отключения и получения свойств обратимого удаления для общей папки в службе файлов учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2d993-623">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="2d993-624">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-624">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="2d993-625">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-625">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="2d993-626">Поддерживается вывод списка общих папок в учетной записи хранения, включая удаленные общие папки, а также добавлена возможность получить данные об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="2d993-626">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="2d993-627">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d993-627">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="2d993-628">Добавлено восстановление удаленной общей папки</span><span class="sxs-lookup"><span data-stu-id="2d993-628">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="2d993-629">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d993-629">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="2d993-630">Изменены командлеты для изменения свойств службы BLOB-объектов. Эти командлеты не получают свойства с сервера, а только сохраняют новые параметры на сервер.</span><span class="sxs-lookup"><span data-stu-id="2d993-630">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="2d993-631">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-631">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="2d993-632">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-632">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="2d993-633">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-633">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d993-634">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-634">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d993-635">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-635">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="2d993-636">Устранена проблема с получением справки для значения по умолчанию для параметра -Kind командлета New-AzStorageAccount [№ 12189]</span><span class="sxs-lookup"><span data-stu-id="2d993-636">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="2d993-637">Устранена проблема путем добавления примера правильной настройки ContentType для отправки большого двоичного объекта [№ 12989]</span><span class="sxs-lookup"><span data-stu-id="2d993-637">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="2d993-638">4.7.0 — сентябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-638">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-639">Az.Accounts</span></span>
* <span data-ttu-id="2d993-640">Изменен формат сообщений о предстоящих критических изменениях.</span><span class="sxs-lookup"><span data-stu-id="2d993-640">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="2d993-641">Версия Azure.Core обновлена до 1.4.1.</span><span class="sxs-lookup"><span data-stu-id="2d993-641">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-642">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-642">Az.Aks</span></span>
* <span data-ttu-id="2d993-643">Добавлена логика проверки параметров на стороне клиента для командлетов New-AzAksCluster, Set-AzAksCluster и New-AzAksNodePool.</span><span class="sxs-lookup"><span data-stu-id="2d993-643">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="2d993-644">[12372]</span><span class="sxs-lookup"><span data-stu-id="2d993-644">[#12372]</span></span>
* <span data-ttu-id="2d993-645">Добавлена поддержка для надстроек в командлете New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-645">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="2d993-646">[11239]</span><span class="sxs-lookup"><span data-stu-id="2d993-646">[#11239]</span></span>
* <span data-ttu-id="2d993-647">Добавлены командлеты Enable-AzAksAddOn и Disable-AzAksAddOn для надстроек.</span><span class="sxs-lookup"><span data-stu-id="2d993-647">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="2d993-648">[11239]</span><span class="sxs-lookup"><span data-stu-id="2d993-648">[#11239]</span></span>
* <span data-ttu-id="2d993-649">Добавлен параметр GenerateSshKey для командлета New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-649">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="2d993-650">[12371]</span><span class="sxs-lookup"><span data-stu-id="2d993-650">[#12371]</span></span>
* <span data-ttu-id="2d993-651">Обновлена версия API до 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-651">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-653">Реализовано отображение дополнительных юридических условий для определенных API.</span><span class="sxs-lookup"><span data-stu-id="2d993-653">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-654">Az.Compute</span></span>
* <span data-ttu-id="2d993-655">Добавлен необязательный параметр -EncryptionType к командлету New-AzVmDiskEncryptionSetConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-655">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="2d993-656">Новые командлеты для нового типа ресурсов: DiskAccess (Get-AzDiskAccess, New-AzDiskAccess, Get-AzDiskAccess).</span><span class="sxs-lookup"><span data-stu-id="2d993-656">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="2d993-657">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-657">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="2d993-658">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-658">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="2d993-659">Добавлено свойство PatchStatus к представлению экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d993-659">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="2d993-660">Добавлено свойство VMHealth к представлению экземпляра виртуальной машины, которое является возвращенным объектом при вызове Get-AzVm с параметром -Status.</span><span class="sxs-lookup"><span data-stu-id="2d993-660">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="2d993-661">Добавлено поле AssignedHost к представлениям экземпляра Get-AzVM и Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-661">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="2d993-662">В поле отображается идентификатор ресурса для экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d993-662">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="2d993-663">Добавлен необязательный параметр -SupportAutomaticPlacement к командлету New-AzHostGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-663">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="2d993-664">Добавлен параметр -HostGroupId к командлетам New-AzVm и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-664">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-665">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-665">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-666">Версия пакета SDK ADF для .NET обновлена до 4.11.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-666">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-667">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-667">Az.EventHub</span></span>
* <span data-ttu-id="2d993-668">Добавлены новые командлеты кластера: New-AzEventHubCluster, Set-AzEventHubCluster, Get-AzEventHubCluster, Remove-AzEventHubCluster, Get-AzEventHubClustersAvailableRegions.</span><span class="sxs-lookup"><span data-stu-id="2d993-668">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="2d993-669">Исправление для проблемы № 10722: исправление ошибки, из-за которой свойству AuthorizationRule.Rights назначалось только значение Listen (Прослушивание).</span><span class="sxs-lookup"><span data-stu-id="2d993-669">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d993-670">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d993-670">Az.Functions</span></span>
* <span data-ttu-id="2d993-671">Удалена возможность создавать Функции версии 2 в регионах, которые не поддерживают ее.</span><span class="sxs-lookup"><span data-stu-id="2d993-671">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="2d993-672">PowerShell 6.2 не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="2d993-672">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="2d993-673">Добавлено предупреждение при создании пользователем приложения-функции PowerShell 6.2 о том, что рекомендуется создать приложение-функцию PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-673">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-674">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-675">Добавлена поддержка создания кластера с использованием конфигурации автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="2d993-675">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="2d993-676">Добавлен новый параметр AutoscaleConfiguration к командлету New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-676">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="2d993-677">Добавлена поддержка управления конфигурацией автомасштабирования для кластера.</span><span class="sxs-lookup"><span data-stu-id="2d993-677">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="2d993-678">Добавлен новый командлет Get-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-678">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d993-679">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-679">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d993-680">Добавлен новый командлет Set-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-680">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d993-681">Добавлен новый командлет Remove-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-681">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d993-682">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleScheduleCondition.</span><span class="sxs-lookup"><span data-stu-id="2d993-682">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-683">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-683">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-684">Добавлена поддержка авторизации с помощью RBAC [10557].</span><span class="sxs-lookup"><span data-stu-id="2d993-684">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="2d993-685">Расширена обработка ошибок в командлете Set-AzKeyVaultAccessPolicy [4007].</span><span class="sxs-lookup"><span data-stu-id="2d993-685">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="2d993-686">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="2d993-686">Az.Kusto</span></span>
* <span data-ttu-id="2d993-687">Выпущена общедоступная версия модуля Az.Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d993-687">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-688">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-688">Az.Network</span></span>
* <span data-ttu-id="2d993-689">[Критическое изменение] Обновлены приведенные ниже командлеты для соответствия виртуальному маршрутизатору ресурсов и виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="2d993-689">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="2d993-690">New-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="2d993-690">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="2d993-691">Добавлен параметр -HostedSubnet для поддержки дочернего ресурса конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d993-691">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="2d993-692">Удалены параметры -HostedGateway и -HostedGatewayId.</span><span class="sxs-lookup"><span data-stu-id="2d993-692">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="2d993-693">Get-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="2d993-693">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="2d993-694">добавлен набор параметров на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-694">Added subscription level parameter set</span></span>
    - <span data-ttu-id="2d993-695">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2d993-695">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="2d993-696">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2d993-696">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="2d993-697">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2d993-697">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="2d993-698">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2d993-698">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="2d993-699">Добавлен новый командлет для порта Azure Express Route.</span><span class="sxs-lookup"><span data-stu-id="2d993-699">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="2d993-700">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="2d993-700">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="2d993-701">Добавлено свойство RemoteBgpCommunities к ресурсу пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-701">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="2d993-702">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="2d993-702">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="2d993-703">Добавлено свойство VpnGatewayIpConfigurations в выходные данные командлета Get-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-703">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="2d993-704">Исправлена ошибка командлета Set-AzApplicationGatewaySslCertificate [9488].</span><span class="sxs-lookup"><span data-stu-id="2d993-704">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="2d993-705">Добавлен параметр AllowActiveFTP в AzureFirewall.</span><span class="sxs-lookup"><span data-stu-id="2d993-705">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="2d993-706">Обновлены следующие команды для функции: Включена возможность настройки и удаления параметров безопасности в Интернете на VPN-шлюзе P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-706">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="2d993-707">Обновлен командлет New-AzP2sVpnGateway: Добавлен необязательный параметр EnableInternetSecurityFlag для клиентов, позволяющий задать значение true для включения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="2d993-707">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="2d993-708">Обновлен командлет Update-AzP2sVpnGateway: Добавлены необязательные параметры EnableInternetSecurityFlag и DisableInternetSecurityFlag для клиентов, позволяющий задать значение true/false для включения/отключения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="2d993-708">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="2d993-709">Добавлен новый командлет Reset-AzP2sVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз P2S виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="2d993-709">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="2d993-710">Добавлен новый командлет Reset-AzVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="2d993-710">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="2d993-711">Обновлен командлет Set-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-711">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="2d993-712">Для свойств группы безопасности сети и таблицы маршрутизации подсети теперь задаются значения NULL, если они явно указаны в параметрах [1548][9718].</span><span class="sxs-lookup"><span data-stu-id="2d993-712">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-713">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-713">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-714">Исправлено состояние удаления для элементов резервного копирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d993-714">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-715">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-715">Az.Resources</span></span>
* <span data-ttu-id="2d993-716">Добавлена отсутствующая проверка для командлета Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="2d993-716">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="2d993-717">Добавлен важный атрибут в параметр SubscriptionId командлета Get-AzResourceGroupDeploymentOperation.</span><span class="sxs-lookup"><span data-stu-id="2d993-717">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="2d993-718">Обновлены командлеты What-If шаблона ARM для отображения изменений ресурса Ignore последними.</span><span class="sxs-lookup"><span data-stu-id="2d993-718">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="2d993-719">Исправлены проблемы безопасности и сериализации параметров массива для командлетов развертывания [12773].</span><span class="sxs-lookup"><span data-stu-id="2d993-719">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-720">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-720">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-721">Добавлены новые командлеты для управляемых кластеров и типов узлов:</span><span class="sxs-lookup"><span data-stu-id="2d993-721">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="2d993-722">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2d993-722">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d993-723">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2d993-723">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d993-724">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2d993-724">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d993-725">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2d993-725">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d993-726">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-726">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="2d993-727">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-727">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="2d993-728">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2d993-728">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d993-729">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2d993-729">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d993-730">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2d993-730">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d993-731">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2d993-731">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d993-732">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="2d993-732">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="2d993-733">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="2d993-733">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="2d993-734">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="2d993-734">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="2d993-735">Restart-AzServiceFabricManagedNodeTyp</span><span class="sxs-lookup"><span data-stu-id="2d993-735">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="2d993-736">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2020-03-01 поставщика ресурсов Service Fabric для текущей модели и 2020-01-01-preview для управляемых кластеров.</span><span class="sxs-lookup"><span data-stu-id="2d993-736">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-737">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-737">Az.Sql</span></span>
* <span data-ttu-id="2d993-738">Добавлен параметр BackupStorageRedundancy к командлетам New-AzSqlInstance и Get-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2d993-738">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="2d993-739">Добавлен командлет Get-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="2d993-739">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d993-740">Добавлен командлет Enable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="2d993-740">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d993-741">Добавлен параметр Force к командлету New-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2d993-741">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="2d993-742">Добавлены командлеты для службы воспроизведения журнала управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-742">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="2d993-743">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="2d993-743">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="2d993-744">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="2d993-744">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="2d993-745">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="2d993-745">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="2d993-746">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="2d993-746">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="2d993-747">Добавлен командлет Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="2d993-747">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d993-748">Добавлен командлет Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="2d993-748">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d993-749">Добавлен командлет Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="2d993-749">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d993-750">Обновлены командлеты New-AzSqlDatabaseImport и New-AzSqlDatabaseExport для поддержки функциональности сетевой изоляции.</span><span class="sxs-lookup"><span data-stu-id="2d993-750">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="2d993-751">Добавлен командлет New-AzSqlDatabaseImportExisting.</span><span class="sxs-lookup"><span data-stu-id="2d993-751">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="2d993-752">Обновлены командлеты баз данных для поддержки указания типа хранилища резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2d993-752">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="2d993-753">Добавлен параметр Force к командлету New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-753">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="2d993-754">Добавлено предупреждение для конфигурации BackupStorageRedundancy в выбранных регионах в командлете New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-754">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="2d993-755">Обновлены командлеты ActiveDirectoryOnlyAuthentication для сервера и экземпляра для включения ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-755">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-756">Az.Storage</span></span>
* <span data-ttu-id="2d993-757">Исправлен сбой отправки BLOB-объекта путем обновления до Microsoft.Azure.Storage.DataMovement 2.0.0 [12220].</span><span class="sxs-lookup"><span data-stu-id="2d993-757">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="2d993-758">Реализована поддержка восстановления до точки во времени.</span><span class="sxs-lookup"><span data-stu-id="2d993-758">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="2d993-759">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-759">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d993-760">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-760">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d993-761">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="2d993-761">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="2d993-762">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="2d993-762">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="2d993-763">Реализована поддержка получения состояния восстановления BLOB-объекта путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeBlobRestoreStatus.</span><span class="sxs-lookup"><span data-stu-id="2d993-763">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="2d993-764">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-764">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="2d993-765">Добавлено важное сообщение с предупреждением о предстоящем изменении выходных данных командлета.</span><span class="sxs-lookup"><span data-stu-id="2d993-765">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="2d993-766">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-766">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="2d993-767">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-767">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="2d993-768">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-768">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d993-769">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-769">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d993-770">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2d993-770">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="2d993-771">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2d993-771">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="2d993-772">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.8.</span><span class="sxs-lookup"><span data-stu-id="2d993-772">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d993-773">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="2d993-773">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d993-774">Томас Ван Лере (Thomas Van Laere) (@ThomVanL), добавление Dockerfile-alpine-3.10 (12911).</span><span class="sxs-lookup"><span data-stu-id="2d993-774">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="2d993-775">Лохит Чаудари Чилукури (Lohith Chowdary Chilukuri) (@Lochiluk), обновление Remove-AzNetworkInterfaceIpConfig.md (12807).</span><span class="sxs-lookup"><span data-stu-id="2d993-775">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="2d993-776">Роберт Стрэнд (Roberth Strand) (@roberthstrand), Get-AzResourceGroup — новый пример и очистка (12828).</span><span class="sxs-lookup"><span data-stu-id="2d993-776">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="2d993-777">Рави Мишра (Ravi Mishra) (@inmishrar), обновление стека среды выполнения веб-приложений Azure до .NET Core (12833).</span><span class="sxs-lookup"><span data-stu-id="2d993-777">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="2d993-778">@jack-education, обновление Set-AzVirtualNetworkSubnetConfig для разрешения удаления группы безопасности сети и таблицы маршрутизации из подсети (12351).</span><span class="sxs-lookup"><span data-stu-id="2d993-778">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="2d993-779">@hagop-globanet, обновление Add-AzApplicationGatewayCustomError.md (12784).</span><span class="sxs-lookup"><span data-stu-id="2d993-779">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="2d993-780">Джошуа Ван Даален (Joshua Van Daalen) (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="2d993-780">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="2d993-781">Изменение правописания Proeprty на Property (12821)</span><span class="sxs-lookup"><span data-stu-id="2d993-781">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="2d993-782">Обновление примеров New-AzResourceLock.md (12806)</span><span class="sxs-lookup"><span data-stu-id="2d993-782">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="2d993-783">Эрагон Риддл (Eragon Riddle) (@eragonriddle), исправлено имя поля параметра в примере (12825)</span><span class="sxs-lookup"><span data-stu-id="2d993-783">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="2d993-784">@rossifumax, исправление опечатки в New-AzConfigurationAssignment.md (12701)</span><span class="sxs-lookup"><span data-stu-id="2d993-784">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="2d993-785">4.6.1 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-785">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="2d993-786">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-786">Az.Compute</span></span>
* <span data-ttu-id="2d993-787">Исправлен параметр -EncryptionAtHost в New-AzVm для удаления значения false по умолчанию [№ 12776].</span><span class="sxs-lookup"><span data-stu-id="2d993-787">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="2d993-788">4.6.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-788">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-789">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-789">Az.Accounts</span></span>
* <span data-ttu-id="2d993-790">Загружаются все общедоступные облачные среды, когда конечная точка обнаружения не возвращает AzureCloud по умолчанию или другие общедоступные среды [№ 12633]</span><span class="sxs-lookup"><span data-stu-id="2d993-790">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="2d993-791">В Get-AzSubscription предоставлен параметр SubscriptionPolicies [№ 12551].</span><span class="sxs-lookup"><span data-stu-id="2d993-791">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-792">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-792">Az.Automation</span></span>
* <span data-ttu-id="2d993-793">В Set-AzAutomationWebhook добавлен параметр -RunOn для определения группы гибридной рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="2d993-793">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-794">Az.Compute</span></span>
* <span data-ttu-id="2d993-795">В New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр -EncryptionAtHost.</span><span class="sxs-lookup"><span data-stu-id="2d993-795">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="2d993-796">В возвращаемый объект Get-AzVM и Get-AzVmss добавлен параметр SecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="2d993-796">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="2d993-797">В Get-AzHostGroup добавлен необязательный параметр -InstanceView.</span><span class="sxs-lookup"><span data-stu-id="2d993-797">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="2d993-798">Добавлен новый командлет Invoke-AzVmPatchAssessment.</span><span class="sxs-lookup"><span data-stu-id="2d993-798">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-799">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-800">В класс PSPipelineRun добавлены отсутствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2d993-800">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-801">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-801">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-802">Включена поддержка создания кластера с функцией шифрования на узле.</span><span class="sxs-lookup"><span data-stu-id="2d993-802">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-803">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-803">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-804">Добавлены предупреждающие сообщения для планирования отключения обратимого удаления.</span><span class="sxs-lookup"><span data-stu-id="2d993-804">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="2d993-805">Добавлены предупреждающие сообщения для планирования удаления атрибута SecretValueText.</span><span class="sxs-lookup"><span data-stu-id="2d993-805">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="2d993-806">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="2d993-806">Az.Maintenance</span></span>
* <span data-ttu-id="2d993-807">В New-AzMaintenanceConfiguration добавлены дополнительные поля, связанные с расписанием.</span><span class="sxs-lookup"><span data-stu-id="2d993-807">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="2d993-808">Добавлен новый командлет для Get-AzMaintenancePublicConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-808">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d993-809">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d993-809">Az.ManagedServices</span></span>
* <span data-ttu-id="2d993-810">Добавлены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="2d993-810">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-811">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-811">Az.Monitor</span></span>
* <span data-ttu-id="2d993-812">Расширен набор параметров, заданный в Set-AzDiagnosticSetting, для разделения включения журналов и метрик [№ 12482].</span><span class="sxs-lookup"><span data-stu-id="2d993-812">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="2d993-813">Для Add-AzMetricAlertRuleV2 исправлена ошибка, возникающая при получении оповещения метрики из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2d993-813">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-814">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-814">Az.Resources</span></span>
* <span data-ttu-id="2d993-815">Изменен ответ Get-AzPolicyAlias для включения сведений о том, изменяется ли этот псевдоним Политикой Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-815">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="2d993-816">Создан новый командлет Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="2d993-816">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="2d993-817">Добавлен командлет Get-AzDeploymentManagementGroupWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области группы управления.</span><span class="sxs-lookup"><span data-stu-id="2d993-817">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="2d993-818">Добавлен командлет Get-AzTenantWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области арендатора.</span><span class="sxs-lookup"><span data-stu-id="2d993-818">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="2d993-819">Переопределены параметры -WhatIf и -Confirm для New-AzManagementGroupDeployment и New-AzTenantDeployment для использования результатов выполнения What-If в шаблоне ARM.</span><span class="sxs-lookup"><span data-stu-id="2d993-819">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="2d993-820">Исправлено поведение параметров -WhatIf и -Confirm для новых командлетов развертывания, чтобы они соответствовали значению False.</span><span class="sxs-lookup"><span data-stu-id="2d993-820">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="2d993-821">Исправлена ошибка сериализации для -TemplateObject и TemplateParameterObject [№ 1528] [№ 6292].</span><span class="sxs-lookup"><span data-stu-id="2d993-821">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="2d993-822">Добавлен атрибут критического изменения в Get-AzResourceGroupDeploymentOperation для предстоящего изменения типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-822">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d993-823">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d993-823">Az.SignalR</span></span>
* <span data-ttu-id="2d993-824">Исправлены ошибки файлов справки Restart-AzSignalR и Update-AzSignalR.</span><span class="sxs-lookup"><span data-stu-id="2d993-824">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="2d993-825">Добавлены командлеты Update-AzSignalRNetworkAcl, Set-AzSignalRUpstream.</span><span class="sxs-lookup"><span data-stu-id="2d993-825">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-826">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-826">Az.Storage</span></span>
* <span data-ttu-id="2d993-827">Поддерживается ускорение запросов больших двоичных объектов:</span><span class="sxs-lookup"><span data-stu-id="2d993-827">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="2d993-828">Get-AzStorageBlobQueryResult;</span><span class="sxs-lookup"><span data-stu-id="2d993-828">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="2d993-829">New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-829">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="2d993-830">Обновлен файл справки; дополнено описание и исправлена опечатка.</span><span class="sxs-lookup"><span data-stu-id="2d993-830">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="2d993-831">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-831">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="2d993-832">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2d993-832">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="2d993-833">Исправлена ошибка, из-за которой работа большого двоичного объекта завершается ошибкой, если связанный подкаталог не существует [№ 12592].</span><span class="sxs-lookup"><span data-stu-id="2d993-833">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="2d993-834">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-834">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="2d993-835">Включена поддержка задания, получения и удаления политики репликации объекта в учетных записях хранения:</span><span class="sxs-lookup"><span data-stu-id="2d993-835">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="2d993-836">New-AzStorageObjectReplicationPolicyRule;</span><span class="sxs-lookup"><span data-stu-id="2d993-836">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="2d993-837">Set-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="2d993-837">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="2d993-838">Get-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="2d993-838">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="2d993-839">Remove-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-839">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="2d993-840">Включена поддержка включения и отключения канала изменений в службе BLOB-объектов учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="2d993-840">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="2d993-841">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-841">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="2d993-842">4.5.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-842">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-843">Az.Accounts</span></span>
* <span data-ttu-id="2d993-844">Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).</span><span class="sxs-lookup"><span data-stu-id="2d993-844">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="2d993-845">Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).</span><span class="sxs-lookup"><span data-stu-id="2d993-845">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="2d993-846">Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-846">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="2d993-847">Исправлено имя модуля и сведения о версии в данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="2d993-847">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="2d993-848">Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.</span><span class="sxs-lookup"><span data-stu-id="2d993-848">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-849">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-849">Az.Aks</span></span>
* <span data-ttu-id="2d993-850">Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).</span><span class="sxs-lookup"><span data-stu-id="2d993-850">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="2d993-851">Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).</span><span class="sxs-lookup"><span data-stu-id="2d993-851">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-852">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-852">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-853">Добавлен новый командлет Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-853">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="2d993-854">Добавлен новый командлет Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-854">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d993-855">Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-855">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="2d993-856">Добавлен новый командлет Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="2d993-856">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="2d993-857">Добавлен новый командлет New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-857">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d993-858">Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-858">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="2d993-859">Добавлен новый командлет New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-859">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="2d993-860">Добавлен новый командлет Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-860">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="2d993-861">Добавлен новый командлет Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-861">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d993-862">Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-862">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="2d993-863">Добавлен новый командлет Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-863">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d993-864">Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="2d993-864">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-865">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-866">Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d993-866">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-867">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-867">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-868">Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).</span><span class="sxs-lookup"><span data-stu-id="2d993-868">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-869">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-869">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-870">Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-870">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="2d993-871">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-871">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="2d993-872">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-872">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="2d993-873">Добавлена поддержка создания кластера с функцией приватного канала:</span><span class="sxs-lookup"><span data-stu-id="2d993-873">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="2d993-874">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-874">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="2d993-875">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-875">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="2d993-876">Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-876">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-877">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-877">Az.Network</span></span>
* <span data-ttu-id="2d993-878">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-878">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="2d993-879">Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-879">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="2d993-880">Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="2d993-880">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="2d993-881">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="2d993-881">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-882">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-882">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-883">Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.</span><span class="sxs-lookup"><span data-stu-id="2d993-883">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="2d993-884">Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2d993-884">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="2d993-885">Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2d993-885">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-887">Улучшена работа с обнаружением контейнеров и элементов Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="2d993-887">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-888">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-888">Az.Resources</span></span>
* <span data-ttu-id="2d993-889">Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="2d993-889">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="2d993-890">Это касается всех соответствующих изменений моделей данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-890">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-891">Az.Sql</span></span>
* <span data-ttu-id="2d993-892">Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="2d993-892">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="2d993-893">Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="2d993-893">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-894">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-894">Az.Storage</span></span>
* <span data-ttu-id="2d993-895">Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="2d993-895">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="2d993-896">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d993-896">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="2d993-897">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2d993-897">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="2d993-898">Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.</span><span class="sxs-lookup"><span data-stu-id="2d993-898">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="2d993-899">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="2d993-899">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="2d993-900">Добавлена поддержка получения данных об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="2d993-900">Supported get single file share usage</span></span>
    - <span data-ttu-id="2d993-901">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d993-901">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="2d993-902">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-902">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-903">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-903">Az.Accounts</span></span>
* <span data-ttu-id="2d993-904">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="2d993-904">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="2d993-905">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="2d993-905">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-906">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-906">Az.Aks</span></span>
* <span data-ttu-id="2d993-907">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="2d993-907">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d993-908">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d993-908">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d993-909">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2d993-909">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-910">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-910">Az.Automation</span></span>
* <span data-ttu-id="2d993-911">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="2d993-911">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-912">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-912">Az.Compute</span></span>
* <span data-ttu-id="2d993-913">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="2d993-913">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-914">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-914">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-915">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-915">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d993-916">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d993-916">Az.EventGrid</span></span>
* <span data-ttu-id="2d993-917">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-917">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="2d993-918">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="2d993-918">Added new features:</span></span>
    - <span data-ttu-id="2d993-919">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="2d993-919">Input mapping</span></span>
    - <span data-ttu-id="2d993-920">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="2d993-920">Event Delivery Schema</span></span>
    - <span data-ttu-id="2d993-921">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="2d993-921">Private Link</span></span>
    - <span data-ttu-id="2d993-922">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="2d993-922">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="2d993-923">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="2d993-923">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="2d993-924">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="2d993-924">Azure Function As Destination</span></span>
    - <span data-ttu-id="2d993-925">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="2d993-925">WebHook Batching</span></span>
    - <span data-ttu-id="2d993-926">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="2d993-926">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="2d993-927">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d993-927">IpFiltering</span></span>
* <span data-ttu-id="2d993-928">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-928">Updated cmdlets:</span></span>
    - <span data-ttu-id="2d993-929">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2d993-929">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="2d993-930">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="2d993-930">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="2d993-931">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="2d993-931">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="2d993-932">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="2d993-932">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="2d993-933">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="2d993-933">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="2d993-934">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="2d993-934">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="2d993-935">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d993-935">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="2d993-936">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="2d993-936">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="2d993-937">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-937">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-938">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-938">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-939">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-939">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="2d993-940">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="2d993-940">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-941">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-941">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-942">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="2d993-942">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-943">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-943">Az.Monitor</span></span>
* <span data-ttu-id="2d993-944">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="2d993-944">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-945">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-945">Az.Network</span></span>
* <span data-ttu-id="2d993-946">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-946">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="2d993-947">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-947">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="2d993-948">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2d993-948">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d993-949">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2d993-949">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d993-950">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2d993-950">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d993-951">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2d993-951">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d993-952">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-952">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="2d993-953">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-953">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="2d993-954">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="2d993-954">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d993-955">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="2d993-955">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d993-956">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="2d993-956">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d993-957">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="2d993-957">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d993-958">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="2d993-958">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="2d993-959">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-959">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="2d993-960">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="2d993-960">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="2d993-961">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="2d993-961">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="2d993-962">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="2d993-962">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-963">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-963">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-964">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2d993-964">Removed project reference to Authentication</span></span>
* <span data-ttu-id="2d993-965">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="2d993-965">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="2d993-966">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="2d993-966">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-967">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-967">Az.Resources</span></span>
* <span data-ttu-id="2d993-968">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-968">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="2d993-969">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="2d993-969">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-970">Az.Sql</span></span>
* <span data-ttu-id="2d993-971">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="2d993-971">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="2d993-972">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-972">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="2d993-973">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="2d993-973">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-974">Az.Storage</span></span>
* <span data-ttu-id="2d993-975">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="2d993-975">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="2d993-976">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="2d993-976">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="2d993-977">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-977">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="2d993-978">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d993-979">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-979">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="2d993-980">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-980">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="2d993-981">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="2d993-981">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="2d993-982">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2d993-982">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="2d993-983">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="2d993-983">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="2d993-984">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2d993-984">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="2d993-985">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2d993-985">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="2d993-986">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="2d993-986">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="2d993-987">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-987">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="2d993-988">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d993-988">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="2d993-989">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2d993-989">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="2d993-990">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-990">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="2d993-991">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-991">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d993-992">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d993-992">Az.StorageSync</span></span>
* <span data-ttu-id="2d993-993">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-993">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="2d993-994">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="2d993-994">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="2d993-995">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2d993-995">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="2d993-996">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="2d993-996">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-997">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-997">Az.Websites</span></span>
* <span data-ttu-id="2d993-998">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="2d993-998">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="2d993-999">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="2d993-999">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-1000">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1000">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1001">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1001">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="2d993-1002">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="2d993-1002">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="2d993-1003">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="2d993-1003">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="2d993-1004">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="2d993-1004">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-1005">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-1005">Az.Aks</span></span>
* <span data-ttu-id="2d993-1006">Заменено использование старого [API AccessProfile](/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="2d993-1006">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d993-1007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-1007">Az.Batch</span></span>
* <span data-ttu-id="2d993-1008">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1008">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="2d993-1009">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="2d993-1009">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-1010">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1010">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-1011">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2d993-1011">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="2d993-1012">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="2d993-1012">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1013">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1013">Az.Compute</span></span>
* <span data-ttu-id="2d993-1014">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1014">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="2d993-1015">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-1015">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="2d993-1016">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="2d993-1016">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="2d993-1017">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-1017">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="2d993-1018">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="2d993-1018">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1019">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1020">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1020">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-1021">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1021">Az.EventHub</span></span>
* <span data-ttu-id="2d993-1022">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="2d993-1022">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d993-1023">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d993-1023">Az.Functions</span></span>
* <span data-ttu-id="2d993-1024">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="2d993-1024">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-1025">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-1025">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-1026">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d993-1026">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d993-1027">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d993-1027">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d993-1028">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1028">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="2d993-1029">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1029">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-1030">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1030">Az.Monitor</span></span>
* <span data-ttu-id="2d993-1031">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="2d993-1031">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="2d993-1032">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="2d993-1032">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1033">Az.Network</span></span>
* <span data-ttu-id="2d993-1034">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-1034">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="2d993-1035">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1035">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="2d993-1036">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="2d993-1036">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="2d993-1037">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2d993-1037">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="2d993-1038">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="2d993-1038">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="2d993-1039">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-1039">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="2d993-1040">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2d993-1040">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="2d993-1041">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2d993-1041">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="2d993-1042">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2d993-1042">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="2d993-1043">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2d993-1043">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="2d993-1044">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1044">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="2d993-1045">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1045">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="2d993-1046">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2d993-1046">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="2d993-1047">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-1047">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="2d993-1048">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="2d993-1048">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="2d993-1049">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="2d993-1049">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="2d993-1050">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="2d993-1050">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="2d993-1051">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="2d993-1051">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="2d993-1052">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="2d993-1052">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="2d993-1053">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="2d993-1053">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="2d993-1054">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="2d993-1054">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="2d993-1055">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="2d993-1055">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="2d993-1056">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="2d993-1056">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="2d993-1057">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="2d993-1057">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="2d993-1058">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="2d993-1058">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="2d993-1059">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="2d993-1059">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="2d993-1060">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="2d993-1060">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="2d993-1061">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="2d993-1061">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="2d993-1062">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1062">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d993-1063">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1063">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d993-1064">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1064">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d993-1065">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1065">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d993-1066">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1066">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d993-1067">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1067">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="2d993-1068">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="2d993-1068">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="2d993-1069">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="2d993-1069">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="2d993-1070">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-1070">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="2d993-1071">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-1071">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="2d993-1072">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-1072">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="2d993-1073">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-1073">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="2d993-1074">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-1074">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="2d993-1075">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1075">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="2d993-1076">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1076">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="2d993-1077">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1077">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d993-1078">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1078">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d993-1079">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1079">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="2d993-1080">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1080">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="2d993-1081">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-1081">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="2d993-1082">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-1082">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-1083">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1083">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-1084">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="2d993-1084">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="2d993-1085">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2d993-1085">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="2d993-1086">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="2d993-1086">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="2d993-1087">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2d993-1087">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="2d993-1088">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2d993-1088">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1089">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1089">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1090">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1090">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="2d993-1091">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d993-1091">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1092">Az.Resources</span></span>
* <span data-ttu-id="2d993-1093">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="2d993-1093">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="2d993-1094">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="2d993-1094">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="2d993-1095">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="2d993-1095">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="2d993-1096">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1096">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="2d993-1097">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2d993-1097">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="2d993-1098">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="2d993-1098">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1099">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1099">Az.Sql</span></span>
* <span data-ttu-id="2d993-1100">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2d993-1100">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="2d993-1101">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1101">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="2d993-1102">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="2d993-1102">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1103">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1103">Az.Storage</span></span>
* <span data-ttu-id="2d993-1104">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="2d993-1104">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="2d993-1105">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-1105">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="2d993-1106">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2d993-1106">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-1107">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-1107">Az.Websites</span></span>
* <span data-ttu-id="2d993-1108">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="2d993-1108">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2d993-1109">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="2d993-1109">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="2d993-1110">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="2d993-1110">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="2d993-1111">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="2d993-1111">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="2d993-1112">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="2d993-1112">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="2d993-1113">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1113">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="2d993-1114">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1114">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-1115">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1115">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1116">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="2d993-1116">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d993-1117">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1117">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d993-1118">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1118">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-1119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-1119">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-1120">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="2d993-1120">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="2d993-1121">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d993-1121">Az.Billing</span></span>
* <span data-ttu-id="2d993-1122">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="2d993-1122">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-1123">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1123">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-1124">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="2d993-1124">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1125">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1126">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="2d993-1126">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="2d993-1127">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="2d993-1127">Az.DataShare</span></span>
* <span data-ttu-id="2d993-1128">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="2d993-1128">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="2d993-1129">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="2d993-1129">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="2d993-1130">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="2d993-1130">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-1131">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1131">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-1132">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1132">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="2d993-1133">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1133">Added optional parameters to</span></span> 
    - <span data-ttu-id="2d993-1134">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2d993-1134">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="2d993-1135">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2d993-1135">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-1136">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1136">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-1137">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="2d993-1137">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2d993-1138">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d993-1138">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d993-1139">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="2d993-1139">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="2d993-1140">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="2d993-1140">Az.PrivateDns</span></span>
* <span data-ttu-id="2d993-1141">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-1141">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1143">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="2d993-1143">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="2d993-1144">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1144">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1145">Az.Resources</span></span>
* <span data-ttu-id="2d993-1146">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="2d993-1146">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="2d993-1147">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="2d993-1147">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="2d993-1148">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-1148">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="2d993-1149">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1149">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="2d993-1150">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1150">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1151">Az.Sql</span></span>
* <span data-ttu-id="2d993-1152">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="2d993-1152">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="2d993-1153">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="2d993-1153">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="2d993-1154">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1154">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1155">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1155">Az.Storage</span></span>
* <span data-ttu-id="2d993-1156">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1156">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="2d993-1157">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1157">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="2d993-1158">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-1158">Highlights since the last release</span></span>
* <span data-ttu-id="2d993-1159">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="2d993-1159">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="2d993-1160">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="2d993-1160">General availability of Az.Functions</span></span> 
* <span data-ttu-id="2d993-1161">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="2d993-1161">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-1162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1162">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1163">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="2d993-1163">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="2d993-1164">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="2d993-1164">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-1165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-1165">Az.Aks</span></span>
* <span data-ttu-id="2d993-1166">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-1166">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="2d993-1167">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2d993-1167">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="2d993-1168">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-1168">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-1169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-1169">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-1170">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="2d993-1170">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="2d993-1171">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="2d993-1171">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="2d993-1172">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="2d993-1172">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d993-1173">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1173">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="2d993-1174">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="2d993-1174">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d993-1175">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1175">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="2d993-1176">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="2d993-1176">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d993-1177">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1177">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="2d993-1178">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="2d993-1178">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d993-1179">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1179">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="2d993-1180">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="2d993-1180">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="2d993-1181">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="2d993-1181">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="2d993-1182">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="2d993-1182">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="2d993-1183">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1183">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="2d993-1184">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="2d993-1184">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="2d993-1185">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="2d993-1185">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2d993-1186">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1186">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2d993-1187">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="2d993-1187">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="2d993-1188">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2d993-1188">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="2d993-1189">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1189">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d993-1190">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-1190">Az.Batch</span></span>
* <span data-ttu-id="2d993-1191">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1191">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="2d993-1192">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="2d993-1192">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="2d993-1193">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="2d993-1193">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="2d993-1194">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="2d993-1194">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="2d993-1195">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="2d993-1195">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="2d993-1196">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1196">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="2d993-1197">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-1197">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="2d993-1198">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-1198">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="2d993-1199">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="2d993-1199">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1200">Az.Compute</span></span>
* <span data-ttu-id="2d993-1201">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1201">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="2d993-1202">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="2d993-1202">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="2d993-1203">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="2d993-1203">Breaking changes</span></span>
    - <span data-ttu-id="2d993-1204">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="2d993-1204">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="2d993-1205">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1205">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="2d993-1206">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-1206">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="2d993-1207">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1207">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="2d993-1208">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-1208">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="2d993-1209">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="2d993-1209">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="2d993-1210">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1210">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1211">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1212">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2d993-1212">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-1213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-1213">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-1214">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="2d993-1214">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="2d993-1215">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="2d993-1215">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="2d993-1216">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="2d993-1216">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="2d993-1217">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="2d993-1217">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d993-1218">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d993-1218">Az.Functions</span></span>
* <span data-ttu-id="2d993-1219">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="2d993-1219">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-1220">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-1220">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-1221">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1221">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d993-1222">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d993-1222">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d993-1223">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d993-1223">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-1224">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1224">Az.IotHub</span></span>
* <span data-ttu-id="2d993-1225">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="2d993-1225">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="2d993-1226">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="2d993-1226">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="2d993-1227">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="2d993-1227">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="2d993-1228">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2d993-1228">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="2d993-1229">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="2d993-1229">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="2d993-1230">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1230">New cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1231">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="2d993-1231">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="2d993-1232">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="2d993-1232">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="2d993-1233">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="2d993-1233">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="2d993-1234">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1234">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="2d993-1235">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1235">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="2d993-1236">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="2d993-1236">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-1237">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-1237">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-1238">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="2d993-1238">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="2d993-1239">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d993-1239">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="2d993-1240">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="2d993-1240">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="2d993-1241">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="2d993-1241">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="2d993-1242">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="2d993-1242">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="2d993-1243">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1243">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="2d993-1244">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="2d993-1244">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-1245">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1245">Az.Monitor</span></span>
* <span data-ttu-id="2d993-1246">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="2d993-1246">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="2d993-1247">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="2d993-1247">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="2d993-1248">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="2d993-1248">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="2d993-1249">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="2d993-1249">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="2d993-1250">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="2d993-1250">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="2d993-1251">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="2d993-1251">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="2d993-1252">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="2d993-1252">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1253">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1253">Az.Network</span></span>
* <span data-ttu-id="2d993-1254">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="2d993-1254">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="2d993-1255">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="2d993-1255">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="2d993-1256">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="2d993-1256">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="2d993-1257">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-1257">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="2d993-1258">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="2d993-1258">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="2d993-1259">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1259">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-1260">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="2d993-1260">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="2d993-1261">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="2d993-1261">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="2d993-1262">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="2d993-1262">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="2d993-1263">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="2d993-1263">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="2d993-1264">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1264">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="2d993-1265">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-1265">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="2d993-1266">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="2d993-1266">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="2d993-1267">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="2d993-1267">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="2d993-1268">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="2d993-1268">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="2d993-1269">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1269">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="2d993-1270">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="2d993-1270">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="2d993-1271">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="2d993-1271">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="2d993-1272">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="2d993-1272">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="2d993-1273">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="2d993-1273">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="2d993-1274">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1274">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="2d993-1275">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="2d993-1275">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="2d993-1276">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="2d993-1276">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="2d993-1277">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2d993-1277">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d993-1278">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="2d993-1278">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-1279">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1279">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-1280">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-1280">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="2d993-1281">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1281">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="2d993-1282">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="2d993-1282">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="2d993-1283">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="2d993-1283">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="2d993-1284">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="2d993-1284">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="2d993-1285">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="2d993-1285">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="2d993-1286">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1286">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="2d993-1287">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="2d993-1287">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1288">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1289">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="2d993-1289">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="2d993-1290">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="2d993-1290">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="2d993-1291">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1291">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="2d993-1292">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1292">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="2d993-1293">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d993-1293">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1294">Az.Resources</span></span>
* <span data-ttu-id="2d993-1295">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="2d993-1295">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="2d993-1296">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="2d993-1296">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="2d993-1297">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="2d993-1297">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="2d993-1298">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="2d993-1298">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="2d993-1299">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="2d993-1299">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="2d993-1300">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="2d993-1300">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="2d993-1301">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="2d993-1301">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="2d993-1302">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1302">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="2d993-1303">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-1303">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="2d993-1304">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="2d993-1304">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="2d993-1305">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="2d993-1305">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="2d993-1306">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="2d993-1306">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="2d993-1307">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="2d993-1307">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="2d993-1308">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="2d993-1308">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="2d993-1309">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="2d993-1309">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="2d993-1310">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-1310">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="2d993-1311">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="2d993-1311">'New-AzDeployment'</span></span>
    - <span data-ttu-id="2d993-1312">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="2d993-1312">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="2d993-1313">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="2d993-1313">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2d993-1314">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1314">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-1315">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-1315">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-1316">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="2d993-1316">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1317">Az.Sql</span></span>
* <span data-ttu-id="2d993-1318">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-1318">Enhance performance of:</span></span>
    - <span data-ttu-id="2d993-1319">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="2d993-1319">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d993-1320">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="2d993-1320">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d993-1321">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="2d993-1321">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d993-1322">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="2d993-1322">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d993-1323">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="2d993-1323">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="2d993-1324">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="2d993-1324">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="2d993-1325">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="2d993-1325">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="2d993-1326">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="2d993-1326">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="2d993-1327">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-1327">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="2d993-1328">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="2d993-1328">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1329">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1329">Az.Storage</span></span>
* <span data-ttu-id="2d993-1330">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="2d993-1330">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="2d993-1331">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="2d993-1331">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="2d993-1332">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-1332">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d993-1333">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="2d993-1333">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="2d993-1334">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="2d993-1334">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="2d993-1335">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="2d993-1335">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="2d993-1336">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="2d993-1336">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="2d993-1337">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-1337">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="2d993-1338">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="2d993-1338">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="2d993-1339">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="2d993-1339">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="2d993-1340">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="2d993-1340">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="2d993-1341">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1341">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="2d993-1342">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="2d993-1342">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="2d993-1343">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1343">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="2d993-1344">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-1344">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="2d993-1345">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-1345">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d993-1346">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1346">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="2d993-1347">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="2d993-1347">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="2d993-1348">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="2d993-1348">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2d993-1349">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1349">Supported failover Storage account</span></span>
    - <span data-ttu-id="2d993-1350">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="2d993-1350">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="2d993-1351">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="2d993-1351">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="2d993-1352">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="2d993-1352">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="2d993-1353">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1353">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="2d993-1354">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1354">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="2d993-1355">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="2d993-1355">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="2d993-1356">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="2d993-1356">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="2d993-1357">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="2d993-1357">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="2d993-1358">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="2d993-1358">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="2d993-1359">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="2d993-1359">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="2d993-1360">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1360">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="2d993-1361">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="2d993-1361">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="2d993-1362">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="2d993-1362">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="2d993-1363">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1363">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="2d993-1364">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2d993-1364">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="2d993-1365">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2d993-1365">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="2d993-1366">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2d993-1366">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="2d993-1367">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1367">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="2d993-1368">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="2d993-1368">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2d993-1369">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d993-1369">Az.TrafficManager</span></span>
* <span data-ttu-id="2d993-1370">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2d993-1370">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-1371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-1371">Az.Websites</span></span>
* <span data-ttu-id="2d993-1372">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-1372">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="2d993-1373">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1373">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="2d993-1374">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-1374">Highlights since the last release</span></span>
* <span data-ttu-id="2d993-1375">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="2d993-1375">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-1376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1376">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1377">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="2d993-1377">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-1378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-1378">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-1379">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="2d993-1379">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="2d993-1380">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1380">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-1381">Az.Cdn</span></span>
* <span data-ttu-id="2d993-1382">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="2d993-1382">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-1384">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="2d993-1384">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1385">Az.Compute</span></span>
* <span data-ttu-id="2d993-1386">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="2d993-1386">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="2d993-1387">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="2d993-1387">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-1388">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1388">Az.IotHub</span></span>
* <span data-ttu-id="2d993-1389">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1389">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1390">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="2d993-1390">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="2d993-1391">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="2d993-1391">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="2d993-1392">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1392">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="2d993-1393">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1393">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1394">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="2d993-1394">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="2d993-1395">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="2d993-1395">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="2d993-1396">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="2d993-1396">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="2d993-1397">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1397">New cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1398">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1398">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="2d993-1399">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1399">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="2d993-1400">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1400">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="2d993-1401">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1401">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="2d993-1402">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1402">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-1403">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-1403">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-1404">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="2d993-1404">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="2d993-1405">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="2d993-1405">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="2d993-1406">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="2d993-1406">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="2d993-1407">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1407">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="2d993-1408">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="2d993-1408">Az.Maintenance</span></span>
* <span data-ttu-id="2d993-1409">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="2d993-1409">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-1410">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1410">Az.Monitor</span></span>
* <span data-ttu-id="2d993-1411">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="2d993-1411">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="2d993-1412">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="2d993-1412">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d993-1413">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="2d993-1413">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d993-1414">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="2d993-1414">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d993-1415">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="2d993-1415">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d993-1416">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2d993-1416">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="2d993-1417">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2d993-1417">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="2d993-1418">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2d993-1418">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1419">Az.Network</span></span>
* <span data-ttu-id="2d993-1420">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="2d993-1420">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="2d993-1421">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-1421">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="2d993-1422">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-1422">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="2d993-1423">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1423">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="2d993-1424">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1424">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="2d993-1425">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="2d993-1425">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="2d993-1426">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-1426">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="2d993-1427">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2d993-1427">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="2d993-1428">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="2d993-1428">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="2d993-1429">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-1429">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="2d993-1430">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="2d993-1430">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="2d993-1431">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-1431">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="2d993-1432">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="2d993-1432">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="2d993-1433">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1433">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="2d993-1434">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="2d993-1434">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="2d993-1435">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-1435">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-1436">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1436">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-1437">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="2d993-1437">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="2d993-1438">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2d993-1438">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-1439">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-1439">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-1440">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-1440">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1441">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1441">Az.Sql</span></span>
* <span data-ttu-id="2d993-1442">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="2d993-1442">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="2d993-1443">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-1443">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1444">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1444">Az.Storage</span></span>
* <span data-ttu-id="2d993-1445">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="2d993-1445">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="2d993-1446">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1446">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="2d993-1447">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-1447">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="2d993-1448">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-1448">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d993-1449">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1449">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="2d993-1450">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2d993-1450">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d993-1451">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2d993-1451">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d993-1452">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="2d993-1452">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="2d993-1453">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2d993-1453">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d993-1454">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="2d993-1454">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="2d993-1455">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2d993-1455">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d993-1456">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="2d993-1456">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="2d993-1457">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2d993-1457">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="2d993-1458">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1458">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="2d993-1459">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-1459">General</span></span>
* <span data-ttu-id="2d993-1460">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="2d993-1460">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="2d993-1461">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="2d993-1461">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="2d993-1462">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](/azure-stack/operator/powershell-install-az-module))</span><span class="sxs-lookup"><span data-stu-id="2d993-1462">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="2d993-1463">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="2d993-1463">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="2d993-1464">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d993-1464">Az.Billing</span></span>
  - <span data-ttu-id="2d993-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1465">Az.Compute</span></span>
  - <span data-ttu-id="2d993-1466">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d993-1466">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="2d993-1467">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1467">Az.EventHub</span></span>
  - <span data-ttu-id="2d993-1468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1468">Az.IotHub</span></span>
  - <span data-ttu-id="2d993-1469">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-1469">Az.KeyVault</span></span>
  - <span data-ttu-id="2d993-1470">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1470">Az.Monitor</span></span>
  - <span data-ttu-id="2d993-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1471">Az.Network</span></span>
  - <span data-ttu-id="2d993-1472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1472">Az.Resources</span></span>
  - <span data-ttu-id="2d993-1473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1473">Az.Storage</span></span>
  - <span data-ttu-id="2d993-1474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-1474">Az.Websites</span></span>
* <span data-ttu-id="2d993-1475">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="2d993-1475">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="2d993-1476">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="2d993-1476">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="2d993-1477">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="2d993-1477">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="2d993-1478">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1478">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-1479">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1479">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1480">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="2d993-1480">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1481">Az.Compute</span></span>
* <span data-ttu-id="2d993-1482">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="2d993-1482">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="2d993-1483">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="2d993-1483">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="2d993-1484">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-1484">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="2d993-1485">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="2d993-1485">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="2d993-1486">[11354]</span><span class="sxs-lookup"><span data-stu-id="2d993-1486">[#11354]</span></span>
* <span data-ttu-id="2d993-1487">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="2d993-1487">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="2d993-1488">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2d993-1488">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="2d993-1489">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2d993-1489">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="2d993-1490">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2d993-1490">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="2d993-1491">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2d993-1491">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="2d993-1492">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="2d993-1492">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="2d993-1493">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d993-1493">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="2d993-1494">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="2d993-1494">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="2d993-1495">[11257]</span><span class="sxs-lookup"><span data-stu-id="2d993-1495">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1496">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1496">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1497">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1497">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="2d993-1498">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="2d993-1498">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-1499">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-1499">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-1500">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="2d993-1500">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="2d993-1501">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="2d993-1501">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-1502">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-1502">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-1503">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="2d993-1503">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-1504">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1504">Az.IotHub</span></span>
* <span data-ttu-id="2d993-1505">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="2d993-1505">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="2d993-1506">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="2d993-1506">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1507">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="2d993-1507">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="2d993-1508">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="2d993-1508">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-1509">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-1510">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d993-1510">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-1511">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1511">Az.Monitor</span></span>
* <span data-ttu-id="2d993-1512">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="2d993-1512">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1513">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1513">Az.Network</span></span>
* <span data-ttu-id="2d993-1514">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="2d993-1514">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="2d993-1515">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1515">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d993-1516">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-1516">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d993-1517">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1517">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="2d993-1518">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1518">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="2d993-1519">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-1519">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-1520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1520">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-1521">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2d993-1521">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1523">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1523">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="2d993-1524">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d993-1524">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="2d993-1525">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="2d993-1525">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="2d993-1526">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d993-1526">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="2d993-1527">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="2d993-1527">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="2d993-1528">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1528">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1529">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1529">Az.Resources</span></span>
* <span data-ttu-id="2d993-1530">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="2d993-1530">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="2d993-1531">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="2d993-1531">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="2d993-1532">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="2d993-1532">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="2d993-1533">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="2d993-1533">Added example.</span></span>
* <span data-ttu-id="2d993-1534">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="2d993-1534">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="2d993-1535">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="2d993-1535">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1536">Az.Sql</span></span>
* <span data-ttu-id="2d993-1537">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="2d993-1537">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="2d993-1538">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="2d993-1538">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d993-1539">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1539">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="2d993-1540">Az.Support</span><span class="sxs-lookup"><span data-stu-id="2d993-1540">Az.Support</span></span>
* <span data-ttu-id="2d993-1541">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="2d993-1541">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-1542">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-1542">Az.Websites</span></span>
* <span data-ttu-id="2d993-1543">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-1543">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="2d993-1544">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2d993-1544">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="2d993-1545">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2d993-1545">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="2d993-1546">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2d993-1546">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="2d993-1547">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2d993-1547">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="2d993-1548">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1548">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-1549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1549">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1550">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="2d993-1550">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="2d993-1551">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="2d993-1551">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="2d993-1552">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="2d993-1552">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-1553">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-1553">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-1554">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="2d993-1554">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="2d993-1555">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="2d993-1555">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="2d993-1556">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="2d993-1556">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="2d993-1557">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="2d993-1557">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-1559">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="2d993-1559">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-1560">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1560">Az.IotHub</span></span>
* <span data-ttu-id="2d993-1561">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1561">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2d993-1562">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="2d993-1562">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1563">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1563">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d993-1564">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1564">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d993-1565">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1565">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d993-1566">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1566">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="2d993-1567">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1567">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="2d993-1568">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="2d993-1568">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1569">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="2d993-1569">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d993-1570">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="2d993-1570">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d993-1571">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="2d993-1571">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d993-1572">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="2d993-1572">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="2d993-1573">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1573">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2d993-1574">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1574">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2d993-1575">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1575">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="2d993-1576">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="2d993-1576">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1577">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="2d993-1577">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="2d993-1578">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="2d993-1578">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="2d993-1579">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="2d993-1579">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-1580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1580">Az.Monitor</span></span>
* <span data-ttu-id="2d993-1581">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="2d993-1581">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1582">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1582">Az.Network</span></span>
* <span data-ttu-id="2d993-1583">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-1583">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="2d993-1584">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="2d993-1584">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="2d993-1585">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="2d993-1585">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="2d993-1586">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="2d993-1586">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1587">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1587">Az.Resources</span></span>
* <span data-ttu-id="2d993-1588">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1588">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="2d993-1589">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="2d993-1589">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="2d993-1590">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="2d993-1590">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="2d993-1591">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="2d993-1591">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="2d993-1592">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="2d993-1592">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="2d993-1593">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="2d993-1593">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="2d993-1594">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="2d993-1594">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="2d993-1595">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1595">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="2d993-1596">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d993-1596">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2d993-1597">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d993-1597">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2d993-1598">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d993-1598">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="2d993-1599">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="2d993-1599">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="2d993-1600">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d993-1600">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="2d993-1601">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1601">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1602">Az.Sql</span></span>
* <span data-ttu-id="2d993-1603">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="2d993-1603">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="2d993-1604">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1604">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="2d993-1605">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1605">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="2d993-1606">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="2d993-1606">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="2d993-1607">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="2d993-1607">Remove an LTR backup</span></span>
    - <span data-ttu-id="2d993-1608">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1608">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="2d993-1609">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="2d993-1609">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="2d993-1610">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2d993-1610">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="2d993-1611">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="2d993-1611">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1612">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1612">Az.Storage</span></span>
* <span data-ttu-id="2d993-1613">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-1613">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="2d993-1614">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-1614">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="2d993-1615">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="2d993-1615">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="2d993-1616">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2d993-1616">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="2d993-1617">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2d993-1617">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-1618">Az.Websites</span></span>
* <span data-ttu-id="2d993-1619">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2d993-1619">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="2d993-1620">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="2d993-1620">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="2d993-1621">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="2d993-1621">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="2d993-1622">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1622">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="2d993-1623">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="2d993-1623">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="2d993-1624">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1624">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d993-1625">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-1625">Highlights since the last major release</span></span>
* <span data-ttu-id="2d993-1626">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="2d993-1626">Updated client side telemetry.</span></span>
* <span data-ttu-id="2d993-1627">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="2d993-1627">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="2d993-1628">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="2d993-1628">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-1629">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1629">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1630">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1630">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-1631">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-1631">Az.Automation</span></span>
* <span data-ttu-id="2d993-1632">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-1632">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-1634">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1634">Updated SDK to 7.0</span></span>
* <span data-ttu-id="2d993-1635">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="2d993-1635">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1636">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1636">Az.Compute</span></span>
* <span data-ttu-id="2d993-1637">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="2d993-1637">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-1638">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-1638">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-1639">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="2d993-1639">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-1640">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1640">Az.IotHub</span></span>
* <span data-ttu-id="2d993-1641">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1641">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2d993-1642">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="2d993-1642">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d993-1643">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1643">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d993-1644">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1644">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d993-1645">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1645">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d993-1646">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d993-1646">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-1647">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-1647">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-1648">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-1648">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-1649">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1649">Az.Monitor</span></span>
* <span data-ttu-id="2d993-1650">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="2d993-1650">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="2d993-1651">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="2d993-1651">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="2d993-1652">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="2d993-1652">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1653">Az.Network</span></span>
* <span data-ttu-id="2d993-1654">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2d993-1654">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="2d993-1655">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-1655">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2d993-1656">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-1656">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2d993-1657">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-1657">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="2d993-1658">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="2d993-1658">No new cmdlets are added.</span></span> <span data-ttu-id="2d993-1659">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1659">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1660">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1661">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-1661">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1662">Az.Resources</span></span>
* <span data-ttu-id="2d993-1663">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d993-1663">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="2d993-1664">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1664">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="2d993-1665">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1665">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="2d993-1666">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1666">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="2d993-1667">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-1667">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="2d993-1668">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="2d993-1668">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="2d993-1669">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="2d993-1669">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="2d993-1670">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1670">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1671">Az.Sql</span></span>
* <span data-ttu-id="2d993-1672">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="2d993-1672">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="2d993-1673">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-1673">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="2d993-1674">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="2d993-1674">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2d993-1675">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2d993-1675">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2d993-1676">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="2d993-1676">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d993-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d993-1677">Az.StorageSync</span></span>
* <span data-ttu-id="2d993-1678">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1678">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="2d993-1679">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1679">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d993-1680">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-1680">Highlights since the last major release</span></span>
* <span data-ttu-id="2d993-1681">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2d993-1681">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="2d993-1682">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="2d993-1682">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-1683">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1683">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1684">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="2d993-1684">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="2d993-1685">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="2d993-1685">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-1686">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-1686">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-1687">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="2d993-1687">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="2d993-1688">**New-AzApiManagementProduct** _ и _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="2d993-1688">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="2d993-1689">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="2d993-1689">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="2d993-1690">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="2d993-1690">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1691">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1691">Az.Compute</span></span>
* <span data-ttu-id="2d993-1692">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d993-1692">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="2d993-1693">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2d993-1693">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="2d993-1694">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1694">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="2d993-1695">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-1695">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="2d993-1696">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1696">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1697">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1698">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1698">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2d993-1699">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2d993-1699">Az.DeploymentManager</span></span>
* <span data-ttu-id="2d993-1700">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="2d993-1700">Adds LIST operations for resources</span></span>
* <span data-ttu-id="2d993-1701">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="2d993-1701">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-1702">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-1702">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-1703">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2d993-1703">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-1704">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-1704">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-1705">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d993-1705">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1706">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1706">Az.Network</span></span>
* <span data-ttu-id="2d993-1707">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="2d993-1707">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="2d993-1708">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="2d993-1708">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="2d993-1709">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2d993-1709">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2d993-1710">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="2d993-1710">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="2d993-1711">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="2d993-1711">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="2d993-1712">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1712">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="2d993-1713">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d993-1713">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="2d993-1714">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1714">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="2d993-1715">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1715">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="2d993-1717">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-1717">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="2d993-1718">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2d993-1718">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="2d993-1719">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="2d993-1719">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-1720">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-1720">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-1721">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="2d993-1721">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="2d993-1722">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="2d993-1722">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="2d993-1723">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="2d993-1723">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="2d993-1724">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="2d993-1724">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1725">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1725">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1726">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="2d993-1726">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="2d993-1727">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d993-1727">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1728">Az.Resources</span></span>
* <span data-ttu-id="2d993-1729">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="2d993-1729">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="2d993-1730">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="2d993-1730">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1731">Az.Sql</span></span>
<span data-ttu-id="2d993-1732">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="2d993-1732">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1733">Az.Storage</span></span>
* <span data-ttu-id="2d993-1734">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2d993-1734">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="2d993-1735">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-1735">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d993-1736">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="2d993-1736">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="2d993-1737">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-1737">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-1738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-1738">Az.Websites</span></span>
* <span data-ttu-id="2d993-1739">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="2d993-1739">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="2d993-1740">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2d993-1740">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="2d993-1741">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1741">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-1742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1742">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1743">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="2d993-1743">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-1744">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-1744">Az.Cdn</span></span>
* <span data-ttu-id="2d993-1745">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2d993-1745">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1746">Az.Compute</span></span>
* <span data-ttu-id="2d993-1747">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="2d993-1747">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2d993-1748">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d993-1748">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d993-1749">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-1749">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2d993-1750">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d993-1750">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2d993-1751">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="2d993-1751">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d993-1752">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1752">Get the Edge Storage Container</span></span>
* <span data-ttu-id="2d993-1753">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="2d993-1753">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d993-1754">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1754">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="2d993-1755">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="2d993-1755">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d993-1756">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1756">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="2d993-1757">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="2d993-1757">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d993-1758">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1758">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="2d993-1759">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="2d993-1759">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d993-1760">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1760">Get the Edge Storage Account</span></span>
* <span data-ttu-id="2d993-1761">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="2d993-1761">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d993-1762">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1762">Create new Edge Storage Account</span></span>
* <span data-ttu-id="2d993-1763">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="2d993-1763">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d993-1764">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1764">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="2d993-1765">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="2d993-1765">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="2d993-1766">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="2d993-1766">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="2d993-1767">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="2d993-1767">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="2d993-1768">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="2d993-1768">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1769">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1769">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1770">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="2d993-1770">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="2d993-1771">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1771">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="2d993-1772">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="2d993-1772">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="2d993-1773">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2d993-1773">Az.DevTestLabs</span></span>
* <span data-ttu-id="2d993-1774">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-1774">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-1775">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1775">Az.EventHub</span></span>
* <span data-ttu-id="2d993-1776">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="2d993-1776">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-1777">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-1777">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-1778">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-1778">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2d993-1779">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d993-1779">Az.MachineLearning</span></span>
* <span data-ttu-id="2d993-1780">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-1780">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="2d993-1781">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="2d993-1781">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d993-1782">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="2d993-1782">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="2d993-1783">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="2d993-1783">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d993-1784">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="2d993-1784">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d993-1785">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="2d993-1785">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d993-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="2d993-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="2d993-1787">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="2d993-1787">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1788">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1788">Az.Network</span></span>
* <span data-ttu-id="2d993-1789">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="2d993-1789">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1791">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1791">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="2d993-1792">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1792">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2d993-1793">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1793">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2d993-1794">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-1794">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1795">Az.Resources</span></span>
* <span data-ttu-id="2d993-1796">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="2d993-1796">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1797">Az.Sql</span></span>
* <span data-ttu-id="2d993-1798">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2d993-1798">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="2d993-1799">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-1799">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2d993-1800">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2d993-1800">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2d993-1801">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="2d993-1801">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1802">Az.Storage</span></span>
* <span data-ttu-id="2d993-1803">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="2d993-1803">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="2d993-1804">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-1804">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="2d993-1805">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="2d993-1805">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="2d993-1806">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2d993-1806">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="2d993-1807">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1807">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="2d993-1808">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-1808">General</span></span>
* <span data-ttu-id="2d993-1809">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="2d993-1809">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1810">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1811">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="2d993-1811">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="2d993-1812">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="2d993-1812">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d993-1813">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-1813">Az.Batch</span></span>
* <span data-ttu-id="2d993-1814">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="2d993-1814">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1815">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1816">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1816">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-1817">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-1817">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-1818">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="2d993-1818">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="2d993-1819">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1819">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d993-1820">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d993-1820">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d993-1821">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="2d993-1821">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-1822">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-1822">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-1823">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="2d993-1823">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="2d993-1824">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="2d993-1824">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="2d993-1825">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2d993-1825">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-1826">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-1826">Az.Monitor</span></span>
* <span data-ttu-id="2d993-1827">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="2d993-1827">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="2d993-1828">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="2d993-1828">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="2d993-1829">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="2d993-1829">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1830">Az.Network</span></span>
* <span data-ttu-id="2d993-1831">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="2d993-1831">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1832">Az.Resources</span></span>
* <span data-ttu-id="2d993-1833">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-1833">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="2d993-1834">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="2d993-1834">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1835">Az.Sql</span></span>
* <span data-ttu-id="2d993-1836">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2d993-1836">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-1837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-1837">Az.Storage</span></span>
* <span data-ttu-id="2d993-1838">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="2d993-1838">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="2d993-1839">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="2d993-1839">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="2d993-1840">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d993-1840">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="2d993-1841">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="2d993-1841">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="2d993-1842">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="2d993-1842">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="2d993-1843">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-1843">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="2d993-1844">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="2d993-1844">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="2d993-1845">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2d993-1845">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="2d993-1846">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2d993-1846">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="2d993-1847">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="2d993-1847">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="2d993-1848">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="2d993-1848">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="2d993-1849">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="2d993-1849">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="2d993-1850">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="2d993-1850">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="2d993-1851">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1851">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d993-1852">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-1852">Highlights since the last major release</span></span>
* <span data-ttu-id="2d993-1853">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d993-1853">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="2d993-1854">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d993-1854">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1855">Az.Compute</span></span>
* <span data-ttu-id="2d993-1856">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2d993-1856">VM Reapply feature</span></span>
    - <span data-ttu-id="2d993-1857">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1857">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="2d993-1858">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="2d993-1858">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="2d993-1859">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d993-1859">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="2d993-1860">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-1860">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="2d993-1861">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-1861">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d993-1862">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="2d993-1862">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="2d993-1863">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="2d993-1863">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="2d993-1864">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2d993-1864">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="2d993-1865">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="2d993-1865">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="2d993-1866">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-1866">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2d993-1867">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d993-1867">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2d993-1868">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1868">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d993-1869">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="2d993-1869">Get the Order</span></span>
* <span data-ttu-id="2d993-1870">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1870">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d993-1871">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="2d993-1871">Create new Order</span></span>
* <span data-ttu-id="2d993-1872">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1872">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d993-1873">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="2d993-1873">Remove the Order</span></span>
* <span data-ttu-id="2d993-1874">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1874">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="2d993-1875">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1875">Now creates Local Share</span></span>
* <span data-ttu-id="2d993-1876">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1876">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="2d993-1877">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="2d993-1877">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="2d993-1878">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1878">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="2d993-1879">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="2d993-1879">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="2d993-1880">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1880">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d993-1881">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="2d993-1881">Gets the information about Triggers</span></span>
* <span data-ttu-id="2d993-1882">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1882">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d993-1883">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="2d993-1883">Create new Triggers</span></span>
* <span data-ttu-id="2d993-1884">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1884">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d993-1885">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="2d993-1885">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1886">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1886">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1887">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1887">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="2d993-1888">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1888">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-1889">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-1889">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-1890">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="2d993-1890">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-1891">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-1891">Az.EventHub</span></span>
* <span data-ttu-id="2d993-1892">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="2d993-1892">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-1893">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-1893">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-1894">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-1894">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="2d993-1895">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-1895">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="2d993-1896">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="2d993-1896">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="2d993-1897">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="2d993-1897">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-1898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-1898">Az.Network</span></span>
* <span data-ttu-id="2d993-1899">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-1899">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="2d993-1900">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="2d993-1900">Az.PrivateDns</span></span>
* <span data-ttu-id="2d993-1901">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d993-1901">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-1902">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-1902">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-1903">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="2d993-1903">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="2d993-1904">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d993-1904">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="2d993-1905">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="2d993-1905">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d993-1906">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d993-1906">Az.RedisCache</span></span>
* <span data-ttu-id="2d993-1907">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="2d993-1907">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="2d993-1908">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="2d993-1908">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="2d993-1909">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="2d993-1909">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-1910">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-1910">Az.Resources</span></span>
- <span data-ttu-id="2d993-1911">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="2d993-1911">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="2d993-1912">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="2d993-1912">Updated create policy definition help example</span></span>
- <span data-ttu-id="2d993-1913">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="2d993-1913">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="2d993-1914">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-1914">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="2d993-1915">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="2d993-1915">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-1916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-1916">Az.Sql</span></span>
* <span data-ttu-id="2d993-1917">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-1917">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="2d993-1918">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="2d993-1918">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="2d993-1919">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-1919">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="2d993-1920">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-1920">General</span></span>
* <span data-ttu-id="2d993-1921">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d993-1921">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-1922">Az.Accounts</span></span>
* <span data-ttu-id="2d993-1923">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="2d993-1923">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2d993-1924">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d993-1924">Az.Advisor</span></span>
* <span data-ttu-id="2d993-1925">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="2d993-1925">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d993-1926">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-1926">Az.Batch</span></span>
* <span data-ttu-id="2d993-1927">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1927">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="2d993-1928">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1928">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="2d993-1929">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1929">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="2d993-1930">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1930">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="2d993-1931">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1931">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="2d993-1932">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1932">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="2d993-1933">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="2d993-1933">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="2d993-1934">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="2d993-1934">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="2d993-1935">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="2d993-1935">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="2d993-1936">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1936">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2d993-1937">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1937">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="2d993-1938">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1938">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="2d993-1939">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1939">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2d993-1940">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1940">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="2d993-1941">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1941">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="2d993-1942">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1942">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="2d993-1943">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1943">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="2d993-1944">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1944">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="2d993-1945">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1945">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="2d993-1946">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2d993-1946">This operation is no longer supported.</span></span>
* <span data-ttu-id="2d993-1947">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1947">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2d993-1948">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1948">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2d993-1949">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1949">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="2d993-1950">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1950">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="2d993-1951">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="2d993-1951">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="2d993-1952">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="2d993-1952">New non-verified images are also now returned.</span></span> <span data-ttu-id="2d993-1953">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="2d993-1953">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="2d993-1954">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="2d993-1954">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="2d993-1955">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="2d993-1955">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="2d993-1956">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1956">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="2d993-1957">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="2d993-1957">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="2d993-1958">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1958">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="2d993-1959">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="2d993-1959">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="2d993-1960">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="2d993-1960">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="2d993-1961">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="2d993-1961">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="2d993-1962">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="2d993-1962">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-1963">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-1963">Az.Cdn</span></span>
* <span data-ttu-id="2d993-1964">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="2d993-1964">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="2d993-1965">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="2d993-1965">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-1966">Az.Compute</span></span>
* <span data-ttu-id="2d993-1967">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="2d993-1967">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="2d993-1968">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2d993-1968">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="2d993-1969">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d993-1969">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="2d993-1970">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-1970">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d993-1971">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-1971">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="2d993-1972">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="2d993-1972">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="2d993-1973">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d993-1973">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d993-1974">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="2d993-1974">Breaking changes</span></span>
    - <span data-ttu-id="2d993-1975">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="2d993-1975">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="2d993-1976">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2d993-1976">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-1977">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-1977">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-1978">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-1978">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-1979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-1979">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-1980">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="2d993-1980">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="2d993-1981">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="2d993-1981">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="2d993-1982">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="2d993-1982">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="2d993-1983">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="2d993-1983">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="2d993-1984">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="2d993-1984">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="2d993-1985">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="2d993-1985">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-1986">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-1986">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-1987">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="2d993-1987">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-1988">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-1988">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-1989">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="2d993-1989">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="2d993-1990">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2d993-1990">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="2d993-1991">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="2d993-1991">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="2d993-1992">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-1992">Removed five cmdlets:</span></span>
    - <span data-ttu-id="2d993-1993">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d993-1993">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d993-1994">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d993-1994">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d993-1995">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d993-1995">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d993-1996">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d993-1996">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="2d993-1997">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d993-1997">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="2d993-1998">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="2d993-1998">Added three cmdlets:</span></span>
    - <span data-ttu-id="2d993-1999">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d993-1999">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2d993-2000">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d993-2000">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2d993-2001">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d993-2001">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="2d993-2002">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2002">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="2d993-2003">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="2d993-2003">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="2d993-2004">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="2d993-2004">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="2d993-2005">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-2005">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="2d993-2006">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="2d993-2006">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="2d993-2007">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="2d993-2007">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="2d993-2008">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="2d993-2008">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="2d993-2009">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="2d993-2009">Added some scenario test cases.</span></span>
* <span data-ttu-id="2d993-2010">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="2d993-2010">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-2011">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2011">Az.IotHub</span></span>
* <span data-ttu-id="2d993-2012">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="2d993-2012">Breaking changes:</span></span>
    - <span data-ttu-id="2d993-2013">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2013">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d993-2014">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-2014">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d993-2015">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2015">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d993-2016">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-2016">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d993-2017">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="2d993-2017">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="2d993-2018">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="2d993-2018">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="2d993-2019">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="2d993-2019">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="2d993-2020">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="2d993-2020">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="2d993-2021">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2021">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d993-2022">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-2022">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d993-2023">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2023">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d993-2024">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="2d993-2024">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2025">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2026">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2026">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="2d993-2027">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2027">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="2d993-2028">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2028">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="2d993-2029">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2029">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="2d993-2030">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2030">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="2d993-2031">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2031">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="2d993-2032">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2032">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="2d993-2033">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2033">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="2d993-2034">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="2d993-2034">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2035">Az.Resources</span></span>
* <span data-ttu-id="2d993-2036">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="2d993-2036">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2037">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2037">Az.Network</span></span>
* <span data-ttu-id="2d993-2038">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="2d993-2038">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="2d993-2039">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2d993-2039">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d993-2040">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2040">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2041">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2041">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2042">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2042">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2043">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2043">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2044">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-2044">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2d993-2045">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="2d993-2045">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="2d993-2046">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="2d993-2046">New cmdlet:</span></span>
        - <span data-ttu-id="2d993-2047">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="2d993-2047">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="2d993-2048">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="2d993-2048">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="2d993-2049">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d993-2049">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="2d993-2050">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-2050">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="2d993-2051">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="2d993-2051">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="2d993-2052">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="2d993-2052">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="2d993-2053">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="2d993-2053">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="2d993-2054">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2054">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="2d993-2055">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2055">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-2056">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2d993-2056">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="2d993-2057">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-2057">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d993-2058">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-2058">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d993-2059">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-2059">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d993-2060">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2060">Set-AzVirtualHub</span></span>
* <span data-ttu-id="2d993-2061">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d993-2061">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="2d993-2062">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="2d993-2062">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d993-2063">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="2d993-2063">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2d993-2064">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="2d993-2064">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2d993-2065">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="2d993-2065">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="2d993-2066">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="2d993-2066">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="2d993-2067">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-2067">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="2d993-2068">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2068">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-2069">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-2069">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="2d993-2070">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="2d993-2070">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d993-2071">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2d993-2071">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d993-2072">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2d993-2072">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d993-2073">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2d993-2073">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d993-2074">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2d993-2074">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d993-2075">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2d993-2075">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="2d993-2076">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="2d993-2076">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="2d993-2077">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2077">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-2078">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="2d993-2078">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="2d993-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="2d993-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="2d993-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2d993-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="2d993-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="2d993-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="2d993-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="2d993-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="2d993-2084">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="2d993-2084">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d993-2085">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2085">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="2d993-2086">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2086">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="2d993-2087">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="2d993-2087">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="2d993-2088">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="2d993-2088">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="2d993-2089">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="2d993-2089">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d993-2090">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="2d993-2090">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="2d993-2091">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="2d993-2091">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="2d993-2092">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="2d993-2092">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="2d993-2093">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="2d993-2093">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="2d993-2094">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="2d993-2094">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="2d993-2095">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2095">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-2096">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d993-2096">New-AzIpGroup</span></span>
        - <span data-ttu-id="2d993-2097">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d993-2097">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="2d993-2098">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d993-2098">Get-AzIpGroup</span></span>
        - <span data-ttu-id="2d993-2099">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d993-2099">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-2100">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-2100">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-2101">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="2d993-2101">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2102">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2102">Az.Sql</span></span>
* <span data-ttu-id="2d993-2103">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2103">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="2d993-2104">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="2d993-2104">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="2d993-2105">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="2d993-2105">Removed deprecated aliases:</span></span>
* <span data-ttu-id="2d993-2106">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="2d993-2106">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="2d993-2107">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="2d993-2107">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="2d993-2108">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-2108">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2d993-2109">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="2d993-2109">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="2d993-2110">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="2d993-2110">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="2d993-2111">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-2111">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2112">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2112">Az.Storage</span></span>
* <span data-ttu-id="2d993-2113">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2d993-2113">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="2d993-2114">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2114">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2d993-2115">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2115">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2d993-2116">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="2d993-2116">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="2d993-2117">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d993-2117">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="2d993-2118">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d993-2118">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="2d993-2119">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2119">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="2d993-2120">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-2120">General</span></span>
* <span data-ttu-id="2d993-2121">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d993-2121">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-2122">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2122">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2123">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="2d993-2123">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-2124">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-2124">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-2125">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2125">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="2d993-2126">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="2d993-2126">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-2127">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-2127">Az.Automation</span></span>
* <span data-ttu-id="2d993-2128">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="2d993-2128">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d993-2129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-2129">Az.Batch</span></span>
* <span data-ttu-id="2d993-2130">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2130">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2131">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2131">Az.Compute</span></span>
* <span data-ttu-id="2d993-2132">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="2d993-2132">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d993-2133">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="2d993-2133">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="2d993-2134">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="2d993-2134">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="2d993-2135">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="2d993-2135">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-2136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-2136">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-2137">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="2d993-2137">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="2d993-2138">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="2d993-2138">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="2d993-2139">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2139">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-2140">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-2140">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-2141">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="2d993-2141">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d993-2142">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d993-2142">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d993-2143">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2143">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="2d993-2144">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="2d993-2144">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="2d993-2145">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-2145">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="2d993-2146">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="2d993-2146">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-2147">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2147">Az.IotHub</span></span>
* <span data-ttu-id="2d993-2148">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="2d993-2148">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="2d993-2149">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2149">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-2150">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-2150">Az.Monitor</span></span>
* <span data-ttu-id="2d993-2151">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="2d993-2151">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="2d993-2152">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="2d993-2152">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="2d993-2153">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="2d993-2153">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="2d993-2154">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d993-2154">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2155">Az.Network</span></span>
* <span data-ttu-id="2d993-2156">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="2d993-2156">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="2d993-2157">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="2d993-2157">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="2d993-2158">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2158">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-2159">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-2159">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="2d993-2160">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2160">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d993-2161">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="2d993-2161">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="2d993-2162">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2162">Updated cmdlets:</span></span>
        - <span data-ttu-id="2d993-2163">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2163">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d993-2164">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2164">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d993-2165">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2165">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2d993-2166">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="2d993-2166">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="2d993-2167">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2d993-2167">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="2d993-2168">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2d993-2168">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="2d993-2169">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="2d993-2169">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d993-2170">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d993-2170">Az.RedisCache</span></span>
* <span data-ttu-id="2d993-2171">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="2d993-2171">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2172">Az.Sql</span></span>
* <span data-ttu-id="2d993-2173">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="2d993-2173">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2174">Az.Storage</span></span>
* <span data-ttu-id="2d993-2175">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2175">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="2d993-2176">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="2d993-2176">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2d993-2177">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2d993-2177">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="2d993-2178">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-2178">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2d993-2179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2179">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d993-2180">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d993-2180">Az.StorageSync</span></span>
* <span data-ttu-id="2d993-2181">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="2d993-2181">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2182">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2182">Az.Websites</span></span>
* <span data-ttu-id="2d993-2183">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2183">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="2d993-2184">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2184">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2d993-2185">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-2185">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-2186">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="2d993-2186">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="2d993-2187">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-2187">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="2d993-2188">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d993-2188">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-2189">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-2189">Az.Automation</span></span>
* <span data-ttu-id="2d993-2190">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="2d993-2190">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="2d993-2191">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="2d993-2191">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="2d993-2192">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="2d993-2192">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2193">Az.Compute</span></span>
* <span data-ttu-id="2d993-2194">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2194">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="2d993-2195">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2195">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d993-2196">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="2d993-2196">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="2d993-2197">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="2d993-2197">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="2d993-2198">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="2d993-2198">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="2d993-2199">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="2d993-2199">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="2d993-2200">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="2d993-2200">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="2d993-2201">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="2d993-2201">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="2d993-2202">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-2202">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-2203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-2203">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-2204">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="2d993-2204">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="2d993-2205">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="2d993-2205">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-2206">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-2206">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-2207">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2207">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-2208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2208">Az.IotHub</span></span>
* <span data-ttu-id="2d993-2209">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d993-2209">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="2d993-2210">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="2d993-2210">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="2d993-2211">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2211">New cmdlets are:</span></span>
    - <span data-ttu-id="2d993-2212">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="2d993-2212">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d993-2213">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="2d993-2213">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d993-2214">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="2d993-2214">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d993-2215">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="2d993-2215">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-2216">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-2216">Az.Monitor</span></span>
* <span data-ttu-id="2d993-2217">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="2d993-2217">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="2d993-2218">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="2d993-2218">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="2d993-2219">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="2d993-2219">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="2d993-2220">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="2d993-2220">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="2d993-2221">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="2d993-2221">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="2d993-2222">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="2d993-2222">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="2d993-2223">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2223">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="2d993-2224">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2224">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="2d993-2225">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-2225">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2d993-2226">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="2d993-2226">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="2d993-2227">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-2227">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2d993-2228">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="2d993-2228">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="2d993-2229">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="2d993-2229">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="2d993-2230">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="2d993-2230">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="2d993-2231">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="2d993-2231">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="2d993-2232">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="2d993-2232">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="2d993-2233">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="2d993-2233">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="2d993-2234">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="2d993-2234">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="2d993-2235">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-2235">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="2d993-2236">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="2d993-2236">Overall improved help files</span></span>
* <span data-ttu-id="2d993-2237">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="2d993-2237">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2238">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2238">Az.Network</span></span>
* <span data-ttu-id="2d993-2239">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-2239">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="2d993-2240">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2240">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="2d993-2241">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="2d993-2241">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="2d993-2242">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="2d993-2242">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="2d993-2243">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-2243">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="2d993-2244">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="2d993-2244">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="2d993-2245">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2d993-2245">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="2d993-2246">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2246">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="2d993-2247">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="2d993-2247">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="2d993-2248">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="2d993-2248">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="2d993-2249">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2249">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="2d993-2250">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="2d993-2250">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="2d993-2251">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2251">New cmdlets</span></span>
        - <span data-ttu-id="2d993-2252">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="2d993-2252">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="2d993-2253">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="2d993-2253">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="2d993-2254">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2d993-2254">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d993-2255">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="2d993-2255">New-VpnSite</span></span>
        - <span data-ttu-id="2d993-2256">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="2d993-2256">Update-VpnSite</span></span>
        - <span data-ttu-id="2d993-2257">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="2d993-2257">New-VpnConnection</span></span>
        - <span data-ttu-id="2d993-2258">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2258">Update-VpnConnection</span></span>
* <span data-ttu-id="2d993-2259">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="2d993-2259">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2261">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="2d993-2261">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="2d993-2262">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2262">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2263">Az.Resources</span></span>
* <span data-ttu-id="2d993-2264">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="2d993-2264">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-2265">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-2265">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-2266">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="2d993-2266">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="2d993-2267">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="2d993-2267">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="2d993-2268">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2d993-2268">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d993-2269">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="2d993-2269">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d993-2270">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="2d993-2270">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d993-2271">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="2d993-2271">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="2d993-2272">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2d993-2272">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d993-2273">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2d993-2273">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d993-2274">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="2d993-2274">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d993-2275">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="2d993-2275">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d993-2276">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="2d993-2276">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="2d993-2277">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="2d993-2277">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d993-2278">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="2d993-2278">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d993-2279">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="2d993-2279">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d993-2280">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="2d993-2280">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="2d993-2281">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2d993-2281">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d993-2282">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d993-2282">Az.SignalR</span></span>
* <span data-ttu-id="2d993-2283">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="2d993-2283">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2284">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2284">Az.Sql</span></span>
* <span data-ttu-id="2d993-2285">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="2d993-2285">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="2d993-2286">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="2d993-2286">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="2d993-2287">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-2287">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2d993-2288">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="2d993-2288">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="2d993-2289">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="2d993-2289">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2290">Az.Storage</span></span>
* <span data-ttu-id="2d993-2291">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="2d993-2291">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2d993-2292">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="2d993-2292">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="2d993-2293">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d993-2293">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="2d993-2294">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d993-2294">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="2d993-2295">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-2295">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="2d993-2296">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-2296">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="2d993-2297">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-2297">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="2d993-2298">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2d993-2298">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d993-2299">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2d993-2299">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d993-2300">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="2d993-2300">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d993-2301">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2d993-2301">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2302">Az.Websites</span></span>
* <span data-ttu-id="2d993-2303">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="2d993-2303">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="2d993-2304">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="2d993-2304">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="2d993-2305">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="2d993-2305">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="2d993-2306">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2306">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="2d993-2307">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-2307">General</span></span>
* <span data-ttu-id="2d993-2308">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="2d993-2308">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-2309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2309">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2310">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="2d993-2310">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-2311">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-2311">Az.Aks</span></span>
* <span data-ttu-id="2d993-2312">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="2d993-2312">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="2d993-2313">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="2d993-2313">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-2314">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-2314">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-2315">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="2d993-2315">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="2d993-2316">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2316">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="2d993-2317">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2317">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="2d993-2318">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="2d993-2318">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="2d993-2319">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="2d993-2319">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d993-2320">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-2320">Az.Batch</span></span>
* <span data-ttu-id="2d993-2321">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="2d993-2321">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-2322">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-2322">Az.Cdn</span></span>
* <span data-ttu-id="2d993-2323">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="2d993-2323">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2324">Az.Compute</span></span>
* <span data-ttu-id="2d993-2325">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2325">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="2d993-2326">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-2326">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="2d993-2327">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d993-2327">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="2d993-2328">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-2328">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="2d993-2329">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2d993-2329">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="2d993-2330">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-2330">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="2d993-2331">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2331">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="2d993-2332">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="2d993-2332">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-2333">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-2333">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-2334">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="2d993-2334">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="2d993-2335">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="2d993-2335">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="2d993-2336">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="2d993-2336">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="2d993-2337">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="2d993-2337">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-2338">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-2338">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-2339">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="2d993-2339">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-2340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2340">Az.EventHub</span></span>
* <span data-ttu-id="2d993-2341">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-2341">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="2d993-2342">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="2d993-2342">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="2d993-2343">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="2d993-2343">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="2d993-2344">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="2d993-2344">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="2d993-2345">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d993-2345">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d993-2346">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="2d993-2346">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-2347">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-2347">Az.Monitor</span></span>
* <span data-ttu-id="2d993-2348">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="2d993-2348">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2349">Az.Network</span></span>
* <span data-ttu-id="2d993-2350">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2350">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="2d993-2351">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="2d993-2351">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="2d993-2352">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="2d993-2352">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="2d993-2353">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2d993-2353">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="2d993-2354">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d993-2354">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="2d993-2355">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2355">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="2d993-2356">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="2d993-2356">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-2357">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2357">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-2358">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="2d993-2358">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="2d993-2359">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="2d993-2359">Added example</span></span>
    - <span data-ttu-id="2d993-2360">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="2d993-2360">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="2d993-2361">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2d993-2361">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="2d993-2362">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="2d993-2362">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2363">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2363">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2364">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2364">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2365">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2365">Az.Resources</span></span>
* <span data-ttu-id="2d993-2366">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="2d993-2366">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="2d993-2367">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="2d993-2367">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="2d993-2368">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="2d993-2368">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="2d993-2369">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-2369">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d993-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d993-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="2d993-2371">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-2371">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="2d993-2372">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="2d993-2372">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="2d993-2373">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="2d993-2373">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-2374">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-2374">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-2375">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="2d993-2375">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="2d993-2376">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2d993-2376">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="2d993-2377">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="2d993-2377">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="2d993-2378">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="2d993-2378">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="2d993-2379">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="2d993-2379">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="2d993-2380">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="2d993-2380">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2381">Az.Sql</span></span>
* <span data-ttu-id="2d993-2382">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="2d993-2382">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2383">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2383">Az.Storage</span></span>
* <span data-ttu-id="2d993-2384">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="2d993-2384">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="2d993-2385">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="2d993-2385">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="2d993-2386">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-2386">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="2d993-2387">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-2387">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="2d993-2388">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="2d993-2388">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="2d993-2389">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-2389">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2390">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2390">Az.Websites</span></span>
* <span data-ttu-id="2d993-2391">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="2d993-2391">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="2d993-2392">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2392">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-2393">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2393">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2394">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="2d993-2394">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2d993-2395">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2395">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2d993-2396">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="2d993-2396">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-2397">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-2397">Az.Automation</span></span>
* <span data-ttu-id="2d993-2398">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d993-2398">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-2399">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2399">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-2400">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-2400">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2401">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2401">Az.Compute</span></span>
* <span data-ttu-id="2d993-2402">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d993-2402">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d993-2403">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d993-2403">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d993-2404">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="2d993-2404">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="2d993-2405">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="2d993-2405">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-2406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-2406">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-2407">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2407">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="2d993-2408">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="2d993-2408">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-2409">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2409">Az.EventHub</span></span>
* <span data-ttu-id="2d993-2410">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="2d993-2410">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2d993-2411">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="2d993-2411">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-2412">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-2412">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-2413">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2413">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d993-2414">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d993-2414">Az.LogicApp</span></span>
* <span data-ttu-id="2d993-2415">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="2d993-2415">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="2d993-2416">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="2d993-2416">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d993-2417">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2417">Az.ManagedServices</span></span>
* <span data-ttu-id="2d993-2418">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="2d993-2418">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2419">Az.Network</span></span>
* <span data-ttu-id="2d993-2420">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="2d993-2420">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="2d993-2421">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2421">New cmdlets</span></span>
        - <span data-ttu-id="2d993-2422">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2d993-2422">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d993-2423">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2d993-2423">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d993-2424">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2424">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2425">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2425">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2426">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2426">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2427">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2427">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d993-2428">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="2d993-2428">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="2d993-2429">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2d993-2429">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="2d993-2430">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2430">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="2d993-2431">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2431">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="2d993-2432">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2432">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="2d993-2433">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2433">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="2d993-2434">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="2d993-2434">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="2d993-2435">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2435">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="2d993-2436">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2436">Updated cmdlets</span></span>
        - <span data-ttu-id="2d993-2437">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2437">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d993-2438">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2438">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d993-2439">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2439">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2d993-2440">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2440">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d993-2441">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-2441">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="2d993-2442">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2d993-2442">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d993-2443">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2443">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2d993-2444">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2444">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2d993-2445">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2d993-2445">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="2d993-2446">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="2d993-2446">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="2d993-2447">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="2d993-2447">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="2d993-2448">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="2d993-2448">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-2449">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2449">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-2450">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="2d993-2450">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="2d993-2451">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2451">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2452">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2453">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2453">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2d993-2454">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2454">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="2d993-2455">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2455">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="2d993-2456">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2456">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2d993-2457">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2457">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="2d993-2458">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2458">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2d993-2459">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2459">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="2d993-2460">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2460">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2d993-2461">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2461">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="2d993-2462">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="2d993-2462">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2463">Az.Resources</span></span>
- <span data-ttu-id="2d993-2464">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-2464">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="2d993-2465">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-2465">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d993-2466">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d993-2466">Az.ServiceBus</span></span>
* <span data-ttu-id="2d993-2467">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="2d993-2467">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2d993-2468">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="2d993-2468">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2469">Az.Sql</span></span>
* <span data-ttu-id="2d993-2470">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="2d993-2470">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="2d993-2471">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2d993-2471">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="2d993-2472">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2472">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2473">Az.Storage</span></span>
* <span data-ttu-id="2d993-2474">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2474">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d993-2475">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d993-2475">Az.StorageSync</span></span>
* <span data-ttu-id="2d993-2476">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="2d993-2476">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="2d993-2477">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="2d993-2477">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2478">Az.Websites</span></span>
* <span data-ttu-id="2d993-2479">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="2d993-2479">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="2d993-2480">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="2d993-2480">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="2d993-2481">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="2d993-2481">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="2d993-2482">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2482">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2483">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2484">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="2d993-2484">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2d993-2485">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2485">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2d993-2486">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2d993-2486">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2d993-2487">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d993-2487">Az.Advisor</span></span>
* <span data-ttu-id="2d993-2488">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="2d993-2488">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2d993-2489">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="2d993-2489">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d993-2490">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-2490">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-2491">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="2d993-2491">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2d993-2492">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2d993-2492">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2d993-2493">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="2d993-2493">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2d993-2494">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="2d993-2494">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2d993-2495">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="2d993-2495">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2d993-2496">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d993-2496">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2d993-2497">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2497">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-2498">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-2498">Az.Automation</span></span>
* <span data-ttu-id="2d993-2499">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2499">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2500">Az.Compute</span></span>
* <span data-ttu-id="2d993-2501">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="2d993-2501">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-2502">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-2503">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="2d993-2503">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d993-2504">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d993-2504">Az.EventGrid</span></span>
* <span data-ttu-id="2d993-2505">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2d993-2505">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-2506">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2506">Az.IotHub</span></span>
* <span data-ttu-id="2d993-2507">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="2d993-2507">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2508">Az.Network</span></span>
* <span data-ttu-id="2d993-2509">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="2d993-2509">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2d993-2510">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="2d993-2510">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-2511">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2511">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-2512">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2d993-2512">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2d993-2513">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="2d993-2513">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-2514">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2514">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-2515">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="2d993-2515">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2516">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2516">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2517">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="2d993-2517">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2518">Az.Resources</span></span>
    - <span data-ttu-id="2d993-2519">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="2d993-2519">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2d993-2520">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="2d993-2520">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2d993-2521">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-2521">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2d993-2522">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="2d993-2522">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d993-2523">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d993-2523">Az.ServiceBus</span></span>
* <span data-ttu-id="2d993-2524">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="2d993-2524">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2525">Az.Sql</span></span>
* <span data-ttu-id="2d993-2526">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2526">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2d993-2527">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-2527">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2d993-2528">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d993-2528">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d993-2529">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d993-2529">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d993-2530">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d993-2530">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d993-2531">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d993-2531">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2d993-2532">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d993-2532">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2d993-2533">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d993-2533">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2d993-2534">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2d993-2534">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2535">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2535">Az.Storage</span></span>
* <span data-ttu-id="2d993-2536">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="2d993-2536">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2d993-2537">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d993-2537">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2d993-2538">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="2d993-2538">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2d993-2539">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2d993-2539">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2d993-2540">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="2d993-2540">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2d993-2541">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2541">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2d993-2542">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2542">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2d993-2543">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="2d993-2543">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2d993-2544">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d993-2544">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2d993-2545">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d993-2545">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d993-2546">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d993-2546">Az.StorageSync</span></span>
* <span data-ttu-id="2d993-2547">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="2d993-2547">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2d993-2548">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2548">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2549">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2550">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="2d993-2550">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2d993-2551">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="2d993-2551">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2d993-2552">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="2d993-2552">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2d993-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2d993-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2d993-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="2d993-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2555">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2555">Az.Compute</span></span>
* <span data-ttu-id="2d993-2556">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-2556">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2d993-2557">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-2557">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2d993-2558">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2d993-2558">Az.Dns</span></span>
* <span data-ttu-id="2d993-2559">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="2d993-2559">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d993-2560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d993-2560">Az.EventGrid</span></span>
* <span data-ttu-id="2d993-2561">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-2561">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2d993-2562">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2562">New cmdlets:</span></span>
    - <span data-ttu-id="2d993-2563">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d993-2563">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d993-2564">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2564">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d993-2565">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d993-2565">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d993-2566">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2566">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2d993-2567">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d993-2567">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d993-2568">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2568">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d993-2569">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2d993-2569">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2d993-2570">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2570">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d993-2571">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2d993-2571">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2d993-2572">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="2d993-2572">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2d993-2573">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2d993-2573">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2d993-2574">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2574">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2d993-2575">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2d993-2575">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2d993-2576">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2576">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="2d993-2577">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2d993-2577">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2d993-2578">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2578">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2d993-2579">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-2579">Updated cmdlets:</span></span>
    - <span data-ttu-id="2d993-2580">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2d993-2580">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2d993-2581">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2581">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2d993-2582">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2582">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2d993-2583">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="2d993-2583">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2d993-2584">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="2d993-2584">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2d993-2585">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="2d993-2585">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2d993-2586">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="2d993-2586">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2d993-2587">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2587">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2d993-2588">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="2d993-2588">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="2d993-2589">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2d993-2589">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2d993-2590">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2590">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2d993-2591">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2d993-2591">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2d993-2592">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2592">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2d993-2593">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2593">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-2594">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-2594">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-2595">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2d993-2595">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2d993-2596">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="2d993-2596">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2d993-2597">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2d993-2597">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2d993-2598">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2598">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2599">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2599">Az.Network</span></span>
* <span data-ttu-id="2d993-2600">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2600">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2d993-2601">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2601">New cmdlets</span></span>
        - <span data-ttu-id="2d993-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2d993-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2d993-2603">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="2d993-2603">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2d993-2604">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2604">New cmdlets</span></span>
        - <span data-ttu-id="2d993-2605">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2d993-2605">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2d993-2606">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2d993-2606">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2d993-2607">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2607">New cmdlets</span></span>
        - <span data-ttu-id="2d993-2608">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d993-2608">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d993-2609">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d993-2609">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d993-2610">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d993-2610">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d993-2611">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-2611">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2d993-2612">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-2612">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2d993-2613">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2d993-2613">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2d993-2614">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2614">New cmdlets</span></span>
        - <span data-ttu-id="2d993-2615">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d993-2615">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d993-2616">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d993-2616">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d993-2617">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d993-2617">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d993-2618">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2d993-2618">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2d993-2619">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2619">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2d993-2620">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2620">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2d993-2621">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2621">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2d993-2622">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="2d993-2622">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2d993-2623">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="2d993-2623">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2d993-2624">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="2d993-2624">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2d993-2625">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-2625">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2d993-2626">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="2d993-2626">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2d993-2627">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-2627">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2d993-2628">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="2d993-2628">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2d993-2629">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2d993-2629">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2d993-2630">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="2d993-2630">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2d993-2631">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="2d993-2631">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2d993-2632">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2632">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2d993-2633">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2d993-2633">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2d993-2634">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2634">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2d993-2635">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2635">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2d993-2636">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-2636">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2d993-2637">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="2d993-2637">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="2d993-2638">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2638">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="2d993-2639">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="2d993-2639">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2d993-2640">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="2d993-2640">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2d993-2641">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="2d993-2641">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-2642">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2642">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-2643">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2d993-2643">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2644">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2644">Az.Resources</span></span>
* <span data-ttu-id="2d993-2645">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d993-2645">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2d993-2646">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="2d993-2646">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2d993-2647">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="2d993-2647">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2d993-2648">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2648">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-2649">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-2649">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-2650">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d993-2650">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2651">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2651">Az.Sql</span></span>
* <span data-ttu-id="2d993-2652">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="2d993-2652">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2d993-2653">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="2d993-2653">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2d993-2654">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="2d993-2654">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2d993-2655">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d993-2655">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d993-2656">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d993-2656">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d993-2657">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d993-2657">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d993-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2d993-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2d993-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2d993-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2660">Az.Storage</span></span>
* <span data-ttu-id="2d993-2661">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2661">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2d993-2662">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2662">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d993-2663">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2663">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2d993-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2665">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2665">Az.Websites</span></span>
* <span data-ttu-id="2d993-2666">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="2d993-2666">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2d993-2667">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="2d993-2667">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2d993-2668">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2668">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2d993-2669">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-2669">Az.Cdn</span></span>
* <span data-ttu-id="2d993-2670">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="2d993-2670">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2671">Az.Compute</span></span>
* <span data-ttu-id="2d993-2672">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="2d993-2672">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2d993-2673">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-2673">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-2674">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2674">Az.EventHub</span></span>
* <span data-ttu-id="2d993-2675">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="2d993-2675">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2d993-2676">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2d993-2676">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2677">Az.Network</span></span>
* <span data-ttu-id="2d993-2678">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="2d993-2678">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2d993-2679">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-2679">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-2680">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2680">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-2681">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="2d993-2681">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2682">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2683">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="2d993-2683">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d993-2684">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d993-2684">Az.ServiceBus</span></span>
* <span data-ttu-id="2d993-2685">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2d993-2685">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-2686">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-2686">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-2687">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="2d993-2687">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2d993-2688">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2d993-2688">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2689">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2689">Az.Sql</span></span>
* <span data-ttu-id="2d993-2690">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2690">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2d993-2691">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="2d993-2691">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2d993-2692">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="2d993-2692">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2d993-2693">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="2d993-2693">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2694">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2694">Az.Websites</span></span>
* <span data-ttu-id="2d993-2695">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="2d993-2695">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2d993-2696">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2696">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2d993-2697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-2697">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-2698">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2698">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2d993-2699">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2699">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2d993-2700">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2700">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2d993-2701">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="2d993-2701">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2d993-2702">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="2d993-2702">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2d993-2703">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="2d993-2703">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2d993-2704">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2704">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2d993-2705">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2705">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2d993-2706">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d993-2706">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2d993-2707">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2707">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2d993-2708">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2708">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2d993-2709">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="2d993-2709">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2d993-2710">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="2d993-2710">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2d993-2711">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2711">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2d993-2712">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2712">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2d993-2713">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2713">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2d993-2714">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2714">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2d993-2715">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2715">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2d993-2716">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d993-2716">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="2d993-2717">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="2d993-2717">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2d993-2718">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-2718">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2d993-2719">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="2d993-2719">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2d993-2720">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="2d993-2720">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2d993-2721">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d993-2721">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="2d993-2722">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="2d993-2722">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2d993-2723">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="2d993-2723">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2d993-2724">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="2d993-2724">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2d993-2725">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d993-2725">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2d993-2726">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d993-2726">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2d993-2727">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-2727">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2d993-2728">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2d993-2728">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="2d993-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2d993-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2d993-2730">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2730">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2d993-2731">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="2d993-2731">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d993-2732">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2732">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2d993-2733">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="2d993-2733">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2d993-2734">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2734">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2d993-2735">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="2d993-2735">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2d993-2736">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="2d993-2736">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2d993-2737">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="2d993-2737">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d993-2738">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2738">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2d993-2739">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-2739">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2d993-2740">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="2d993-2740">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2d993-2741">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2741">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2d993-2742">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="2d993-2742">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d993-2743">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2743">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2d993-2744">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-2744">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2d993-2745">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2745">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2d993-2746">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="2d993-2746">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2d993-2747">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="2d993-2747">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2d993-2748">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2748">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2d993-2749">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="2d993-2749">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2d993-2750">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="2d993-2750">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2d993-2751">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="2d993-2751">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2d993-2752">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="2d993-2752">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2d993-2753">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-2753">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2d993-2754">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="2d993-2754">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2d993-2755">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2755">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2d993-2756">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2756">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2d993-2757">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-2757">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2d993-2758">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="2d993-2758">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2d993-2759">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2759">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2d993-2760">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2760">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2d993-2761">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="2d993-2761">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2d993-2762">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-2762">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2d993-2763">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2d993-2763">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2d993-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2d993-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2d993-2765">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="2d993-2765">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2d993-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2d993-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2d993-2767">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-2767">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2d993-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2d993-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2d993-2769">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="2d993-2769">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2d993-2770">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="2d993-2770">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2d993-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2d993-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2d993-2772">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="2d993-2772">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="2d993-2773">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-2773">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2d993-2774">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="2d993-2774">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-2775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-2775">Az.Automation</span></span>
* <span data-ttu-id="2d993-2776">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="2d993-2776">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2d993-2777">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="2d993-2777">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2d993-2778">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="2d993-2778">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2d993-2779">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="2d993-2779">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2d993-2780">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="2d993-2780">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2d993-2781">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="2d993-2781">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2d993-2782">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="2d993-2782">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2783">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2783">Az.Compute</span></span>
* <span data-ttu-id="2d993-2784">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-2784">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2d993-2785">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2d993-2785">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-2786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-2786">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-2787">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-2787">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-2788">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-2788">Az.Monitor</span></span>
* <span data-ttu-id="2d993-2789">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="2d993-2789">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2790">Az.Network</span></span>
* <span data-ttu-id="2d993-2791">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2791">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2d993-2792">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="2d993-2792">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d993-2793">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="2d993-2793">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2d993-2794">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="2d993-2794">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2795">Az.Resources</span></span>
* <span data-ttu-id="2d993-2796">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="2d993-2796">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2797">Az.Sql</span></span>
* <span data-ttu-id="2d993-2798">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d993-2798">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2d993-2799">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2799">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-2800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2800">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2801">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="2d993-2801">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-2802">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2802">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-2803">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="2d993-2803">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2d993-2804">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2d993-2804">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2805">Az.Compute</span></span>
* <span data-ttu-id="2d993-2806">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="2d993-2806">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2d993-2807">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2d993-2807">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2d993-2808">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-2808">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2d993-2809">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2d993-2809">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2d993-2810">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2d993-2810">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2d993-2811">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-2811">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="2d993-2812">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="2d993-2812">Breaking changes</span></span>
    - <span data-ttu-id="2d993-2813">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2d993-2813">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2d993-2814">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="2d993-2814">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2d993-2815">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2d993-2815">Az.DeploymentManager</span></span>
* <span data-ttu-id="2d993-2816">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="2d993-2816">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2d993-2817">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2d993-2817">Az.Dns</span></span>
* <span data-ttu-id="2d993-2818">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="2d993-2818">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2d993-2819">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2819">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2d993-2820">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="2d993-2820">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d993-2821">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-2821">Az.FrontDoor</span></span>
* <span data-ttu-id="2d993-2822">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="2d993-2822">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2d993-2823">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="2d993-2823">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2d993-2824">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-2824">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-2825">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="2d993-2825">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2d993-2826">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d993-2826">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2d993-2827">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d993-2827">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2d993-2828">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="2d993-2828">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2d993-2829">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="2d993-2829">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2d993-2830">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="2d993-2830">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2d993-2831">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="2d993-2831">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-2832">Az.Monitor</span></span>
* <span data-ttu-id="2d993-2833">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="2d993-2833">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="2d993-2834">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2d993-2834">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2d993-2835">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2d993-2835">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2d993-2836">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2d993-2836">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2d993-2837">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2d993-2837">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2d993-2838">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2d993-2838">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2d993-2839">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2d993-2839">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2d993-2840">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2840">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d993-2841">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2841">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d993-2842">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2842">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d993-2843">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2843">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d993-2844">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d993-2844">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d993-2845">См. подробнее об [API SQR](/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="2d993-2845">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2d993-2846">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="2d993-2846">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2847">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2847">Az.Network</span></span>
* <span data-ttu-id="2d993-2848">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="2d993-2848">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2d993-2849">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2849">New cmdlets</span></span>
        - <span data-ttu-id="2d993-2850">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-2850">New-AzNatGateway</span></span>
        - <span data-ttu-id="2d993-2851">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-2851">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2d993-2852">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-2852">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2d993-2853">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-2853">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2d993-2854">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="2d993-2854">Updated cmdlets</span></span>
        - <span data-ttu-id="2d993-2855">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2d993-2855">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2d993-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2d993-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2d993-2857">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="2d993-2857">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2d993-2858">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2858">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2d993-2859">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2859">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-2860">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2860">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-2861">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2861">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2d993-2862">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2d993-2862">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2d993-2863">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="2d993-2863">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2864">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2864">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2865">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d993-2865">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2d993-2866">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d993-2866">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2d993-2867">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d993-2867">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2d993-2868">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="2d993-2868">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2d993-2869">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="2d993-2869">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2d993-2870">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="2d993-2870">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2d993-2871">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2d993-2871">Az.Relay</span></span>
* <span data-ttu-id="2d993-2872">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2872">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d993-2873">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d993-2873">Az.ServiceBus</span></span>
* <span data-ttu-id="2d993-2874">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2d993-2874">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-2875">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-2875">Az.Storage</span></span>
* <span data-ttu-id="2d993-2876">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="2d993-2876">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2d993-2877">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-2877">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2d993-2878">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2d993-2878">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2d993-2879">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2879">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d993-2880">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="2d993-2880">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2d993-2881">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2881">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2d993-2882">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2882">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2d993-2883">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-2883">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2884">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2884">Az.Websites</span></span>
* <span data-ttu-id="2d993-2885">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="2d993-2885">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2d993-2886">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="2d993-2886">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2d993-2887">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2887">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d993-2888">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-2888">Highlights since the last major release</span></span>
* <span data-ttu-id="2d993-2889">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="2d993-2889">General availability of `Az` module</span></span>
* <span data-ttu-id="2d993-2890">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d993-2890">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d993-2891">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d993-2891">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d993-2892">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="2d993-2892">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d993-2893">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2d993-2893">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d993-2894">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="2d993-2894">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d993-2895">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="2d993-2895">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-2896">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2896">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2897">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="2d993-2897">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d993-2898">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-2898">Az.Batch</span></span>
* <span data-ttu-id="2d993-2899">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2899">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-2900">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-2900">Az.Cdn</span></span>
* <span data-ttu-id="2d993-2901">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-2902">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2902">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-2903">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2904">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2904">Az.Compute</span></span>
* <span data-ttu-id="2d993-2905">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="2d993-2905">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2d993-2906">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d993-2907">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2d993-2907">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-2908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-2908">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-2909">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2d993-2909">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-2910">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-2910">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-2911">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d993-2912">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d993-2912">Az.EventGrid</span></span>
* <span data-ttu-id="2d993-2913">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="2d993-2913">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-2914">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2914">Az.EventHub</span></span>
* <span data-ttu-id="2d993-2915">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2d993-2915">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d993-2916">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d993-2916">Az.HDInsight</span></span>
* <span data-ttu-id="2d993-2917">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2917">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-2918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-2918">Az.IotHub</span></span>
* <span data-ttu-id="2d993-2919">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2919">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-2920">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-2920">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-2921">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2921">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d993-2922">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2d993-2922">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2d993-2923">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d993-2923">Az.MachineLearning</span></span>
* <span data-ttu-id="2d993-2924">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2924">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2d993-2925">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2d993-2925">Az.Media</span></span>
* <span data-ttu-id="2d993-2926">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-2927">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-2927">Az.Monitor</span></span>
  * <span data-ttu-id="2d993-2928">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="2d993-2928">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2d993-2929">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2d993-2929">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2d993-2930">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2d993-2930">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2d993-2931">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d993-2931">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2d993-2932">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d993-2932">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2d993-2933">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d993-2933">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2d993-2934">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-2934">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-2935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-2935">Az.Network</span></span>
* <span data-ttu-id="2d993-2936">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d993-2937">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2d993-2937">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2d993-2938">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2d993-2938">Az.NotificationHubs</span></span>
* <span data-ttu-id="2d993-2939">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-2940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-2940">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-2941">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2d993-2942">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d993-2942">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d993-2943">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2943">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-2944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2944">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-2945">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d993-2946">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2946">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2d993-2947">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2947">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2d993-2948">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="2d993-2948">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d993-2949">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d993-2949">Az.RedisCache</span></span>
* <span data-ttu-id="2d993-2950">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2951">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2951">Az.Resources</span></span>
* <span data-ttu-id="2d993-2952">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2d993-2952">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2953">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2953">Az.Sql</span></span>
* <span data-ttu-id="2d993-2954">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="2d993-2954">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2d993-2955">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2955">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d993-2956">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2956">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2d993-2957">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="2d993-2957">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2d993-2958">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2958">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2d993-2959">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2d993-2959">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2d993-2960">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="2d993-2960">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-2961">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-2961">Az.Websites</span></span>
* <span data-ttu-id="2d993-2962">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="2d993-2962">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2d993-2963">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="2d993-2963">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d993-2964">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2964">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2d993-2965">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2d993-2965">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2d993-2966">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-2966">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d993-2967">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-2967">Highlights since the last major release</span></span>
* <span data-ttu-id="2d993-2968">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="2d993-2968">General availability of `Az` module</span></span>
* <span data-ttu-id="2d993-2969">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d993-2969">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d993-2970">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d993-2970">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d993-2971">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="2d993-2971">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d993-2972">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2d993-2972">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d993-2973">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="2d993-2973">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d993-2974">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="2d993-2974">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d993-2975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-2975">Az.Accounts</span></span>
* <span data-ttu-id="2d993-2976">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="2d993-2976">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d993-2977">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d993-2977">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d993-2978">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2d993-2978">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2d993-2979">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="2d993-2979">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-2980">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-2980">Az.Automation</span></span>
* <span data-ttu-id="2d993-2981">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="2d993-2981">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2d993-2982">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="2d993-2982">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2d993-2983">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-2983">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-2984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-2984">Az.Compute</span></span>
* <span data-ttu-id="2d993-2985">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="2d993-2985">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d993-2986">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="2d993-2986">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2d993-2987">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d993-2987">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d993-2988">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="2d993-2988">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-2989">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-2989">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-2990">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="2d993-2990">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2d993-2991">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-2991">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-2992">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-2992">Az.Resources</span></span>
* <span data-ttu-id="2d993-2993">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="2d993-2993">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2d993-2994">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-2994">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2d993-2995">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="2d993-2995">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2d993-2996">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="2d993-2996">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2d993-2997">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="2d993-2997">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2d993-2998">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="2d993-2998">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-2999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-2999">Az.Sql</span></span>
* <span data-ttu-id="2d993-3000">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-3000">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-3001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-3001">Az.Storage</span></span>
* <span data-ttu-id="2d993-3002">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3002">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2d993-3003">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d993-3003">New-AzStorageContext</span></span>
* <span data-ttu-id="2d993-3004">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="2d993-3004">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2d993-3005">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-3005">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2d993-3006">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-3006">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2d993-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2d993-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2d993-3009">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3009">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2d993-3010">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-3010">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2d993-3011">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d993-3011">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2d993-3012">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d993-3012">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2d993-3013">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d993-3013">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2d993-3014">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3014">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d993-3015">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="2d993-3015">Highlights since the last major release</span></span>
* <span data-ttu-id="2d993-3016">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="2d993-3016">General availability of `Az` module</span></span>
* <span data-ttu-id="2d993-3017">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d993-3017">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d993-3018">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d993-3018">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d993-3019">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="2d993-3019">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d993-3020">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2d993-3020">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d993-3021">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="2d993-3021">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d993-3022">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="2d993-3022">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-3023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-3023">Az.Automation</span></span>
* <span data-ttu-id="2d993-3024">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="2d993-3024">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2d993-3025">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="2d993-3025">Dynamic grouping</span></span>
    * <span data-ttu-id="2d993-3026">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="2d993-3026">Pre-Post script</span></span>
    * <span data-ttu-id="2d993-3027">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3027">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3028">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3028">Az.Compute</span></span>
* <span data-ttu-id="2d993-3029">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="2d993-3029">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2d993-3030">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-3030">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-3031">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-3031">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-3032">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d993-3032">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-3033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3033">Az.Network</span></span>
* <span data-ttu-id="2d993-3034">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3034">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2d993-3035">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d993-3035">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-3036">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3036">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-3037">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d993-3037">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2d993-3038">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="2d993-3038">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3039">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3039">Az.Resources</span></span>
* <span data-ttu-id="2d993-3040">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-3040">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2d993-3041">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="2d993-3041">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-3042">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3042">Az.Sql</span></span>
* <span data-ttu-id="2d993-3043">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="2d993-3043">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-3044">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-3044">Az.Storage</span></span>
* <span data-ttu-id="2d993-3045">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-3045">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2d993-3046">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-3046">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d993-3047">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-3047">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d993-3048">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d993-3048">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d993-3049">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2d993-3049">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2d993-3050">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2d993-3050">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2d993-3051">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2d993-3051">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-3052">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-3052">Az.Websites</span></span>
* <span data-ttu-id="2d993-3053">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="2d993-3053">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="2d993-3054">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3054">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-3055">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-3055">Az.Accounts</span></span>
* <span data-ttu-id="2d993-3056">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="2d993-3056">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2d993-3057">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="2d993-3057">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-3058">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-3058">Az.Automation</span></span>
* <span data-ttu-id="2d993-3059">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3059">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d993-3060">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3060">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2d993-3061">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="2d993-3061">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-3062">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-3062">Az.Cdn</span></span>
* <span data-ttu-id="2d993-3063">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="2d993-3063">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3064">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3064">Az.Compute</span></span>
* <span data-ttu-id="2d993-3065">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="2d993-3065">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-3066">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-3066">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-3067">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="2d993-3067">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d993-3068">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d993-3068">Az.LogicApp</span></span>
* <span data-ttu-id="2d993-3069">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="2d993-3069">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-3070">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3070">Az.Network</span></span>
* <span data-ttu-id="2d993-3071">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="2d993-3071">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-3072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3072">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-3073">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3073">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2d993-3074">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="2d993-3074">SDK Update</span></span>
* <span data-ttu-id="2d993-3075">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="2d993-3075">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2d993-3076">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="2d993-3076">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3077">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3077">Az.Resources</span></span>
* <span data-ttu-id="2d993-3078">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="2d993-3078">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2d993-3079">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="2d993-3079">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2d993-3080">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="2d993-3080">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2d993-3081">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="2d993-3081">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2d993-3082">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="2d993-3082">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2d993-3083">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="2d993-3083">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-3084">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3084">Az.Sql</span></span>
* <span data-ttu-id="2d993-3085">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="2d993-3085">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2d993-3086">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="2d993-3086">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-3087">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-3087">Az.Storage</span></span>
* <span data-ttu-id="2d993-3088">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2d993-3088">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2d993-3089">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3089">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2d993-3090">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3090">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d993-3091">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="2d993-3091">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-3092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-3092">Az.Automation</span></span>
* <span data-ttu-id="2d993-3093">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-3093">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2d993-3094">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-3094">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2d993-3095">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-3095">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-3096">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3096">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-3097">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d993-3097">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3098">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3098">Az.Compute</span></span>
* <span data-ttu-id="2d993-3099">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="2d993-3099">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2d993-3100">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="2d993-3100">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2d993-3101">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2d993-3101">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2d993-3102">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2d993-3102">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-3103">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-3103">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-3104">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="2d993-3104">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d993-3105">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d993-3105">Az.EventHub</span></span>
* <span data-ttu-id="2d993-3106">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="2d993-3106">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-3107">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-3107">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-3108">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="2d993-3108">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d993-3109">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d993-3109">Az.LogicApp</span></span>
* <span data-ttu-id="2d993-3110">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="2d993-3110">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2d993-3111">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-3111">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2d993-3112">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="2d993-3112">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2d993-3113">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="2d993-3113">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d993-3114">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="2d993-3114">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d993-3115">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="2d993-3115">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d993-3116">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="2d993-3116">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2d993-3117">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="2d993-3117">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2d993-3118">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2d993-3118">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d993-3119">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2d993-3119">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d993-3120">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="2d993-3120">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d993-3121">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d993-3121">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2d993-3122">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-3122">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d993-3123">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-3123">Az.Monitor</span></span>
* <span data-ttu-id="2d993-3124">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="2d993-3124">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-3125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3125">Az.Network</span></span>
* <span data-ttu-id="2d993-3126">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="2d993-3126">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-3127">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-3127">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d993-3128">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2d993-3128">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2d993-3129">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2d993-3129">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="2d993-3130">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="2d993-3130">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3131">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3131">Az.Resources</span></span>
* <span data-ttu-id="2d993-3132">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="2d993-3132">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d993-3133">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="2d993-3133">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2d993-3134">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="2d993-3134">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2d993-3135">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="2d993-3135">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-3136">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3136">Az.Sql</span></span>
* <span data-ttu-id="2d993-3137">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-3137">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2d993-3138">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="2d993-3138">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-3139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-3139">Az.Websites</span></span>
* <span data-ttu-id="2d993-3140">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="2d993-3140">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2d993-3141">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3141">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-3142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-3142">Az.Accounts</span></span>
* <span data-ttu-id="2d993-3143">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d993-3143">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d993-3144">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3144">Az.AnalysisServices</span></span>
<span data-ttu-id="2d993-3145">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="2d993-3145">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3146">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3146">Az.Compute</span></span>
* <span data-ttu-id="2d993-3147">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="2d993-3147">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2d993-3148">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="2d993-3148">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2d993-3149">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="2d993-3149">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-3150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3150">Az.RecoveryServices</span></span>
<span data-ttu-id="2d993-3151">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="2d993-3151">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3152">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3152">Az.Resources</span></span>
* <span data-ttu-id="2d993-3153">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3153">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="2d993-3154">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="2d993-3154">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d993-3155">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="2d993-3155">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="2d993-3156">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="2d993-3156">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-3157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3157">Az.Sql</span></span>
* <span data-ttu-id="2d993-3158">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d993-3158">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2d993-3159">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3159">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2d993-3160">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="2d993-3160">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2d993-3161">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3161">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-3162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-3162">Az.Accounts</span></span>
* <span data-ttu-id="2d993-3163">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="2d993-3163">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d993-3164">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3164">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d993-3165">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="2d993-3165">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-3166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3166">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d993-3167">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="2d993-3167">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2d993-3168">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3168">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-3169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-3169">Az.Accounts</span></span>
* <span data-ttu-id="2d993-3170">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="2d993-3170">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d993-3171">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3171">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d993-3172">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="2d993-3172">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d993-3173">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d993-3173">Az.Aks</span></span>
* <span data-ttu-id="2d993-3174">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3174">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d993-3175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-3175">Az.Automation</span></span>
* <span data-ttu-id="2d993-3176">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="2d993-3176">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2d993-3177">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3177">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d993-3178">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d993-3178">Az.Cdn</span></span>
* <span data-ttu-id="2d993-3179">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3179">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3180">Az.Compute</span></span>
* <span data-ttu-id="2d993-3181">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="2d993-3181">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2d993-3182">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-3182">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2d993-3183">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d993-3183">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d993-3184">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d993-3184">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d993-3185">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3185">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d993-3186">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d993-3186">Az.DataFactory</span></span>
* <span data-ttu-id="2d993-3187">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-3187">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-3188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-3188">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-3189">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="2d993-3189">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2d993-3190">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="2d993-3190">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2d993-3191">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3191">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-3192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-3192">Az.IotHub</span></span>
* <span data-ttu-id="2d993-3193">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2d993-3193">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d993-3194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-3194">Az.KeyVault</span></span>
* <span data-ttu-id="2d993-3195">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3195">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-3196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3196">Az.Network</span></span>
* <span data-ttu-id="2d993-3197">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3197">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3198">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3198">Az.Resources</span></span>
* <span data-ttu-id="2d993-3199">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="2d993-3199">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2d993-3200">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3200">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2d993-3201">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2d993-3201">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2d993-3202">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="2d993-3202">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2d993-3203">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="2d993-3203">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2d993-3204">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-3204">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2d993-3205">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="2d993-3205">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-3206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-3206">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-3207">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="2d993-3207">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2d993-3208">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2d993-3208">Fix some error messages.</span></span>
* <span data-ttu-id="2d993-3209">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="2d993-3209">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2d993-3210">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="2d993-3210">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d993-3211">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d993-3211">Az.SignalR</span></span>
* <span data-ttu-id="2d993-3212">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3212">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-3213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3213">Az.Sql</span></span>
* <span data-ttu-id="2d993-3214">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3214">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d993-3215">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="2d993-3215">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2d993-3216">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="2d993-3216">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2d993-3217">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="2d993-3217">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-3218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-3218">Az.Storage</span></span>
* <span data-ttu-id="2d993-3219">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3219">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d993-3220">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="2d993-3220">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2d993-3221">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-3221">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2d993-3222">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2d993-3222">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2d993-3223">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d993-3223">Az.TrafficManager</span></span>
* <span data-ttu-id="2d993-3224">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3224">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-3225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-3225">Az.Websites</span></span>
* <span data-ttu-id="2d993-3226">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d993-3227">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="2d993-3227">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2d993-3228">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="2d993-3228">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2d993-3229">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3229">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d993-3230">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-3230">Az.Accounts</span></span>
* <span data-ttu-id="2d993-3231">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="2d993-3231">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3232">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3232">Az.Compute</span></span>
* <span data-ttu-id="2d993-3233">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="2d993-3233">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2d993-3234">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="2d993-3234">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2d993-3235">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2d993-3235">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-3236">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-3236">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-3237">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="2d993-3237">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2d993-3238">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3238">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d993-3239">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d993-3239">Az.EventGrid</span></span>
* <span data-ttu-id="2d993-3240">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-3240">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2d993-3241">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2d993-3241">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2d993-3242">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="2d993-3242">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d993-3243">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="2d993-3243">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d993-3244">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="2d993-3244">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d993-3245">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="2d993-3245">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2d993-3246">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="2d993-3246">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d993-3247">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="2d993-3247">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d993-3248">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="2d993-3248">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d993-3249">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="2d993-3249">Dead letter endpoint.</span></span>
* <span data-ttu-id="2d993-3250">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2d993-3250">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2d993-3251">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="2d993-3251">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d993-3252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d993-3252">Az.IotHub</span></span>
* <span data-ttu-id="2d993-3253">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="2d993-3253">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d993-3254">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d993-3254">Az.LogicApp</span></span>
* <span data-ttu-id="2d993-3255">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="2d993-3255">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3256">Az.Resources</span></span>
* <span data-ttu-id="2d993-3257">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="2d993-3257">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2d993-3258">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="2d993-3258">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2d993-3259">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2d993-3259">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d993-3260">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d993-3260">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2d993-3261">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="2d993-3261">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2d993-3262">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="2d993-3262">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d993-3263">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d993-3263">Az.SignalR</span></span>
* <span data-ttu-id="2d993-3264">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2d993-3264">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-3265">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3265">Az.Sql</span></span>
* <span data-ttu-id="2d993-3266">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="2d993-3266">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d993-3267">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-3267">Az.Storage</span></span>
* <span data-ttu-id="2d993-3268">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="2d993-3268">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2d993-3269">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d993-3269">New-AzStorageContext</span></span>
* <span data-ttu-id="2d993-3270">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2d993-3270">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2d993-3271">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d993-3271">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-3272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-3272">Az.Websites</span></span>
* <span data-ttu-id="2d993-3273">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="2d993-3273">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2d993-3274">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2d993-3274">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2d993-3275">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3275">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2d993-3276">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-3276">General</span></span>

- <span data-ttu-id="2d993-3277">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="2d993-3277">General Availability of Az Module</span></span>
- <span data-ttu-id="2d993-3278">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="2d993-3278">Online help for each module</span></span>
- <span data-ttu-id="2d993-3279">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="2d993-3279">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2d993-3280">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3280">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2d993-3281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d993-3281">Az.Accounts</span></span>
- <span data-ttu-id="2d993-3282">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="2d993-3282">Changed from Az.Profile</span></span>
- <span data-ttu-id="2d993-3283">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="2d993-3283">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d993-3284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-3284">Az.ApiManagement</span></span>
- <span data-ttu-id="2d993-3285">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="2d993-3285">Fixes for #7002</span></span>
- <span data-ttu-id="2d993-3286">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2d993-3287">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d993-3287">Az.Batch</span></span>
- <span data-ttu-id="2d993-3288">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2d993-3288">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2d993-3289">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="2d993-3289">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2d993-3290">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3290">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2d993-3291">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d993-3291">Az.Billing</span></span>
- <span data-ttu-id="2d993-3292">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="2d993-3292">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2d993-3293">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3293">Az.CognitivServices</span></span>
- <span data-ttu-id="2d993-3294">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="2d993-3294">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2d993-3295">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2d993-3295">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d993-3296">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d993-3296">Az.ContainerInstance</span></span>
- <span data-ttu-id="2d993-3297">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="2d993-3297">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2d993-3298">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d993-3298">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2d993-3299">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d993-3300">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-3300">Az.DataLakeStore</span></span>
- <span data-ttu-id="2d993-3301">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2d993-3302">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d993-3302">Az.Monitor</span></span>
- <span data-ttu-id="2d993-3303">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3303">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2d993-3304">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d993-3304">Az.KeyVault</span></span>
- <span data-ttu-id="2d993-3305">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="2d993-3305">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2d993-3306">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d993-3306">Az.MachineLearning</span></span>
- <span data-ttu-id="2d993-3307">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2d993-3307">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2d993-3308">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2d993-3308">Az.Media</span></span>
- <span data-ttu-id="2d993-3309">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d993-3309">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d993-3310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3310">Az.Network</span></span>
<span data-ttu-id="2d993-3311">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="2d993-3311">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2d993-3312">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-3312">New cmdlets added:</span></span>
        - <span data-ttu-id="2d993-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d993-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d993-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d993-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d993-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d993-3318">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2d993-3318">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2d993-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2d993-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2d993-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d993-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2d993-3321">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d993-3321">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2d993-3322">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d993-3322">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2d993-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d993-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d993-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d993-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d993-3325">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-3325">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2d993-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2d993-3327">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d993-3327">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2d993-3328">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d993-3328">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2d993-3329">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-3329">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d993-3330">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-3330">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d993-3331">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-3331">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2d993-3332">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d993-3332">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2d993-3333">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2d993-3334">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-3334">Az.OperationalInsights</span></span>
- <span data-ttu-id="2d993-3335">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3335">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2d993-3336">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d993-3336">Az.Profile</span></span>
- <span data-ttu-id="2d993-3337">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="2d993-3337">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-3338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3338">Az.RecoveryServices</span></span>
- <span data-ttu-id="2d993-3339">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2d993-3340">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3340">Az.Resources</span></span>
- <span data-ttu-id="2d993-3341">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d993-3342">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-3342">Az.ServiceFabric</span></span>
- <span data-ttu-id="2d993-3343">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="2d993-3343">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2d993-3344">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3344">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2d993-3345">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d993-3345">Az.SIgnalR</span></span>
- <span data-ttu-id="2d993-3346">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d993-3346">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2d993-3347">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3347">Az.Sql</span></span>
- <span data-ttu-id="2d993-3348">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="2d993-3348">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2d993-3349">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3349">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2d993-3350">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3350">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d993-3351">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-3351">Az.Storage</span></span>
- <span data-ttu-id="2d993-3352">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3352">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d993-3353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-3353">Az.Websites</span></span>
- <span data-ttu-id="2d993-3354">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="2d993-3354">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2d993-3355">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3355">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2d993-3356">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-3356">General</span></span>

* <span data-ttu-id="2d993-3357">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="2d993-3357">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d993-3358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3358">Az.Compute</span></span>

* <span data-ttu-id="2d993-3359">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="2d993-3359">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d993-3360">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-3360">Az.DataLakeStore</span></span>

* <span data-ttu-id="2d993-3361">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="2d993-3361">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2d993-3362">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d993-3362">Az.FrontDoor</span></span>

* <span data-ttu-id="2d993-3363">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="2d993-3363">Fixed some broken links</span></span>
    - <span data-ttu-id="2d993-3364">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-3364">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2d993-3365">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2d993-3365">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d993-3366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3366">Az.RecoveryServices</span></span>

* <span data-ttu-id="2d993-3367">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3367">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2d993-3368">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="2d993-3368">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d993-3369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3369">Az.Resources</span></span>

* <span data-ttu-id="2d993-3370">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="2d993-3370">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2d993-3371">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3371">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2d993-3372">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3372">Az.Sql</span></span>

* <span data-ttu-id="2d993-3373">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="2d993-3373">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2d993-3374">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="2d993-3374">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2d993-3375">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="2d993-3375">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d993-3376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d993-3376">Az.Storage</span></span>

* <span data-ttu-id="2d993-3377">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-3377">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2d993-3378">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="2d993-3378">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2d993-3379">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-3379">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d993-3380">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="2d993-3380">Support Static Website configuration</span></span>
    - <span data-ttu-id="2d993-3381">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d993-3381">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2d993-3382">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d993-3382">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d993-3383">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-3383">Az.Websites</span></span>

* <span data-ttu-id="2d993-3384">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2d993-3384">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="2d993-3385">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="2d993-3385">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2d993-3386">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3386">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2d993-3387">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3387">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d993-3388">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d993-3388">Az.ApiManagement</span></span>
* <span data-ttu-id="2d993-3389">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3389">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2d993-3390">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d993-3390">Az.Automation</span></span>
* <span data-ttu-id="2d993-3391">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="2d993-3391">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d993-3392">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="2d993-3392">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2d993-3393">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="2d993-3393">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2d993-3394">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="2d993-3394">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2d993-3395">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="2d993-3395">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d993-3396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3396">Az.Compute</span></span>
* <span data-ttu-id="2d993-3397">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="2d993-3397">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2d993-3398">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3398">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d993-3399">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d993-3399">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d993-3400">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3400">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2d993-3401">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d993-3401">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d993-3402">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2d993-3402">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d993-3403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3403">Az.Network</span></span>
* <span data-ttu-id="2d993-3404">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="2d993-3404">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2d993-3405">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3405">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2d993-3406">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="2d993-3406">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="2d993-3407">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d993-3407">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2d993-3408">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d993-3408">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d993-3409">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2d993-3409">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2d993-3410">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="2d993-3410">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2d993-3411">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2d993-3411">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2d993-3412">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="2d993-3412">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2d993-3413">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3413">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2d993-3414">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2d993-3414">Az.Relay</span></span>
* <span data-ttu-id="2d993-3415">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="2d993-3415">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d993-3416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3416">Az.Resources</span></span>
* <span data-ttu-id="2d993-3417">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="2d993-3417">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2d993-3418">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="2d993-3418">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2d993-3419">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="2d993-3419">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d993-3420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-3420">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-3421">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="2d993-3421">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2d993-3422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3422">Az.Sql</span></span>
* <span data-ttu-id="2d993-3423">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3423">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2d993-3424">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2d993-3424">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d993-3425">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2d993-3425">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d993-3426">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2d993-3426">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d993-3427">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="2d993-3427">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d993-3428">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-3428">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d993-3429">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-3429">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d993-3430">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-3430">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d993-3431">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d993-3431">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2d993-3432">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d993-3432">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2d993-3433">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="2d993-3433">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2d993-3434">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3434">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2d993-3435">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d993-3435">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d993-3436">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d993-3436">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d993-3437">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d993-3437">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2d993-3438">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d993-3438">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2d993-3439">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="2d993-3439">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2d993-3440">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3440">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d993-3441">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2d993-3441">General</span></span>
* <span data-ttu-id="2d993-3442">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="2d993-3442">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2d993-3443">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d993-3443">Az.Profile</span></span>
* <span data-ttu-id="2d993-3444">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="2d993-3444">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2d993-3445">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="2d993-3445">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2d993-3446">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2d993-3446">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2d993-3447">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="2d993-3447">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2d993-3448">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="2d993-3448">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2d993-3449">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="2d993-3449">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2d993-3450">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="2d993-3450">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-3451">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3451">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-3452">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2d993-3452">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3453">Az.Compute</span></span>
* <span data-ttu-id="2d993-3454">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d993-3454">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2d993-3455">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2d993-3455">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2d993-3456">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2d993-3456">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-3457">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-3457">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-3458">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2d993-3458">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2d993-3459">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="2d993-3459">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2d993-3460">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2d993-3460">Az.Insights</span></span>
* <span data-ttu-id="2d993-3461">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="2d993-3461">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2d993-3462">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="2d993-3462">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2d993-3463">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="2d993-3463">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2d993-3464">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="2d993-3464">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-3465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3465">Az.Network</span></span>
* <span data-ttu-id="2d993-3466">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="2d993-3466">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2d993-3467">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-3467">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2d993-3468">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2d993-3468">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2d993-3469">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d993-3469">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2d993-3470">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2d993-3470">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2d993-3471">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d993-3471">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2d993-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d993-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d993-3473">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d993-3473">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d993-3474">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="2d993-3474">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3475">Az.Resources</span></span>
* <span data-ttu-id="2d993-3476">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="2d993-3476">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2d993-3477">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2d993-3477">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d993-3478">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d993-3478">Az.ServiceBus</span></span>
* <span data-ttu-id="2d993-3479">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="2d993-3479">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d993-3480">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d993-3480">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d993-3481">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="2d993-3481">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2d993-3482">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2d993-3482">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2d993-3483">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2d993-3483">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2d993-3484">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2d993-3484">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2d993-3485">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2d993-3485">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2d993-3486">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3486">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2d993-3487">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d993-3487">Az.Profile</span></span>
* <span data-ttu-id="2d993-3488">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="2d993-3488">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2d993-3489">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="2d993-3489">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3490">Az.Compute</span></span>
* <span data-ttu-id="2d993-3491">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="2d993-3491">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2d993-3492">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2d993-3492">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d993-3493">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d993-3493">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d993-3494">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="2d993-3494">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2d993-3495">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d993-3495">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2d993-3496">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d993-3496">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d993-3497">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d993-3497">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d993-3498">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d993-3498">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-3499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3499">Az.Network</span></span>
* <span data-ttu-id="2d993-3500">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="2d993-3500">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2d993-3501">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2d993-3501">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3502">Az.Resources</span></span>
* <span data-ttu-id="2d993-3503">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="2d993-3503">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2d993-3504">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="2d993-3504">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2d993-3505">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3505">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2d993-3506">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="2d993-3506">Azure.Storage</span></span>
* <span data-ttu-id="2d993-3507">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="2d993-3507">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2d993-3508">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-3508">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2d993-3509">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d993-3509">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d993-3510">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="2d993-3510">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2d993-3511">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2d993-3511">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d993-3512">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d993-3512">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d993-3513">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2d993-3513">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d993-3514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d993-3514">Az.Compute</span></span>
* <span data-ttu-id="2d993-3515">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="2d993-3515">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2d993-3516">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d993-3516">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2d993-3517">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3517">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2d993-3518">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d993-3518">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2d993-3519">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="2d993-3519">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d993-3520">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d993-3520">Az.Network</span></span>
* <span data-ttu-id="2d993-3521">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="2d993-3521">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2d993-3522">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="2d993-3522">new cmdlets added</span></span>
    - <span data-ttu-id="2d993-3523">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d993-3523">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d993-3524">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d993-3524">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d993-3525">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d993-3525">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d993-3526">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d993-3526">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d993-3527">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-3527">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2d993-3528">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-3528">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2d993-3529">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="2d993-3529">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2d993-3530">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2d993-3530">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2d993-3531">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2d993-3531">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d993-3532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d993-3532">Az.RedisCache</span></span>
* <span data-ttu-id="2d993-3533">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="2d993-3533">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2d993-3534">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="2d993-3534">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d993-3535">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d993-3535">Az.Resources</span></span>
* <span data-ttu-id="2d993-3536">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d993-3536">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d993-3537">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="2d993-3537">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d993-3538">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d993-3538">Az.Sql</span></span>
* <span data-ttu-id="2d993-3539">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="2d993-3539">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d993-3540">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d993-3540">Az.Websites</span></span>
* <span data-ttu-id="2d993-3541">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="2d993-3541">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2d993-3542">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="2d993-3542">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2d993-3543">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="2d993-3543">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2d993-3544">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="2d993-3544">Initial Release</span></span>
