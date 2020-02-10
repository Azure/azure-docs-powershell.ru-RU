---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002679"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6621b-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6621b-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="6621b-104">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6621b-105">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6621b-105">Highlights since the last major release</span></span>
* <span data-ttu-id="6621b-106">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6621b-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="6621b-107">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="6621b-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6621b-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-108">Az.Accounts</span></span>
* <span data-ttu-id="6621b-109">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="6621b-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="6621b-110">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="6621b-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6621b-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-111">Az.ApiManagement</span></span>
* <span data-ttu-id="6621b-112">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="6621b-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="6621b-113">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="6621b-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="6621b-114">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="6621b-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="6621b-115">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="6621b-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-116">Az.Compute</span></span>
* <span data-ttu-id="6621b-117">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6621b-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="6621b-118">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6621b-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="6621b-119">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="6621b-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="6621b-121">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-122">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-123">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6621b-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6621b-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="6621b-125">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="6621b-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="6621b-126">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="6621b-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6621b-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6621b-127">Az.HDInsight</span></span>
* <span data-ttu-id="6621b-128">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="6621b-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6621b-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-129">Az.KeyVault</span></span>
* <span data-ttu-id="6621b-130">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6621b-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-131">Az.Network</span></span>
* <span data-ttu-id="6621b-132">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="6621b-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="6621b-133">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="6621b-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="6621b-134">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6621b-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6621b-135">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="6621b-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="6621b-136">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="6621b-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="6621b-137">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="6621b-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="6621b-138">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="6621b-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="6621b-139">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="6621b-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="6621b-140">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-140">New cmdlets added:</span></span>
        - <span data-ttu-id="6621b-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6621b-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="6621b-142">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6621b-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="6621b-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6621b-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="6621b-144">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="6621b-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6621b-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="6621b-146">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="6621b-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="6621b-147">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="6621b-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="6621b-148">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="6621b-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="6621b-149">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="6621b-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-151">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="6621b-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="6621b-152">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6621b-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-153">Az.Resources</span></span>
* <span data-ttu-id="6621b-154">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="6621b-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="6621b-155">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="6621b-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-156">Az.Sql</span></span>
<span data-ttu-id="6621b-157">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="6621b-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-158">Az.Storage</span></span>
* <span data-ttu-id="6621b-159">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6621b-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="6621b-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="6621b-161">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="6621b-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="6621b-162">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6621b-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-163">Az.Websites</span></span>
* <span data-ttu-id="6621b-164">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="6621b-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="6621b-165">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6621b-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="6621b-166">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-167">Az.Accounts</span></span>
* <span data-ttu-id="6621b-168">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="6621b-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6621b-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6621b-169">Az.Cdn</span></span>
* <span data-ttu-id="6621b-170">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6621b-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-171">Az.Compute</span></span>
* <span data-ttu-id="6621b-172">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="6621b-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6621b-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6621b-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="6621b-174">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6621b-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6621b-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6621b-176">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6621b-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6621b-177">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="6621b-178">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6621b-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6621b-179">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="6621b-180">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6621b-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6621b-181">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="6621b-182">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="6621b-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6621b-183">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="6621b-184">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="6621b-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6621b-185">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="6621b-186">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="6621b-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6621b-187">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="6621b-188">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="6621b-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6621b-189">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="6621b-190">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="6621b-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="6621b-191">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="6621b-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="6621b-192">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="6621b-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="6621b-193">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="6621b-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-194">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-195">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6621b-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="6621b-196">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="6621b-197">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="6621b-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="6621b-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6621b-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="6621b-199">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6621b-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6621b-200">Az.EventHub</span></span>
* <span data-ttu-id="6621b-201">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="6621b-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6621b-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6621b-202">Az.HDInsight</span></span>
* <span data-ttu-id="6621b-203">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6621b-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6621b-204">Az.MachineLearning</span></span>
* <span data-ttu-id="6621b-205">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="6621b-206">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6621b-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="6621b-207">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="6621b-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="6621b-208">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6621b-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="6621b-209">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6621b-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="6621b-210">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="6621b-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="6621b-211">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="6621b-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="6621b-212">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="6621b-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-213">Az.Network</span></span>
* <span data-ttu-id="6621b-214">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="6621b-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-216">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="6621b-217">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6621b-218">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6621b-219">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-220">Az.Resources</span></span>
* <span data-ttu-id="6621b-221">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="6621b-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-222">Az.Sql</span></span>
* <span data-ttu-id="6621b-223">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6621b-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="6621b-224">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="6621b-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6621b-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6621b-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6621b-226">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="6621b-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-227">Az.Storage</span></span>
* <span data-ttu-id="6621b-228">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="6621b-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="6621b-229">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="6621b-230">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="6621b-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="6621b-231">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="6621b-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="6621b-232">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="6621b-233">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6621b-233">General</span></span>
* <span data-ttu-id="6621b-234">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="6621b-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6621b-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-235">Az.Accounts</span></span>
* <span data-ttu-id="6621b-236">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="6621b-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="6621b-237">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="6621b-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6621b-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6621b-238">Az.Batch</span></span>
* <span data-ttu-id="6621b-239">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="6621b-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-240">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-241">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6621b-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6621b-242">Az.FrontDoor</span></span>
* <span data-ttu-id="6621b-243">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="6621b-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="6621b-244">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="6621b-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6621b-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6621b-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="6621b-246">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="6621b-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6621b-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-247">Az.KeyVault</span></span>
* <span data-ttu-id="6621b-248">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="6621b-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="6621b-249">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="6621b-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="6621b-250">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6621b-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6621b-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-251">Az.Monitor</span></span>
* <span data-ttu-id="6621b-252">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="6621b-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="6621b-253">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="6621b-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="6621b-254">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="6621b-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-255">Az.Network</span></span>
* <span data-ttu-id="6621b-256">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="6621b-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-257">Az.Resources</span></span>
* <span data-ttu-id="6621b-258">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="6621b-259">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="6621b-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-260">Az.Sql</span></span>
* <span data-ttu-id="6621b-261">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="6621b-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-262">Az.Storage</span></span>
* <span data-ttu-id="6621b-263">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="6621b-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="6621b-264">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="6621b-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="6621b-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6621b-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="6621b-266">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="6621b-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="6621b-267">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="6621b-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="6621b-268">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6621b-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="6621b-269">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="6621b-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="6621b-270">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6621b-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="6621b-271">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6621b-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="6621b-272">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="6621b-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="6621b-273">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="6621b-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="6621b-274">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="6621b-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="6621b-275">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="6621b-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="6621b-276">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6621b-277">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6621b-277">Highlights since the last major release</span></span>
* <span data-ttu-id="6621b-278">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6621b-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6621b-279">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6621b-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-280">Az.Compute</span></span>
* <span data-ttu-id="6621b-281">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6621b-281">VM Reapply feature</span></span>
    - <span data-ttu-id="6621b-282">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6621b-283">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="6621b-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6621b-284">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6621b-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6621b-285">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6621b-286">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6621b-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6621b-287">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="6621b-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6621b-288">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="6621b-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6621b-289">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="6621b-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6621b-290">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="6621b-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6621b-291">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6621b-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6621b-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6621b-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6621b-293">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="6621b-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6621b-294">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="6621b-294">Get the Order</span></span>
* <span data-ttu-id="6621b-295">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="6621b-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6621b-296">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="6621b-296">Create new Order</span></span>
* <span data-ttu-id="6621b-297">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="6621b-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6621b-298">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="6621b-298">Remove the Order</span></span>
* <span data-ttu-id="6621b-299">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="6621b-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6621b-300">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="6621b-300">Now creates Local Share</span></span>
* <span data-ttu-id="6621b-301">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="6621b-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6621b-302">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="6621b-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6621b-303">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="6621b-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6621b-304">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6621b-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6621b-305">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="6621b-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6621b-306">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="6621b-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="6621b-307">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="6621b-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6621b-308">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="6621b-308">Create new Triggers</span></span>
* <span data-ttu-id="6621b-309">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="6621b-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6621b-310">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="6621b-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-311">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-312">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6621b-313">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="6621b-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-315">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="6621b-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6621b-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6621b-316">Az.EventHub</span></span>
* <span data-ttu-id="6621b-317">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="6621b-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6621b-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6621b-318">Az.FrontDoor</span></span>
* <span data-ttu-id="6621b-319">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="6621b-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6621b-320">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6621b-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6621b-321">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="6621b-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6621b-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6621b-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-323">Az.Network</span></span>
* <span data-ttu-id="6621b-324">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6621b-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6621b-325">Az.PrivateDns</span></span>
* <span data-ttu-id="6621b-326">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6621b-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-328">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="6621b-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6621b-329">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="6621b-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6621b-330">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="6621b-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6621b-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6621b-331">Az.RedisCache</span></span>
* <span data-ttu-id="6621b-332">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="6621b-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6621b-333">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="6621b-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6621b-334">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="6621b-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-335">Az.Resources</span></span>
- <span data-ttu-id="6621b-336">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="6621b-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6621b-337">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="6621b-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="6621b-338">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="6621b-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6621b-339">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="6621b-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6621b-340">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="6621b-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-341">Az.Sql</span></span>
* <span data-ttu-id="6621b-342">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6621b-343">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="6621b-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6621b-344">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6621b-345">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6621b-345">General</span></span>
* <span data-ttu-id="6621b-346">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6621b-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6621b-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-347">Az.Accounts</span></span>
* <span data-ttu-id="6621b-348">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="6621b-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6621b-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6621b-349">Az.Advisor</span></span>
* <span data-ttu-id="6621b-350">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="6621b-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6621b-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6621b-351">Az.Batch</span></span>
* <span data-ttu-id="6621b-352">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6621b-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6621b-353">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6621b-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6621b-354">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="6621b-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="6621b-355">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="6621b-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6621b-356">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6621b-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6621b-357">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6621b-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6621b-358">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="6621b-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6621b-359">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="6621b-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6621b-360">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="6621b-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6621b-361">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6621b-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6621b-362">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="6621b-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="6621b-363">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="6621b-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6621b-364">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6621b-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6621b-365">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="6621b-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6621b-366">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="6621b-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6621b-367">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="6621b-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6621b-368">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6621b-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6621b-369">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6621b-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6621b-370">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="6621b-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="6621b-371">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6621b-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="6621b-372">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6621b-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6621b-373">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6621b-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6621b-374">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="6621b-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6621b-375">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="6621b-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="6621b-376">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="6621b-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6621b-377">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="6621b-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="6621b-378">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="6621b-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6621b-379">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="6621b-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="6621b-380">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="6621b-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6621b-381">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="6621b-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6621b-382">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="6621b-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6621b-383">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="6621b-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6621b-384">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="6621b-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6621b-385">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="6621b-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6621b-386">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="6621b-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6621b-387">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="6621b-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6621b-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6621b-388">Az.Cdn</span></span>
* <span data-ttu-id="6621b-389">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="6621b-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6621b-390">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="6621b-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-391">Az.Compute</span></span>
* <span data-ttu-id="6621b-392">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="6621b-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6621b-393">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6621b-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6621b-394">Добавлен параметр ProximityPlacementGroupId в следующие командлеты: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6621b-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="6621b-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6621b-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6621b-396">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6621b-397">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6621b-398">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="6621b-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6621b-399">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6621b-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6621b-400">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="6621b-400">Breaking changes</span></span>
    - <span data-ttu-id="6621b-401">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="6621b-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6621b-402">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6621b-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-403">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-404">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-406">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="6621b-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6621b-407">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="6621b-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6621b-408">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="6621b-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6621b-409">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="6621b-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6621b-410">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="6621b-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6621b-411">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="6621b-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6621b-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6621b-412">Az.FrontDoor</span></span>
* <span data-ttu-id="6621b-413">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="6621b-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6621b-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6621b-414">Az.HDInsight</span></span>
* <span data-ttu-id="6621b-415">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="6621b-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6621b-416">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6621b-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6621b-417">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="6621b-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6621b-418">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="6621b-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6621b-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6621b-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6621b-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6621b-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6621b-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6621b-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6621b-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6621b-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6621b-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6621b-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6621b-424">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="6621b-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="6621b-425">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6621b-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6621b-426">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6621b-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6621b-427">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6621b-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6621b-428">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="6621b-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6621b-429">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="6621b-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6621b-430">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="6621b-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6621b-431">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="6621b-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6621b-432">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="6621b-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6621b-433">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="6621b-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6621b-434">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="6621b-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6621b-435">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="6621b-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="6621b-436">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="6621b-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6621b-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6621b-437">Az.IotHub</span></span>
* <span data-ttu-id="6621b-438">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="6621b-438">Breaking changes:</span></span>
    - <span data-ttu-id="6621b-439">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6621b-440">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6621b-441">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6621b-442">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6621b-443">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="6621b-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6621b-444">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="6621b-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6621b-445">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="6621b-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6621b-446">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="6621b-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6621b-447">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6621b-448">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6621b-449">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6621b-450">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="6621b-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-452">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6621b-453">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6621b-454">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6621b-455">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6621b-456">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6621b-457">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6621b-458">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6621b-459">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6621b-460">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="6621b-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-461">Az.Resources</span></span>
* <span data-ttu-id="6621b-462">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="6621b-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-463">Az.Network</span></span>
* <span data-ttu-id="6621b-464">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="6621b-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6621b-465">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6621b-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="6621b-466">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-467">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-468">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-469">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6621b-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6621b-471">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="6621b-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6621b-472">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="6621b-472">New cmdlet:</span></span>
        - <span data-ttu-id="6621b-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6621b-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6621b-474">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="6621b-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6621b-475">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6621b-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6621b-476">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6621b-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6621b-477">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="6621b-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6621b-478">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="6621b-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6621b-479">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="6621b-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6621b-480">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6621b-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6621b-481">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-481">New cmdlets added:</span></span>
        - <span data-ttu-id="6621b-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6621b-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6621b-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6621b-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6621b-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6621b-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6621b-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6621b-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6621b-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6621b-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6621b-487">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="6621b-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6621b-488">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6621b-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6621b-489">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="6621b-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6621b-490">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="6621b-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6621b-491">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6621b-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6621b-492">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6621b-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6621b-493">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6621b-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6621b-494">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-494">New cmdlets added:</span></span>
        - <span data-ttu-id="6621b-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6621b-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6621b-496">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6621b-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6621b-497">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6621b-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6621b-498">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6621b-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6621b-499">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6621b-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6621b-500">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6621b-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6621b-501">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6621b-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6621b-502">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="6621b-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6621b-503">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-503">New cmdlets added:</span></span>
        - <span data-ttu-id="6621b-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6621b-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6621b-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6621b-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6621b-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6621b-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6621b-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6621b-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6621b-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6621b-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6621b-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6621b-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6621b-510">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6621b-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6621b-511">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="6621b-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6621b-512">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="6621b-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6621b-513">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="6621b-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6621b-514">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="6621b-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6621b-515">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="6621b-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6621b-516">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6621b-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6621b-517">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6621b-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6621b-518">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="6621b-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6621b-519">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="6621b-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6621b-520">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="6621b-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6621b-521">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-521">New cmdlets added:</span></span>
        - <span data-ttu-id="6621b-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6621b-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="6621b-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6621b-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6621b-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6621b-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6621b-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6621b-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6621b-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-527">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="6621b-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-528">Az.Sql</span></span>
* <span data-ttu-id="6621b-529">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="6621b-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6621b-530">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="6621b-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6621b-531">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="6621b-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6621b-532">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="6621b-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6621b-533">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="6621b-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6621b-534">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6621b-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6621b-535">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="6621b-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6621b-536">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="6621b-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="6621b-537">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-538">Az.Storage</span></span>
* <span data-ttu-id="6621b-539">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6621b-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6621b-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6621b-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6621b-542">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="6621b-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6621b-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6621b-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6621b-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6621b-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="6621b-545">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6621b-546">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6621b-546">General</span></span>
* <span data-ttu-id="6621b-547">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6621b-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6621b-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-548">Az.Accounts</span></span>
* <span data-ttu-id="6621b-549">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="6621b-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6621b-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-550">Az.ApiManagement</span></span>
* <span data-ttu-id="6621b-551">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="6621b-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6621b-552">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="6621b-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-553">Az.Automation</span></span>
* <span data-ttu-id="6621b-554">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="6621b-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="6621b-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6621b-555">Az.Batch</span></span>
* <span data-ttu-id="6621b-556">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-557">Az.Compute</span></span>
* <span data-ttu-id="6621b-558">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="6621b-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6621b-559">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="6621b-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6621b-560">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="6621b-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="6621b-561">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="6621b-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-562">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-563">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="6621b-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6621b-564">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="6621b-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6621b-565">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-567">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="6621b-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6621b-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6621b-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="6621b-569">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6621b-570">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="6621b-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6621b-571">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="6621b-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6621b-572">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="6621b-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6621b-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6621b-573">Az.IotHub</span></span>
* <span data-ttu-id="6621b-574">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="6621b-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6621b-575">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="6621b-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="6621b-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-576">Az.Monitor</span></span>
* <span data-ttu-id="6621b-577">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="6621b-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6621b-578">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="6621b-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6621b-579">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="6621b-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6621b-580">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6621b-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-581">Az.Network</span></span>
* <span data-ttu-id="6621b-582">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="6621b-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6621b-583">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="6621b-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6621b-584">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-584">New cmdlets added:</span></span>
        - <span data-ttu-id="6621b-585">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="6621b-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6621b-586">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6621b-587">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="6621b-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6621b-588">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="6621b-589">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6621b-590">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6621b-591">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6621b-592">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="6621b-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6621b-593">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6621b-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6621b-594">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6621b-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6621b-595">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="6621b-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6621b-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6621b-596">Az.RedisCache</span></span>
* <span data-ttu-id="6621b-597">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="6621b-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-598">Az.Sql</span></span>
* <span data-ttu-id="6621b-599">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="6621b-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-600">Az.Storage</span></span>
* <span data-ttu-id="6621b-601">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6621b-602">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="6621b-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6621b-603">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6621b-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6621b-604">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="6621b-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6621b-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6621b-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6621b-606">Az.StorageSync</span></span>
* <span data-ttu-id="6621b-607">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="6621b-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-608">Az.Websites</span></span>
* <span data-ttu-id="6621b-609">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="6621b-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6621b-610">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6621b-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-611">Az.ApiManagement</span></span>
* <span data-ttu-id="6621b-612">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="6621b-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6621b-613">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="6621b-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6621b-614">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6621b-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-615">Az.Automation</span></span>
* <span data-ttu-id="6621b-616">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="6621b-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6621b-617">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="6621b-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6621b-618">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="6621b-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-619">Az.Compute</span></span>
* <span data-ttu-id="6621b-620">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6621b-621">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6621b-622">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="6621b-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6621b-623">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="6621b-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6621b-624">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="6621b-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6621b-625">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="6621b-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6621b-626">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="6621b-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6621b-627">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="6621b-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6621b-628">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-629">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-630">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="6621b-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6621b-631">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="6621b-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6621b-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6621b-632">Az.HDInsight</span></span>
* <span data-ttu-id="6621b-633">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="6621b-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6621b-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6621b-634">Az.IotHub</span></span>
* <span data-ttu-id="6621b-635">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="6621b-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6621b-636">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="6621b-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6621b-637">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-637">New cmdlets are:</span></span>
    - <span data-ttu-id="6621b-638">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="6621b-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6621b-639">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="6621b-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6621b-640">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="6621b-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6621b-641">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="6621b-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6621b-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-642">Az.Monitor</span></span>
* <span data-ttu-id="6621b-643">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="6621b-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6621b-644">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="6621b-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6621b-645">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="6621b-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6621b-646">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="6621b-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="6621b-647">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="6621b-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6621b-648">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="6621b-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="6621b-649">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="6621b-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6621b-650">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="6621b-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6621b-651">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="6621b-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6621b-652">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="6621b-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6621b-653">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="6621b-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6621b-654">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="6621b-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6621b-655">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="6621b-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6621b-656">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="6621b-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6621b-657">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="6621b-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6621b-658">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="6621b-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6621b-659">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="6621b-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6621b-660">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="6621b-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6621b-661">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6621b-662">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="6621b-662">Overall improved help files</span></span>
* <span data-ttu-id="6621b-663">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="6621b-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-664">Az.Network</span></span>
* <span data-ttu-id="6621b-665">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="6621b-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="6621b-666">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="6621b-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6621b-667">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="6621b-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6621b-668">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="6621b-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6621b-669">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="6621b-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6621b-670">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="6621b-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6621b-671">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="6621b-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6621b-672">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="6621b-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6621b-673">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="6621b-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6621b-674">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="6621b-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6621b-675">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6621b-676">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="6621b-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6621b-677">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-677">New cmdlets</span></span>
        - <span data-ttu-id="6621b-678">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="6621b-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6621b-679">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="6621b-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6621b-680">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6621b-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="6621b-681">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="6621b-681">New-VpnSite</span></span>
        - <span data-ttu-id="6621b-682">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="6621b-682">Update-VpnSite</span></span>
        - <span data-ttu-id="6621b-683">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="6621b-683">New-VpnConnection</span></span>
        - <span data-ttu-id="6621b-684">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-684">Update-VpnConnection</span></span>
* <span data-ttu-id="6621b-685">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="6621b-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-687">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="6621b-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6621b-688">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6621b-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-689">Az.Resources</span></span>
* <span data-ttu-id="6621b-690">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="6621b-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6621b-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-692">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="6621b-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6621b-693">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="6621b-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6621b-694">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6621b-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6621b-695">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="6621b-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6621b-696">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="6621b-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6621b-697">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="6621b-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6621b-698">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6621b-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6621b-699">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6621b-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6621b-700">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="6621b-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6621b-701">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="6621b-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6621b-702">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="6621b-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6621b-703">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="6621b-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6621b-704">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="6621b-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6621b-705">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="6621b-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6621b-706">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="6621b-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6621b-707">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6621b-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6621b-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6621b-708">Az.SignalR</span></span>
* <span data-ttu-id="6621b-709">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="6621b-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-710">Az.Sql</span></span>
* <span data-ttu-id="6621b-711">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="6621b-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6621b-712">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="6621b-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6621b-713">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6621b-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6621b-714">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="6621b-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6621b-715">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="6621b-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-716">Az.Storage</span></span>
* <span data-ttu-id="6621b-717">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="6621b-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6621b-718">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="6621b-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6621b-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6621b-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6621b-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6621b-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6621b-721">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="6621b-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6621b-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6621b-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6621b-723">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="6621b-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6621b-724">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6621b-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6621b-725">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6621b-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6621b-726">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="6621b-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6621b-727">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="6621b-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-728">Az.Websites</span></span>
* <span data-ttu-id="6621b-729">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="6621b-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6621b-730">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="6621b-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6621b-731">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="6621b-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6621b-732">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6621b-733">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6621b-733">General</span></span>
* <span data-ttu-id="6621b-734">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="6621b-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6621b-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-735">Az.Accounts</span></span>
* <span data-ttu-id="6621b-736">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="6621b-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6621b-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6621b-737">Az.Aks</span></span>
* <span data-ttu-id="6621b-738">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="6621b-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6621b-739">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="6621b-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6621b-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-740">Az.ApiManagement</span></span>
* <span data-ttu-id="6621b-741">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="6621b-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6621b-742">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="6621b-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6621b-743">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="6621b-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6621b-744">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="6621b-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6621b-745">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="6621b-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6621b-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6621b-746">Az.Batch</span></span>
* <span data-ttu-id="6621b-747">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="6621b-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6621b-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6621b-748">Az.Cdn</span></span>
* <span data-ttu-id="6621b-749">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="6621b-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-750">Az.Compute</span></span>
* <span data-ttu-id="6621b-751">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6621b-752">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6621b-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6621b-753">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6621b-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6621b-754">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6621b-755">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6621b-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6621b-756">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6621b-757">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6621b-758">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="6621b-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-759">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-760">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="6621b-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6621b-761">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="6621b-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6621b-762">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="6621b-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6621b-763">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="6621b-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-765">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="6621b-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6621b-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6621b-766">Az.EventHub</span></span>
* <span data-ttu-id="6621b-767">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6621b-768">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="6621b-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6621b-769">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="6621b-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6621b-770">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="6621b-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6621b-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6621b-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6621b-772">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="6621b-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6621b-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-773">Az.Monitor</span></span>
* <span data-ttu-id="6621b-774">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="6621b-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-775">Az.Network</span></span>
* <span data-ttu-id="6621b-776">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6621b-777">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="6621b-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6621b-778">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="6621b-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6621b-779">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6621b-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6621b-780">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="6621b-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="6621b-781">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="6621b-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6621b-782">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="6621b-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6621b-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="6621b-784">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="6621b-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6621b-785">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="6621b-785">Added example</span></span>
    - <span data-ttu-id="6621b-786">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="6621b-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6621b-787">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="6621b-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6621b-788">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="6621b-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-790">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-791">Az.Resources</span></span>
* <span data-ttu-id="6621b-792">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="6621b-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6621b-793">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="6621b-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6621b-794">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="6621b-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6621b-795">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="6621b-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6621b-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6621b-796">Az.ServiceBus</span></span>
* <span data-ttu-id="6621b-797">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6621b-798">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="6621b-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6621b-799">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="6621b-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="6621b-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-801">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="6621b-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6621b-802">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6621b-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6621b-803">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="6621b-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6621b-804">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="6621b-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6621b-805">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="6621b-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6621b-806">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="6621b-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-807">Az.Sql</span></span>
* <span data-ttu-id="6621b-808">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="6621b-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-809">Az.Storage</span></span>
* <span data-ttu-id="6621b-810">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="6621b-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6621b-811">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6621b-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6621b-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6621b-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6621b-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6621b-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6621b-814">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6621b-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6621b-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6621b-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-816">Az.Websites</span></span>
* <span data-ttu-id="6621b-817">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="6621b-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6621b-818">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-819">Az.Accounts</span></span>
* <span data-ttu-id="6621b-820">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6621b-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6621b-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6621b-822">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="6621b-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="6621b-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-823">Az.Automation</span></span>
* <span data-ttu-id="6621b-824">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="6621b-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6621b-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6621b-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="6621b-826">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-827">Az.Compute</span></span>
* <span data-ttu-id="6621b-828">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6621b-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6621b-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6621b-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6621b-830">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="6621b-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6621b-831">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="6621b-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-832">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-833">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6621b-834">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="6621b-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6621b-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6621b-835">Az.EventHub</span></span>
* <span data-ttu-id="6621b-836">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="6621b-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6621b-837">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="6621b-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6621b-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-838">Az.KeyVault</span></span>
* <span data-ttu-id="6621b-839">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6621b-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6621b-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6621b-840">Az.LogicApp</span></span>
* <span data-ttu-id="6621b-841">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="6621b-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6621b-842">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="6621b-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6621b-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6621b-843">Az.ManagedServices</span></span>
* <span data-ttu-id="6621b-844">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="6621b-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-845">Az.Network</span></span>
* <span data-ttu-id="6621b-846">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="6621b-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6621b-847">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-847">New cmdlets</span></span>
        - <span data-ttu-id="6621b-848">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6621b-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6621b-849">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="6621b-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6621b-850">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-851">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-852">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-853">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6621b-854">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="6621b-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6621b-855">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="6621b-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6621b-856">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6621b-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6621b-857">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6621b-858">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="6621b-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6621b-859">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="6621b-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6621b-860">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="6621b-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6621b-861">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="6621b-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6621b-862">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-862">Updated cmdlets</span></span>
        - <span data-ttu-id="6621b-863">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6621b-864">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6621b-865">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6621b-866">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="6621b-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6621b-867">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6621b-868">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6621b-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="6621b-869">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6621b-870">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6621b-871">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="6621b-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6621b-872">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="6621b-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6621b-873">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="6621b-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6621b-874">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="6621b-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6621b-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="6621b-876">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="6621b-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="6621b-877">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="6621b-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-879">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6621b-880">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6621b-881">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6621b-882">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6621b-883">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6621b-884">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6621b-885">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6621b-886">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6621b-887">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6621b-888">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="6621b-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-889">Az.Resources</span></span>
- <span data-ttu-id="6621b-890">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6621b-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6621b-891">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6621b-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6621b-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6621b-892">Az.ServiceBus</span></span>
* <span data-ttu-id="6621b-893">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="6621b-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6621b-894">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="6621b-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-895">Az.Sql</span></span>
* <span data-ttu-id="6621b-896">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="6621b-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6621b-897">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6621b-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6621b-898">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="6621b-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-899">Az.Storage</span></span>
* <span data-ttu-id="6621b-900">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6621b-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6621b-901">Az.StorageSync</span></span>
* <span data-ttu-id="6621b-902">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="6621b-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6621b-903">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="6621b-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-904">Az.Websites</span></span>
* <span data-ttu-id="6621b-905">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="6621b-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6621b-906">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="6621b-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6621b-907">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="6621b-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6621b-908">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-909">Az.Accounts</span></span>
* <span data-ttu-id="6621b-910">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="6621b-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6621b-911">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="6621b-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6621b-912">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="6621b-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6621b-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6621b-913">Az.Advisor</span></span>
* <span data-ttu-id="6621b-914">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="6621b-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6621b-915">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="6621b-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6621b-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-916">Az.ApiManagement</span></span>
* <span data-ttu-id="6621b-917">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="6621b-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6621b-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6621b-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6621b-919">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="6621b-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6621b-920">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="6621b-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6621b-921">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="6621b-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6621b-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6621b-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6621b-923">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="6621b-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-924">Az.Automation</span></span>
* <span data-ttu-id="6621b-925">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="6621b-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-926">Az.Compute</span></span>
* <span data-ttu-id="6621b-927">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="6621b-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-928">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-929">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="6621b-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6621b-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6621b-930">Az.EventGrid</span></span>
* <span data-ttu-id="6621b-931">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6621b-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6621b-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6621b-932">Az.IotHub</span></span>
* <span data-ttu-id="6621b-933">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="6621b-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-934">Az.Network</span></span>
* <span data-ttu-id="6621b-935">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="6621b-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6621b-936">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="6621b-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6621b-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="6621b-938">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="6621b-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6621b-939">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="6621b-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6621b-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="6621b-941">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="6621b-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-943">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="6621b-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-944">Az.Resources</span></span>
    - <span data-ttu-id="6621b-945">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="6621b-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6621b-946">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="6621b-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6621b-947">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="6621b-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6621b-948">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="6621b-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6621b-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6621b-949">Az.ServiceBus</span></span>
* <span data-ttu-id="6621b-950">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="6621b-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-951">Az.Sql</span></span>
* <span data-ttu-id="6621b-952">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6621b-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6621b-953">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="6621b-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6621b-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6621b-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6621b-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6621b-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6621b-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6621b-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6621b-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6621b-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6621b-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6621b-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6621b-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6621b-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6621b-960">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6621b-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-961">Az.Storage</span></span>
* <span data-ttu-id="6621b-962">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="6621b-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6621b-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6621b-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6621b-964">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="6621b-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6621b-965">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6621b-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6621b-966">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="6621b-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6621b-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6621b-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6621b-969">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="6621b-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6621b-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6621b-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6621b-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6621b-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6621b-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6621b-972">Az.StorageSync</span></span>
* <span data-ttu-id="6621b-973">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="6621b-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6621b-974">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-975">Az.Accounts</span></span>
* <span data-ttu-id="6621b-976">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="6621b-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6621b-977">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="6621b-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6621b-978">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="6621b-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6621b-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="6621b-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6621b-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="6621b-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-981">Az.Compute</span></span>
* <span data-ttu-id="6621b-982">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6621b-983">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6621b-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6621b-984">Az.Dns</span></span>
* <span data-ttu-id="6621b-985">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="6621b-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6621b-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6621b-986">Az.EventGrid</span></span>
* <span data-ttu-id="6621b-987">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6621b-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6621b-988">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-988">New cmdlets:</span></span>
    - <span data-ttu-id="6621b-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6621b-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6621b-990">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6621b-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6621b-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6621b-992">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6621b-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6621b-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6621b-994">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6621b-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6621b-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6621b-996">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6621b-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6621b-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6621b-998">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6621b-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6621b-999">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6621b-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6621b-1000">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6621b-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6621b-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6621b-1002">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="6621b-1003">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6621b-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6621b-1004">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6621b-1005">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="6621b-1006">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6621b-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6621b-1007">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6621b-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6621b-1008">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6621b-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6621b-1009">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="6621b-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6621b-1010">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6621b-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6621b-1011">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="6621b-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6621b-1012">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="6621b-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6621b-1013">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6621b-1014">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="6621b-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="6621b-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6621b-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6621b-1016">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6621b-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6621b-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6621b-1018">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6621b-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6621b-1019">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6621b-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6621b-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6621b-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="6621b-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6621b-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6621b-1022">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="6621b-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6621b-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6621b-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6621b-1024">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1025">Az.Network</span></span>
* <span data-ttu-id="6621b-1026">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6621b-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6621b-1027">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-1027">New cmdlets</span></span>
        - <span data-ttu-id="6621b-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6621b-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6621b-1029">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="6621b-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6621b-1030">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-1030">New cmdlets</span></span> 
        - <span data-ttu-id="6621b-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6621b-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6621b-1032">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="6621b-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6621b-1033">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-1033">New cmdlets</span></span> 
        - <span data-ttu-id="6621b-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6621b-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="6621b-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6621b-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6621b-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6621b-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6621b-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6621b-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6621b-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6621b-1039">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6621b-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6621b-1040">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-1040">New cmdlets</span></span>
        - <span data-ttu-id="6621b-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6621b-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6621b-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6621b-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6621b-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6621b-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6621b-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6621b-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6621b-1045">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6621b-1046">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6621b-1047">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6621b-1048">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="6621b-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6621b-1049">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="6621b-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6621b-1050">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="6621b-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6621b-1051">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6621b-1052">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="6621b-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6621b-1053">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6621b-1054">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="6621b-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6621b-1055">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6621b-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6621b-1056">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="6621b-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6621b-1057">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="6621b-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6621b-1058">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6621b-1059">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6621b-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6621b-1060">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6621b-1061">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6621b-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6621b-1062">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6621b-1063">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="6621b-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="6621b-1064">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6621b-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="6621b-1065">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="6621b-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6621b-1066">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="6621b-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6621b-1067">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="6621b-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6621b-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="6621b-1069">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6621b-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1070">Az.Resources</span></span>
* <span data-ttu-id="6621b-1071">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="6621b-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6621b-1072">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="6621b-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6621b-1073">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="6621b-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6621b-1074">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6621b-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-1076">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6621b-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1077">Az.Sql</span></span>
* <span data-ttu-id="6621b-1078">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="6621b-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6621b-1079">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="6621b-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6621b-1080">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6621b-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6621b-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6621b-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6621b-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6621b-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6621b-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6621b-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6621b-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6621b-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6621b-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6621b-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1086">Az.Storage</span></span>
* <span data-ttu-id="6621b-1087">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6621b-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="6621b-1089">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6621b-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6621b-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1091">Az.Websites</span></span>
* <span data-ttu-id="6621b-1092">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6621b-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6621b-1093">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="6621b-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6621b-1094">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6621b-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6621b-1095">Az.Cdn</span></span>
* <span data-ttu-id="6621b-1096">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="6621b-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1097">Az.Compute</span></span>
* <span data-ttu-id="6621b-1098">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6621b-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6621b-1099">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6621b-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6621b-1100">Az.EventHub</span></span>
* <span data-ttu-id="6621b-1101">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="6621b-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6621b-1102">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6621b-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1103">Az.Network</span></span>
* <span data-ttu-id="6621b-1104">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6621b-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6621b-1105">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="6621b-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6621b-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="6621b-1107">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="6621b-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-1109">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="6621b-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6621b-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6621b-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="6621b-1111">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6621b-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6621b-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-1113">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="6621b-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6621b-1114">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6621b-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1115">Az.Sql</span></span>
* <span data-ttu-id="6621b-1116">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6621b-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6621b-1117">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="6621b-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6621b-1118">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="6621b-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6621b-1119">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="6621b-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1120">Az.Websites</span></span>
* <span data-ttu-id="6621b-1121">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="6621b-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6621b-1122">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6621b-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="6621b-1124">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6621b-1125">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6621b-1126">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6621b-1127">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="6621b-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6621b-1128">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="6621b-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6621b-1129">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="6621b-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6621b-1130">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6621b-1131">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6621b-1132">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6621b-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6621b-1133">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="6621b-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6621b-1134">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6621b-1135">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="6621b-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6621b-1136">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="6621b-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6621b-1137">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6621b-1138">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6621b-1139">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6621b-1140">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6621b-1141">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6621b-1142">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="6621b-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="6621b-1143">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="6621b-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6621b-1144">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="6621b-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6621b-1145">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="6621b-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6621b-1146">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="6621b-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6621b-1147">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6621b-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="6621b-1148">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="6621b-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6621b-1149">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="6621b-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6621b-1150">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="6621b-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6621b-1151">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6621b-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6621b-1152">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6621b-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6621b-1153">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6621b-1154">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6621b-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="6621b-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6621b-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6621b-1156">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6621b-1157">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="6621b-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6621b-1158">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6621b-1159">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="6621b-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6621b-1160">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6621b-1161">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="6621b-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6621b-1162">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="6621b-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6621b-1163">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="6621b-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="6621b-1164">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6621b-1165">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6621b-1166">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="6621b-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6621b-1167">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6621b-1168">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="6621b-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6621b-1169">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6621b-1170">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="6621b-1171">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6621b-1172">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="6621b-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6621b-1173">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="6621b-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6621b-1174">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6621b-1175">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="6621b-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6621b-1176">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="6621b-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6621b-1177">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="6621b-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6621b-1178">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="6621b-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6621b-1179">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="6621b-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6621b-1180">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="6621b-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6621b-1181">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6621b-1182">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6621b-1183">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6621b-1184">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="6621b-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6621b-1185">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6621b-1186">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6621b-1187">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6621b-1188">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6621b-1189">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6621b-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6621b-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6621b-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6621b-1191">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="6621b-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6621b-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6621b-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6621b-1193">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6621b-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6621b-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6621b-1195">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="6621b-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6621b-1196">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="6621b-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6621b-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6621b-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6621b-1198">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="6621b-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="6621b-1199">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6621b-1200">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="6621b-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-1201">Az.Automation</span></span>
* <span data-ttu-id="6621b-1202">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="6621b-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6621b-1203">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="6621b-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6621b-1204">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="6621b-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6621b-1205">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6621b-1206">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="6621b-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6621b-1207">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="6621b-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6621b-1208">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="6621b-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1209">Az.Compute</span></span>
* <span data-ttu-id="6621b-1210">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6621b-1211">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6621b-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-1213">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6621b-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-1214">Az.Monitor</span></span>
* <span data-ttu-id="6621b-1215">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="6621b-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1216">Az.Network</span></span>
* <span data-ttu-id="6621b-1217">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6621b-1218">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="6621b-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="6621b-1219">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="6621b-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6621b-1220">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="6621b-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1221">Az.Resources</span></span>
* <span data-ttu-id="6621b-1222">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1223">Az.Sql</span></span>
* <span data-ttu-id="6621b-1224">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6621b-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6621b-1225">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1226">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1227">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="6621b-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6621b-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="6621b-1229">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="6621b-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6621b-1230">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6621b-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1231">Az.Compute</span></span>
* <span data-ttu-id="6621b-1232">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="6621b-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6621b-1233">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6621b-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6621b-1234">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6621b-1235">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="6621b-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6621b-1236">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="6621b-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6621b-1237">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6621b-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="6621b-1238">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="6621b-1238">Breaking changes</span></span>
    - <span data-ttu-id="6621b-1239">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="6621b-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6621b-1240">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="6621b-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6621b-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6621b-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="6621b-1242">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="6621b-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6621b-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6621b-1243">Az.Dns</span></span>
* <span data-ttu-id="6621b-1244">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="6621b-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6621b-1245">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="6621b-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6621b-1246">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="6621b-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6621b-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6621b-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="6621b-1248">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="6621b-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6621b-1249">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="6621b-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6621b-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6621b-1250">Az.HDInsight</span></span>
* <span data-ttu-id="6621b-1251">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="6621b-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6621b-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6621b-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6621b-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6621b-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6621b-1254">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="6621b-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6621b-1255">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="6621b-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6621b-1256">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="6621b-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6621b-1257">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="6621b-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6621b-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-1258">Az.Monitor</span></span>
* <span data-ttu-id="6621b-1259">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="6621b-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="6621b-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6621b-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6621b-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6621b-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6621b-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6621b-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6621b-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6621b-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6621b-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6621b-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6621b-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6621b-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6621b-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6621b-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6621b-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6621b-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6621b-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6621b-1271">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="6621b-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6621b-1272">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="6621b-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1273">Az.Network</span></span>
* <span data-ttu-id="6621b-1274">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6621b-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6621b-1275">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-1275">New cmdlets</span></span>
        - <span data-ttu-id="6621b-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6621b-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="6621b-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6621b-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6621b-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6621b-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6621b-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6621b-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6621b-1280">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="6621b-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="6621b-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6621b-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6621b-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6621b-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6621b-1283">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="6621b-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6621b-1284">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6621b-1285">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6621b-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="6621b-1287">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6621b-1288">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="6621b-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6621b-1289">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="6621b-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-1291">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6621b-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6621b-1292">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6621b-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6621b-1293">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6621b-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6621b-1294">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="6621b-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6621b-1295">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="6621b-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6621b-1296">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="6621b-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6621b-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6621b-1297">Az.Relay</span></span>
* <span data-ttu-id="6621b-1298">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6621b-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6621b-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="6621b-1300">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6621b-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1301">Az.Storage</span></span>
* <span data-ttu-id="6621b-1302">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="6621b-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6621b-1303">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="6621b-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6621b-1304">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="6621b-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6621b-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="6621b-1306">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="6621b-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6621b-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6621b-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6621b-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1310">Az.Websites</span></span>
* <span data-ttu-id="6621b-1311">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="6621b-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6621b-1312">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="6621b-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6621b-1313">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6621b-1314">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6621b-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="6621b-1315">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="6621b-1316">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6621b-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6621b-1317">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6621b-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6621b-1318">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="6621b-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6621b-1319">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6621b-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6621b-1320">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="6621b-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6621b-1321">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="6621b-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6621b-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1322">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1323">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="6621b-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6621b-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6621b-1324">Az.Batch</span></span>
* <span data-ttu-id="6621b-1325">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6621b-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6621b-1326">Az.Cdn</span></span>
* <span data-ttu-id="6621b-1327">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6621b-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="6621b-1329">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1330">Az.Compute</span></span>
* <span data-ttu-id="6621b-1331">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="6621b-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6621b-1332">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6621b-1333">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6621b-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-1334">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-1335">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="6621b-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-1337">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6621b-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6621b-1338">Az.EventGrid</span></span>
* <span data-ttu-id="6621b-1339">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="6621b-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6621b-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6621b-1340">Az.EventHub</span></span>
* <span data-ttu-id="6621b-1341">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6621b-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="6621b-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6621b-1342">Az.HDInsight</span></span>
* <span data-ttu-id="6621b-1343">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6621b-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6621b-1344">Az.IotHub</span></span>
* <span data-ttu-id="6621b-1345">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6621b-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-1346">Az.KeyVault</span></span>
* <span data-ttu-id="6621b-1347">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6621b-1348">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6621b-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6621b-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6621b-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="6621b-1350">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6621b-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6621b-1351">Az.Media</span></span>
* <span data-ttu-id="6621b-1352">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6621b-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-1353">Az.Monitor</span></span>
  * <span data-ttu-id="6621b-1354">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="6621b-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6621b-1355">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6621b-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6621b-1356">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6621b-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6621b-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6621b-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6621b-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6621b-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6621b-1359">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6621b-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6621b-1360">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1361">Az.Network</span></span>
* <span data-ttu-id="6621b-1362">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6621b-1363">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6621b-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6621b-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6621b-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="6621b-1365">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6621b-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="6621b-1367">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6621b-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6621b-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6621b-1369">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-1371">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6621b-1372">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6621b-1373">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6621b-1374">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="6621b-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6621b-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6621b-1375">Az.RedisCache</span></span>
* <span data-ttu-id="6621b-1376">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1377">Az.Resources</span></span>
* <span data-ttu-id="6621b-1378">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6621b-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1379">Az.Sql</span></span>
* <span data-ttu-id="6621b-1380">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="6621b-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6621b-1381">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6621b-1382">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6621b-1383">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="6621b-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6621b-1384">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6621b-1385">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6621b-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6621b-1386">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="6621b-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1387">Az.Websites</span></span>
* <span data-ttu-id="6621b-1388">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="6621b-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6621b-1389">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="6621b-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6621b-1390">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6621b-1391">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="6621b-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6621b-1392">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6621b-1393">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6621b-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="6621b-1394">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="6621b-1395">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6621b-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6621b-1396">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6621b-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6621b-1397">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="6621b-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6621b-1398">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6621b-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6621b-1399">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="6621b-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6621b-1400">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="6621b-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6621b-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1401">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1402">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6621b-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="6621b-1404">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6621b-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6621b-1405">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-1406">Az.Automation</span></span>
* <span data-ttu-id="6621b-1407">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="6621b-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6621b-1408">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="6621b-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6621b-1409">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1410">Az.Compute</span></span>
* <span data-ttu-id="6621b-1411">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6621b-1412">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="6621b-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6621b-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="6621b-1414">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="6621b-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-1415">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-1416">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="6621b-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6621b-1417">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1418">Az.Resources</span></span>
* <span data-ttu-id="6621b-1419">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="6621b-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6621b-1420">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6621b-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6621b-1421">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="6621b-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6621b-1422">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="6621b-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6621b-1423">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="6621b-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6621b-1424">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="6621b-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1425">Az.Sql</span></span>
* <span data-ttu-id="6621b-1426">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1427">Az.Storage</span></span>
* <span data-ttu-id="6621b-1428">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6621b-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6621b-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="6621b-1430">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="6621b-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6621b-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6621b-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6621b-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6621b-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6621b-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6621b-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6621b-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6621b-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6621b-1435">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6621b-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6621b-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6621b-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6621b-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6621b-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6621b-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6621b-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6621b-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6621b-1440">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6621b-1441">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="6621b-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="6621b-1442">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="6621b-1443">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6621b-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6621b-1444">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6621b-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6621b-1445">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="6621b-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6621b-1446">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6621b-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6621b-1447">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="6621b-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6621b-1448">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="6621b-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-1449">Az.Automation</span></span>
* <span data-ttu-id="6621b-1450">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="6621b-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6621b-1451">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="6621b-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="6621b-1452">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="6621b-1452">Pre-Post script</span></span>
    * <span data-ttu-id="6621b-1453">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1454">Az.Compute</span></span>
* <span data-ttu-id="6621b-1455">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="6621b-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6621b-1456">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6621b-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-1457">Az.KeyVault</span></span>
* <span data-ttu-id="6621b-1458">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6621b-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1459">Az.Network</span></span>
* <span data-ttu-id="6621b-1460">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6621b-1461">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-1463">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="6621b-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6621b-1464">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="6621b-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1465">Az.Resources</span></span>
* <span data-ttu-id="6621b-1466">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6621b-1467">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="6621b-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1468">Az.Sql</span></span>
* <span data-ttu-id="6621b-1469">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1470">Az.Storage</span></span>
* <span data-ttu-id="6621b-1471">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6621b-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6621b-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6621b-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6621b-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6621b-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6621b-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6621b-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6621b-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6621b-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6621b-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6621b-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1478">Az.Websites</span></span>
* <span data-ttu-id="6621b-1479">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="6621b-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6621b-1480">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1481">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1482">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="6621b-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6621b-1483">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="6621b-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-1484">Az.Automation</span></span>
* <span data-ttu-id="6621b-1485">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6621b-1486">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6621b-1487">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="6621b-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6621b-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6621b-1488">Az.Cdn</span></span>
* <span data-ttu-id="6621b-1489">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="6621b-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1490">Az.Compute</span></span>
* <span data-ttu-id="6621b-1491">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="6621b-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-1492">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-1493">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="6621b-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6621b-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6621b-1494">Az.LogicApp</span></span>
* <span data-ttu-id="6621b-1495">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="6621b-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1496">Az.Network</span></span>
* <span data-ttu-id="6621b-1497">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="6621b-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-1499">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6621b-1500">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="6621b-1500">SDK Update</span></span>
* <span data-ttu-id="6621b-1501">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="6621b-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6621b-1502">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="6621b-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1503">Az.Resources</span></span>
* <span data-ttu-id="6621b-1504">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6621b-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6621b-1505">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="6621b-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6621b-1506">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6621b-1507">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="6621b-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6621b-1508">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6621b-1509">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="6621b-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1510">Az.Sql</span></span>
* <span data-ttu-id="6621b-1511">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="6621b-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6621b-1512">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="6621b-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1513">Az.Storage</span></span>
* <span data-ttu-id="6621b-1514">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="6621b-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6621b-1515">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6621b-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="6621b-1517">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="6621b-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-1518">Az.Automation</span></span>
* <span data-ttu-id="6621b-1519">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6621b-1520">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6621b-1521">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6621b-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="6621b-1523">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="6621b-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1524">Az.Compute</span></span>
* <span data-ttu-id="6621b-1525">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="6621b-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6621b-1526">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="6621b-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6621b-1527">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6621b-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6621b-1528">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6621b-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-1530">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="6621b-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6621b-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6621b-1531">Az.EventHub</span></span>
* <span data-ttu-id="6621b-1532">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="6621b-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6621b-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-1533">Az.KeyVault</span></span>
* <span data-ttu-id="6621b-1534">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="6621b-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6621b-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6621b-1535">Az.LogicApp</span></span>
* <span data-ttu-id="6621b-1536">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="6621b-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6621b-1537">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6621b-1538">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="6621b-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6621b-1539">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6621b-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6621b-1540">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6621b-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6621b-1541">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6621b-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6621b-1542">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="6621b-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6621b-1543">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="6621b-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6621b-1544">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6621b-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6621b-1545">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6621b-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6621b-1546">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6621b-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6621b-1547">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6621b-1548">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6621b-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-1549">Az.Monitor</span></span>
* <span data-ttu-id="6621b-1550">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="6621b-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1551">Az.Network</span></span>
* <span data-ttu-id="6621b-1552">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="6621b-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6621b-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="6621b-1554">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="6621b-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6621b-1555">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6621b-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6621b-1556">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="6621b-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6621b-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1557">Az.Resources</span></span>
* <span data-ttu-id="6621b-1558">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="6621b-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6621b-1559">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="6621b-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6621b-1560">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="6621b-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6621b-1561">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="6621b-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1562">Az.Sql</span></span>
* <span data-ttu-id="6621b-1563">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="6621b-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6621b-1564">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="6621b-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1565">Az.Websites</span></span>
* <span data-ttu-id="6621b-1566">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="6621b-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6621b-1567">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1568">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1569">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6621b-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6621b-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="6621b-1571">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="6621b-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1572">Az.Compute</span></span>
* <span data-ttu-id="6621b-1573">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="6621b-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6621b-1574">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="6621b-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6621b-1575">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="6621b-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="6621b-1577">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="6621b-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1578">Az.Resources</span></span>
* <span data-ttu-id="6621b-1579">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6621b-1580">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="6621b-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6621b-1581">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="6621b-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6621b-1582">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="6621b-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1583">Az.Sql</span></span>
* <span data-ttu-id="6621b-1584">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6621b-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6621b-1585">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6621b-1586">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="6621b-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6621b-1587">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1588">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1589">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6621b-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6621b-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="6621b-1591">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6621b-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="6621b-1593">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6621b-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6621b-1594">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1595">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1596">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6621b-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6621b-1597">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6621b-1598">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="6621b-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6621b-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6621b-1599">Az.Aks</span></span>
* <span data-ttu-id="6621b-1600">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6621b-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-1601">Az.Automation</span></span>
* <span data-ttu-id="6621b-1602">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="6621b-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6621b-1603">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6621b-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6621b-1604">Az.Cdn</span></span>
* <span data-ttu-id="6621b-1605">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1606">Az.Compute</span></span>
* <span data-ttu-id="6621b-1607">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="6621b-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6621b-1608">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6621b-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6621b-1609">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6621b-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6621b-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6621b-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6621b-1611">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6621b-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6621b-1612">Az.DataFactory</span></span>
* <span data-ttu-id="6621b-1613">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-1615">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="6621b-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6621b-1616">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="6621b-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6621b-1617">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6621b-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6621b-1618">Az.IotHub</span></span>
* <span data-ttu-id="6621b-1619">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6621b-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6621b-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-1620">Az.KeyVault</span></span>
* <span data-ttu-id="6621b-1621">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1622">Az.Network</span></span>
* <span data-ttu-id="6621b-1623">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1624">Az.Resources</span></span>
* <span data-ttu-id="6621b-1625">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="6621b-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6621b-1626">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6621b-1627">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6621b-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6621b-1628">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="6621b-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6621b-1629">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="6621b-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6621b-1630">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6621b-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6621b-1631">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="6621b-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6621b-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-1633">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="6621b-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6621b-1634">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6621b-1634">Fix some error messages.</span></span>
* <span data-ttu-id="6621b-1635">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="6621b-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6621b-1636">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="6621b-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6621b-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6621b-1637">Az.SignalR</span></span>
* <span data-ttu-id="6621b-1638">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1639">Az.Sql</span></span>
* <span data-ttu-id="6621b-1640">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6621b-1641">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6621b-1642">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="6621b-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6621b-1643">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="6621b-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1644">Az.Storage</span></span>
* <span data-ttu-id="6621b-1645">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6621b-1646">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="6621b-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6621b-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6621b-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6621b-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6621b-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6621b-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6621b-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="6621b-1650">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1651">Az.Websites</span></span>
* <span data-ttu-id="6621b-1652">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6621b-1653">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="6621b-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6621b-1654">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="6621b-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6621b-1655">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6621b-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1656">Az.Accounts</span></span>
* <span data-ttu-id="6621b-1657">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="6621b-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1658">Az.Compute</span></span>
* <span data-ttu-id="6621b-1659">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="6621b-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6621b-1660">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="6621b-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6621b-1661">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6621b-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-1663">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="6621b-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6621b-1664">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6621b-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6621b-1665">Az.EventGrid</span></span>
* <span data-ttu-id="6621b-1666">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6621b-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6621b-1667">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6621b-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6621b-1668">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6621b-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6621b-1669">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="6621b-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6621b-1670">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="6621b-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6621b-1671">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6621b-1672">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6621b-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6621b-1673">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="6621b-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6621b-1674">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="6621b-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6621b-1675">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="6621b-1676">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6621b-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6621b-1677">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="6621b-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6621b-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6621b-1678">Az.IotHub</span></span>
* <span data-ttu-id="6621b-1679">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="6621b-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6621b-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6621b-1680">Az.LogicApp</span></span>
* <span data-ttu-id="6621b-1681">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="6621b-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1682">Az.Resources</span></span>
* <span data-ttu-id="6621b-1683">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="6621b-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6621b-1684">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="6621b-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6621b-1685">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6621b-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6621b-1686">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="6621b-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6621b-1687">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="6621b-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6621b-1688">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="6621b-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6621b-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6621b-1689">Az.SignalR</span></span>
* <span data-ttu-id="6621b-1690">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6621b-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1691">Az.Sql</span></span>
* <span data-ttu-id="6621b-1692">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="6621b-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6621b-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1693">Az.Storage</span></span>
* <span data-ttu-id="6621b-1694">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="6621b-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6621b-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6621b-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="6621b-1696">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6621b-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6621b-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6621b-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1698">Az.Websites</span></span>
* <span data-ttu-id="6621b-1699">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="6621b-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6621b-1700">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6621b-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6621b-1701">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6621b-1702">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6621b-1702">General</span></span>

- <span data-ttu-id="6621b-1703">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="6621b-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="6621b-1704">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="6621b-1704">Online help for each module</span></span>
- <span data-ttu-id="6621b-1705">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="6621b-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6621b-1706">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6621b-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6621b-1707">Az.Accounts</span></span>
- <span data-ttu-id="6621b-1708">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="6621b-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="6621b-1709">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="6621b-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6621b-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="6621b-1711">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="6621b-1711">Fixes for #7002</span></span>
- <span data-ttu-id="6621b-1712">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6621b-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6621b-1713">Az.Batch</span></span>
- <span data-ttu-id="6621b-1714">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6621b-1715">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6621b-1716">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6621b-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6621b-1717">Az.Billing</span></span>
- <span data-ttu-id="6621b-1718">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="6621b-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6621b-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="6621b-1720">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="6621b-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6621b-1721">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6621b-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6621b-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6621b-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="6621b-1723">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="6621b-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6621b-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6621b-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6621b-1725">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="6621b-1727">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6621b-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6621b-1728">Az.Monitor</span></span>
- <span data-ttu-id="6621b-1729">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6621b-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6621b-1730">Az.KeyVault</span></span>
- <span data-ttu-id="6621b-1731">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="6621b-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6621b-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6621b-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="6621b-1733">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6621b-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6621b-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6621b-1734">Az.Media</span></span>
- <span data-ttu-id="6621b-1735">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6621b-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6621b-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1736">Az.Network</span></span>
<span data-ttu-id="6621b-1737">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="6621b-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6621b-1738">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="6621b-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6621b-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6621b-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6621b-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6621b-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6621b-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6621b-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6621b-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6621b-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6621b-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6621b-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6621b-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6621b-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6621b-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6621b-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6621b-1747">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6621b-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6621b-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6621b-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6621b-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6621b-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6621b-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6621b-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6621b-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6621b-1753">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6621b-1754">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6621b-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6621b-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6621b-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6621b-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6621b-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6621b-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6621b-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6621b-1758">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6621b-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6621b-1759">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6621b-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="6621b-1761">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6621b-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6621b-1762">Az.Profile</span></span>
- <span data-ttu-id="6621b-1763">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6621b-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="6621b-1765">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6621b-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1766">Az.Resources</span></span>
- <span data-ttu-id="6621b-1767">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6621b-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="6621b-1769">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="6621b-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6621b-1770">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6621b-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6621b-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="6621b-1772">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6621b-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6621b-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1773">Az.Sql</span></span>
- <span data-ttu-id="6621b-1774">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="6621b-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6621b-1775">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6621b-1776">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6621b-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1777">Az.Storage</span></span>
- <span data-ttu-id="6621b-1778">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6621b-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1779">Az.Websites</span></span>
- <span data-ttu-id="6621b-1780">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6621b-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6621b-1781">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6621b-1782">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6621b-1782">General</span></span>

* <span data-ttu-id="6621b-1783">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="6621b-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6621b-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1784">Az.Compute</span></span>

* <span data-ttu-id="6621b-1785">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="6621b-1787">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="6621b-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6621b-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6621b-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="6621b-1789">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="6621b-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="6621b-1790">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6621b-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6621b-1791">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="6621b-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6621b-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="6621b-1793">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6621b-1794">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="6621b-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6621b-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1795">Az.Resources</span></span>

* <span data-ttu-id="6621b-1796">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="6621b-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6621b-1797">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6621b-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1798">Az.Sql</span></span>

* <span data-ttu-id="6621b-1799">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="6621b-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6621b-1800">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="6621b-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6621b-1801">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="6621b-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6621b-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6621b-1802">Az.Storage</span></span>

* <span data-ttu-id="6621b-1803">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6621b-1804">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="6621b-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6621b-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6621b-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6621b-1806">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="6621b-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="6621b-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6621b-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6621b-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6621b-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6621b-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1809">Az.Websites</span></span>

* <span data-ttu-id="6621b-1810">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6621b-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6621b-1811">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="6621b-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6621b-1812">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6621b-1813">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6621b-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6621b-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="6621b-1815">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6621b-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6621b-1816">Az.Automation</span></span>
* <span data-ttu-id="6621b-1817">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="6621b-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6621b-1818">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="6621b-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6621b-1819">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="6621b-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6621b-1820">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="6621b-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6621b-1821">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="6621b-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6621b-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1822">Az.Compute</span></span>
* <span data-ttu-id="6621b-1823">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="6621b-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6621b-1824">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6621b-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6621b-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="6621b-1826">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6621b-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6621b-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6621b-1828">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6621b-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6621b-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1829">Az.Network</span></span>
* <span data-ttu-id="6621b-1830">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="6621b-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6621b-1831">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6621b-1832">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6621b-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6621b-1833">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6621b-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6621b-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6621b-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6621b-1835">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6621b-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6621b-1836">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="6621b-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6621b-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6621b-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6621b-1838">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="6621b-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6621b-1839">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6621b-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6621b-1840">Az.Relay</span></span>
* <span data-ttu-id="6621b-1841">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="6621b-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6621b-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1842">Az.Resources</span></span>
* <span data-ttu-id="6621b-1843">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="6621b-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6621b-1844">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="6621b-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6621b-1845">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="6621b-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6621b-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-1847">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="6621b-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6621b-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1848">Az.Sql</span></span>
* <span data-ttu-id="6621b-1849">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6621b-1850">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6621b-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6621b-1851">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6621b-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6621b-1852">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6621b-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6621b-1853">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6621b-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6621b-1854">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6621b-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6621b-1855">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6621b-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6621b-1856">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6621b-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6621b-1857">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6621b-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6621b-1858">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="6621b-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6621b-1859">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="6621b-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6621b-1860">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6621b-1861">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6621b-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6621b-1862">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6621b-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6621b-1863">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6621b-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6621b-1864">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6621b-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6621b-1865">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="6621b-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6621b-1866">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6621b-1867">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6621b-1867">General</span></span>
* <span data-ttu-id="6621b-1868">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="6621b-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6621b-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6621b-1869">Az.Profile</span></span>
* <span data-ttu-id="6621b-1870">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6621b-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6621b-1871">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="6621b-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6621b-1872">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6621b-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6621b-1873">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="6621b-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6621b-1874">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6621b-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6621b-1875">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="6621b-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6621b-1876">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="6621b-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6621b-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="6621b-1878">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6621b-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1879">Az.Compute</span></span>
* <span data-ttu-id="6621b-1880">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6621b-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6621b-1881">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6621b-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6621b-1882">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6621b-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-1884">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="6621b-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6621b-1885">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="6621b-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6621b-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6621b-1886">Az.Insights</span></span>
* <span data-ttu-id="6621b-1887">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="6621b-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6621b-1888">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6621b-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6621b-1889">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="6621b-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6621b-1890">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="6621b-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1891">Az.Network</span></span>
* <span data-ttu-id="6621b-1892">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="6621b-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6621b-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6621b-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6621b-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6621b-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6621b-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6621b-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6621b-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6621b-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6621b-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6621b-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6621b-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6621b-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6621b-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6621b-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="6621b-1900">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="6621b-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1901">Az.Resources</span></span>
* <span data-ttu-id="6621b-1902">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="6621b-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6621b-1903">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6621b-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6621b-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6621b-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="6621b-1905">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="6621b-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6621b-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6621b-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="6621b-1907">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="6621b-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6621b-1908">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6621b-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6621b-1909">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6621b-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6621b-1910">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6621b-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6621b-1911">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6621b-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6621b-1912">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6621b-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6621b-1913">Az.Profile</span></span>
* <span data-ttu-id="6621b-1914">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="6621b-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6621b-1915">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6621b-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1916">Az.Compute</span></span>
* <span data-ttu-id="6621b-1917">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="6621b-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6621b-1918">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="6621b-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6621b-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6621b-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="6621b-1920">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="6621b-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6621b-1921">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6621b-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6621b-1922">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6621b-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6621b-1923">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6621b-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6621b-1924">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6621b-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1925">Az.Network</span></span>
* <span data-ttu-id="6621b-1926">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="6621b-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6621b-1927">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="6621b-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1928">Az.Resources</span></span>
* <span data-ttu-id="6621b-1929">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="6621b-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6621b-1930">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="6621b-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6621b-1931">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6621b-1932">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="6621b-1932">Azure.Storage</span></span>
* <span data-ttu-id="6621b-1933">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="6621b-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6621b-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6621b-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6621b-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6621b-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6621b-1936">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="6621b-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6621b-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6621b-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6621b-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6621b-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="6621b-1939">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6621b-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6621b-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6621b-1940">Az.Compute</span></span>
* <span data-ttu-id="6621b-1941">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="6621b-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6621b-1942">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6621b-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6621b-1943">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6621b-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6621b-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6621b-1945">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="6621b-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6621b-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6621b-1946">Az.Network</span></span>
* <span data-ttu-id="6621b-1947">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="6621b-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6621b-1948">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6621b-1948">new cmdlets added</span></span>
    - <span data-ttu-id="6621b-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6621b-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6621b-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6621b-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6621b-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6621b-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6621b-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6621b-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6621b-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6621b-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6621b-1955">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="6621b-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6621b-1956">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6621b-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6621b-1957">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6621b-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6621b-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6621b-1958">Az.RedisCache</span></span>
* <span data-ttu-id="6621b-1959">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="6621b-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6621b-1960">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="6621b-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6621b-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6621b-1961">Az.Resources</span></span>
* <span data-ttu-id="6621b-1962">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6621b-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6621b-1963">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="6621b-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6621b-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6621b-1964">Az.Sql</span></span>
* <span data-ttu-id="6621b-1965">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="6621b-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6621b-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6621b-1966">Az.Websites</span></span>
* <span data-ttu-id="6621b-1967">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="6621b-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6621b-1968">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="6621b-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6621b-1969">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6621b-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6621b-1970">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="6621b-1970">Initial Release</span></span>
