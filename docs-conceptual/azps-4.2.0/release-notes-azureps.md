---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 8d53923f76506469cdc2c111faf7c4568b54f7de
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "84294799"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="d4332-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4332-103">Azure PowerShell release notes</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="d4332-104">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-104">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-105">Az.Accounts</span></span>
* <span data-ttu-id="d4332-106">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="d4332-106">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4332-107">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4332-107">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4332-108">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-108">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-109">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-110">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="d4332-110">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="d4332-111">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d4332-111">Az.Billing</span></span>
* <span data-ttu-id="d4332-112">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="d4332-112">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-114">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="d4332-114">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-115">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-116">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="d4332-116">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="d4332-117">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="d4332-117">Az.DataShare</span></span>
* <span data-ttu-id="d4332-118">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="d4332-118">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="d4332-119">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="d4332-119">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="d4332-120">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="d4332-120">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-121">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-121">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-122">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-122">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="d4332-123">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-123">Added optional parameters to</span></span> 
    - <span data-ttu-id="d4332-124">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d4332-124">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="d4332-125">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d4332-125">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-126">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-126">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-127">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="d4332-127">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d4332-128">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d4332-128">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d4332-129">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d4332-129">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d4332-130">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d4332-130">Az.PrivateDns</span></span>
* <span data-ttu-id="d4332-131">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-131">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-132">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-132">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-133">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="d4332-133">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="d4332-134">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="d4332-134">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-135">Az.Resources</span></span>
* <span data-ttu-id="d4332-136">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="d4332-136">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="d4332-137">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="d4332-137">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="d4332-138">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-138">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="d4332-139">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="d4332-139">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="d4332-140">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="d4332-140">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-141">Az.Sql</span></span>
* <span data-ttu-id="d4332-142">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="d4332-142">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="d4332-143">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="d4332-143">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="d4332-144">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-144">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-145">Az.Storage</span></span>
* <span data-ttu-id="d4332-146">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-146">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="d4332-147">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-147">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="d4332-148">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-148">Highlights since the last release</span></span>
* <span data-ttu-id="d4332-149">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="d4332-149">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="d4332-150">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="d4332-150">General availability of Az.Functions</span></span> 
* <span data-ttu-id="d4332-151">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="d4332-151">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-152">Az.Accounts</span></span>
* <span data-ttu-id="d4332-153">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="d4332-153">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="d4332-154">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="d4332-154">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="d4332-155">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d4332-155">Az.Aks</span></span>
* <span data-ttu-id="d4332-156">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="d4332-156">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="d4332-157">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d4332-157">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="d4332-158">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="d4332-158">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-159">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-159">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-160">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="d4332-160">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="d4332-161">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="d4332-161">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="d4332-162">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d4332-162">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d4332-163">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d4332-163">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d4332-164">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d4332-164">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d4332-165">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d4332-165">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="d4332-166">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d4332-166">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d4332-167">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d4332-167">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d4332-168">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="d4332-168">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d4332-169">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d4332-169">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d4332-170">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="d4332-170">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="d4332-171">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="d4332-171">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="d4332-172">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="d4332-172">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="d4332-173">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="d4332-173">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="d4332-174">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="d4332-174">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="d4332-175">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="d4332-175">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d4332-176">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-176">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d4332-177">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="d4332-177">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="d4332-178">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="d4332-178">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="d4332-179">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-179">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4332-180">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4332-180">Az.Batch</span></span>
* <span data-ttu-id="d4332-181">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-181">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="d4332-182">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="d4332-182">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="d4332-183">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="d4332-183">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="d4332-184">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="d4332-184">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="d4332-185">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="d4332-185">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="d4332-186">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="d4332-186">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="d4332-187">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-187">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="d4332-188">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-188">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="d4332-189">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="d4332-189">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-190">Az.Compute</span></span>
* <span data-ttu-id="d4332-191">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="d4332-191">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="d4332-192">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="d4332-192">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="d4332-193">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d4332-193">Breaking changes</span></span>
    - <span data-ttu-id="d4332-194">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="d4332-194">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="d4332-195">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-195">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="d4332-196">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4332-196">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="d4332-197">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-197">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="d4332-198">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-198">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="d4332-199">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="d4332-199">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="d4332-200">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-200">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-201">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-202">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d4332-202">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4332-203">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-203">Az.FrontDoor</span></span>
* <span data-ttu-id="d4332-204">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="d4332-204">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="d4332-205">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="d4332-205">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="d4332-206">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="d4332-206">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="d4332-207">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="d4332-207">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d4332-208">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d4332-208">Az.Functions</span></span>
* <span data-ttu-id="d4332-209">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="d4332-209">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4332-210">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-210">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-211">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="d4332-211">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d4332-212">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d4332-212">Az.HealthcareApis</span></span>
* <span data-ttu-id="d4332-213">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4332-213">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-214">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-214">Az.IotHub</span></span>
* <span data-ttu-id="d4332-215">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="d4332-215">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="d4332-216">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="d4332-216">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="d4332-217">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="d4332-217">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="d4332-218">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d4332-218">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="d4332-219">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="d4332-219">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="d4332-220">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-220">New cmdlets are:</span></span>
    - <span data-ttu-id="d4332-221">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="d4332-221">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d4332-222">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="d4332-222">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d4332-223">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="d4332-223">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d4332-224">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-224">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="d4332-225">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-225">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="d4332-226">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="d4332-226">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-227">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-227">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-228">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="d4332-228">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="d4332-229">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4332-229">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="d4332-230">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="d4332-230">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="d4332-231">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="d4332-231">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="d4332-232">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="d4332-232">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="d4332-233">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="d4332-233">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="d4332-234">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="d4332-234">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-235">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-235">Az.Monitor</span></span>
* <span data-ttu-id="d4332-236">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="d4332-236">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="d4332-237">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="d4332-237">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="d4332-238">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="d4332-238">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="d4332-239">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="d4332-239">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="d4332-240">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="d4332-240">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="d4332-241">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="d4332-241">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="d4332-242">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="d4332-242">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-243">Az.Network</span></span>
* <span data-ttu-id="d4332-244">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="d4332-244">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="d4332-245">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="d4332-245">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="d4332-246">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="d4332-246">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="d4332-247">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-247">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="d4332-248">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="d4332-248">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="d4332-249">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-249">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-250">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="d4332-250">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d4332-251">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="d4332-251">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d4332-252">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="d4332-252">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d4332-253">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="d4332-253">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="d4332-254">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="d4332-254">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="d4332-255">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-255">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="d4332-256">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="d4332-256">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="d4332-257">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="d4332-257">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="d4332-258">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d4332-258">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="d4332-259">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d4332-259">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="d4332-260">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="d4332-260">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="d4332-261">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="d4332-261">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d4332-262">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="d4332-262">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d4332-263">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="d4332-263">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d4332-264">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-264">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="d4332-265">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="d4332-265">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="d4332-266">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="d4332-266">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="d4332-267">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d4332-267">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4332-268">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="d4332-268">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-269">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-269">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-270">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="d4332-270">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="d4332-271">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-271">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="d4332-272">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="d4332-272">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="d4332-273">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="d4332-273">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="d4332-274">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="d4332-274">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="d4332-275">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="d4332-275">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="d4332-276">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-276">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="d4332-277">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="d4332-277">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-279">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d4332-279">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="d4332-280">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="d4332-280">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="d4332-281">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-281">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="d4332-282">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d4332-282">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="d4332-283">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4332-283">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-284">Az.Resources</span></span>
* <span data-ttu-id="d4332-285">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="d4332-285">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="d4332-286">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="d4332-286">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="d4332-287">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="d4332-287">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="d4332-288">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="d4332-288">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="d4332-289">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="d4332-289">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="d4332-290">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="d4332-290">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="d4332-291">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="d4332-291">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="d4332-292">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="d4332-292">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="d4332-293">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="d4332-293">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="d4332-294">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="d4332-294">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="d4332-295">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="d4332-295">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="d4332-296">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="d4332-296">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="d4332-297">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="d4332-297">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="d4332-298">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="d4332-298">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="d4332-299">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="d4332-299">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="d4332-300">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d4332-300">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="d4332-301">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="d4332-301">'New-AzDeployment'</span></span>
    - <span data-ttu-id="d4332-302">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="d4332-302">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="d4332-303">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="d4332-303">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d4332-304">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-304">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-306">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="d4332-306">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-307">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-307">Az.Sql</span></span>
* <span data-ttu-id="d4332-308">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d4332-308">Enhance performance of:</span></span>
    - <span data-ttu-id="d4332-309">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d4332-309">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d4332-310">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d4332-310">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d4332-311">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d4332-311">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d4332-312">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="d4332-312">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d4332-313">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="d4332-313">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d4332-314">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="d4332-314">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d4332-315">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="d4332-315">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d4332-316">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="d4332-316">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="d4332-317">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-317">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="d4332-318">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="d4332-318">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-319">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-319">Az.Storage</span></span>
* <span data-ttu-id="d4332-320">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="d4332-320">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="d4332-321">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="d4332-321">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="d4332-322">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-322">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d4332-323">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="d4332-323">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="d4332-324">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="d4332-324">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="d4332-325">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="d4332-325">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="d4332-326">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="d4332-326">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="d4332-327">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-327">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="d4332-328">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="d4332-328">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="d4332-329">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d4332-329">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="d4332-330">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="d4332-330">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="d4332-331">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="d4332-331">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="d4332-332">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="d4332-332">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="d4332-333">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-333">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="d4332-334">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-334">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="d4332-335">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-335">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d4332-336">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-336">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="d4332-337">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="d4332-337">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="d4332-338">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="d4332-338">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d4332-339">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-339">Supported failover Storage account</span></span>
    - <span data-ttu-id="d4332-340">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="d4332-340">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="d4332-341">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="d4332-341">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="d4332-342">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="d4332-342">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="d4332-343">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="d4332-343">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="d4332-344">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-344">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d4332-345">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="d4332-345">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="d4332-346">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="d4332-346">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="d4332-347">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="d4332-347">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="d4332-348">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="d4332-348">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="d4332-349">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="d4332-349">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="d4332-350">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-350">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d4332-351">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="d4332-351">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="d4332-352">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="d4332-352">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="d4332-353">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-353">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d4332-354">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d4332-354">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="d4332-355">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d4332-355">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="d4332-356">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="d4332-356">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="d4332-357">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-357">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="d4332-358">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="d4332-358">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d4332-359">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d4332-359">Az.TrafficManager</span></span>
* <span data-ttu-id="d4332-360">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d4332-360">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-361">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-361">Az.Websites</span></span>
* <span data-ttu-id="d4332-362">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-362">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="d4332-363">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-363">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="d4332-364">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-364">Highlights since the last release</span></span>
* <span data-ttu-id="d4332-365">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="d4332-365">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-366">Az.Accounts</span></span>
* <span data-ttu-id="d4332-367">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="d4332-367">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-368">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-368">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-369">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="d4332-369">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="d4332-370">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="d4332-370">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4332-371">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-371">Az.Cdn</span></span>
* <span data-ttu-id="d4332-372">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="d4332-372">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-373">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-373">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-374">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="d4332-374">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-375">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-375">Az.Compute</span></span>
* <span data-ttu-id="d4332-376">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="d4332-376">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="d4332-377">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="d4332-377">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-378">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-378">Az.IotHub</span></span>
* <span data-ttu-id="d4332-379">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-379">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="d4332-380">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d4332-380">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="d4332-381">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d4332-381">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="d4332-382">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-382">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="d4332-383">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-383">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="d4332-384">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="d4332-384">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="d4332-385">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="d4332-385">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="d4332-386">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="d4332-386">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="d4332-387">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-387">New cmdlets are:</span></span>
    - <span data-ttu-id="d4332-388">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4332-388">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d4332-389">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4332-389">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d4332-390">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4332-390">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d4332-391">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4332-391">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="d4332-392">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-392">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-393">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-393">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-394">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d4332-394">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="d4332-395">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="d4332-395">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="d4332-396">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="d4332-396">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="d4332-397">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d4332-397">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="d4332-398">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="d4332-398">Az.Maintenance</span></span>
* <span data-ttu-id="d4332-399">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="d4332-399">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-400">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-400">Az.Monitor</span></span>
* <span data-ttu-id="d4332-401">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="d4332-401">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="d4332-402">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4332-402">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d4332-403">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4332-403">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d4332-404">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4332-404">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d4332-405">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4332-405">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d4332-406">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d4332-406">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="d4332-407">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d4332-407">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="d4332-408">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d4332-408">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-409">Az.Network</span></span>
* <span data-ttu-id="d4332-410">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="d4332-410">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="d4332-411">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-411">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="d4332-412">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-412">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="d4332-413">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-413">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="d4332-414">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-414">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="d4332-415">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="d4332-415">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="d4332-416">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-416">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="d4332-417">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d4332-417">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="d4332-418">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="d4332-418">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="d4332-419">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-419">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="d4332-420">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="d4332-420">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="d4332-421">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-421">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="d4332-422">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="d4332-422">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="d4332-423">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="d4332-423">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="d4332-424">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="d4332-424">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="d4332-425">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-425">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-426">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-426">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-427">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="d4332-427">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="d4332-428">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d4332-428">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-429">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-430">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="d4332-430">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-431">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-431">Az.Sql</span></span>
* <span data-ttu-id="d4332-432">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="d4332-432">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="d4332-433">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-433">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-434">Az.Storage</span></span>
* <span data-ttu-id="d4332-435">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="d4332-435">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="d4332-436">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-436">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="d4332-437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-437">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="d4332-438">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-438">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d4332-439">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="d4332-439">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="d4332-440">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d4332-440">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d4332-441">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d4332-441">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d4332-442">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="d4332-442">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="d4332-443">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d4332-443">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d4332-444">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="d4332-444">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="d4332-445">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d4332-445">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d4332-446">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="d4332-446">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="d4332-447">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d4332-447">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="d4332-448">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-448">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="d4332-449">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-449">General</span></span>
* <span data-ttu-id="d4332-450">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="d4332-450">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="d4332-451">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="d4332-451">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="d4332-452">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="d4332-452">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="d4332-453">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="d4332-453">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="d4332-454">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d4332-454">Az.Billing</span></span>
  - <span data-ttu-id="d4332-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-455">Az.Compute</span></span>
  - <span data-ttu-id="d4332-456">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d4332-456">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="d4332-457">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-457">Az.EventHub</span></span>
  - <span data-ttu-id="d4332-458">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-458">Az.IotHub</span></span>
  - <span data-ttu-id="d4332-459">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-459">Az.KeyVault</span></span>
  - <span data-ttu-id="d4332-460">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-460">Az.Monitor</span></span>
  - <span data-ttu-id="d4332-461">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-461">Az.Network</span></span>
  - <span data-ttu-id="d4332-462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-462">Az.Resources</span></span>
  - <span data-ttu-id="d4332-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-463">Az.Storage</span></span>
  - <span data-ttu-id="d4332-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-464">Az.Websites</span></span>
* <span data-ttu-id="d4332-465">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="d4332-465">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="d4332-466">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="d4332-466">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="d4332-467">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="d4332-467">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="d4332-468">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-468">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-469">Az.Accounts</span></span>
* <span data-ttu-id="d4332-470">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="d4332-470">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-471">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-471">Az.Compute</span></span>
* <span data-ttu-id="d4332-472">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="d4332-472">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="d4332-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="d4332-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="d4332-474">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d4332-474">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="d4332-475">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="d4332-475">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="d4332-476">[11354]</span><span class="sxs-lookup"><span data-stu-id="d4332-476">[#11354]</span></span>
* <span data-ttu-id="d4332-477">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="d4332-477">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="d4332-478">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4332-478">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d4332-479">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4332-479">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d4332-480">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4332-480">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d4332-481">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d4332-481">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="d4332-482">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="d4332-482">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="d4332-483">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d4332-483">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="d4332-484">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="d4332-484">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="d4332-485">[11257]</span><span class="sxs-lookup"><span data-stu-id="d4332-485">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-486">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-487">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-487">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="d4332-488">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="d4332-488">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-489">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-490">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="d4332-490">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="d4332-491">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="d4332-491">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4332-492">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-492">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-493">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="d4332-493">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-494">Az.IotHub</span></span>
* <span data-ttu-id="d4332-495">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="d4332-495">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="d4332-496">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d4332-496">New Cmdlets are:</span></span>
    - <span data-ttu-id="d4332-497">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d4332-497">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="d4332-498">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d4332-498">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-499">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-500">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d4332-500">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-501">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-501">Az.Monitor</span></span>
* <span data-ttu-id="d4332-502">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="d4332-502">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-503">Az.Network</span></span>
* <span data-ttu-id="d4332-504">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="d4332-504">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="d4332-505">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-505">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d4332-506">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-506">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d4332-507">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d4332-507">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="d4332-508">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d4332-508">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="d4332-509">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="d4332-509">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-510">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-510">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-511">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d4332-511">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-512">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-513">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-513">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="d4332-514">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4332-514">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="d4332-515">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="d4332-515">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="d4332-516">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4332-516">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="d4332-517">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d4332-517">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="d4332-518">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-518">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-519">Az.Resources</span></span>
* <span data-ttu-id="d4332-520">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="d4332-520">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="d4332-521">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="d4332-521">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="d4332-522">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="d4332-522">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="d4332-523">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="d4332-523">Added example.</span></span>
* <span data-ttu-id="d4332-524">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="d4332-524">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="d4332-525">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="d4332-525">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-526">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-526">Az.Sql</span></span>
* <span data-ttu-id="d4332-527">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="d4332-527">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="d4332-528">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="d4332-528">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d4332-529">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-529">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="d4332-530">Az.Support</span><span class="sxs-lookup"><span data-stu-id="d4332-530">Az.Support</span></span>
* <span data-ttu-id="d4332-531">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="d4332-531">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-532">Az.Websites</span></span>
* <span data-ttu-id="d4332-533">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-533">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="d4332-534">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d4332-534">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d4332-535">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d4332-535">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d4332-536">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d4332-536">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d4332-537">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d4332-537">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="d4332-538">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-538">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-539">Az.Accounts</span></span>
* <span data-ttu-id="d4332-540">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="d4332-540">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="d4332-541">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="d4332-541">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="d4332-542">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="d4332-542">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-543">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-543">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-544">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="d4332-544">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="d4332-545">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="d4332-545">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="d4332-546">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="d4332-546">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="d4332-547">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="d4332-547">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-548">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-548">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-549">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="d4332-549">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-550">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-550">Az.IotHub</span></span>
* <span data-ttu-id="d4332-551">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-551">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d4332-552">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d4332-552">New Cmdlets are:</span></span>
    - <span data-ttu-id="d4332-553">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-553">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d4332-554">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-554">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d4332-555">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-555">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d4332-556">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-556">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="d4332-557">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-557">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="d4332-558">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d4332-558">New Cmdlets are:</span></span>
    - <span data-ttu-id="d4332-559">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d4332-559">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="d4332-560">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d4332-560">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="d4332-561">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d4332-561">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="d4332-562">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d4332-562">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="d4332-563">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-563">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d4332-564">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-564">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d4332-565">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-565">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="d4332-566">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d4332-566">New Cmdlets are:</span></span>
    - <span data-ttu-id="d4332-567">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="d4332-567">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="d4332-568">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="d4332-568">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="d4332-569">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="d4332-569">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-570">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-570">Az.Monitor</span></span>
* <span data-ttu-id="d4332-571">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="d4332-571">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-572">Az.Network</span></span>
* <span data-ttu-id="d4332-573">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="d4332-573">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="d4332-574">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="d4332-574">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="d4332-575">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="d4332-575">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="d4332-576">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d4332-576">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-577">Az.Resources</span></span>
* <span data-ttu-id="d4332-578">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="d4332-578">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="d4332-579">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="d4332-579">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="d4332-580">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="d4332-580">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="d4332-581">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="d4332-581">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="d4332-582">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="d4332-582">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="d4332-583">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="d4332-583">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="d4332-584">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d4332-584">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="d4332-585">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d4332-585">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="d4332-586">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4332-586">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d4332-587">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4332-587">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d4332-588">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4332-588">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="d4332-589">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="d4332-589">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="d4332-590">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4332-590">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="d4332-591">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-591">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-592">Az.Sql</span></span>
* <span data-ttu-id="d4332-593">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d4332-593">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="d4332-594">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-594">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="d4332-595">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-595">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="d4332-596">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="d4332-596">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="d4332-597">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="d4332-597">Remove an LTR backup</span></span>
    - <span data-ttu-id="d4332-598">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-598">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="d4332-599">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d4332-599">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="d4332-600">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d4332-600">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="d4332-601">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d4332-601">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-602">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-602">Az.Storage</span></span>
* <span data-ttu-id="d4332-603">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-603">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="d4332-604">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-604">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="d4332-605">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="d4332-605">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="d4332-606">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d4332-606">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="d4332-607">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d4332-607">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-608">Az.Websites</span></span>
* <span data-ttu-id="d4332-609">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d4332-609">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="d4332-610">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="d4332-610">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="d4332-611">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="d4332-611">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="d4332-612">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4332-612">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="d4332-613">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="d4332-613">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="d4332-614">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-614">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4332-615">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-615">Highlights since the last major release</span></span>
* <span data-ttu-id="d4332-616">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="d4332-616">Updated client side telemetry.</span></span>
* <span data-ttu-id="d4332-617">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="d4332-617">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="d4332-618">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="d4332-618">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-619">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-619">Az.Accounts</span></span>
* <span data-ttu-id="d4332-620">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d4332-620">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-621">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-621">Az.Automation</span></span>
* <span data-ttu-id="d4332-622">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-622">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-623">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-623">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-624">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-624">Updated SDK to 7.0</span></span>
* <span data-ttu-id="d4332-625">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="d4332-625">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-626">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-626">Az.Compute</span></span>
* <span data-ttu-id="d4332-627">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="d4332-627">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4332-628">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-628">Az.FrontDoor</span></span>
* <span data-ttu-id="d4332-629">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="d4332-629">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-630">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-630">Az.IotHub</span></span>
* <span data-ttu-id="d4332-631">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="d4332-631">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d4332-632">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="d4332-632">New Cmdlets are:</span></span>
    - <span data-ttu-id="d4332-633">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-633">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d4332-634">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-634">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d4332-635">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-635">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d4332-636">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d4332-636">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-637">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-638">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-638">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-639">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-639">Az.Monitor</span></span>
* <span data-ttu-id="d4332-640">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="d4332-640">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="d4332-641">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="d4332-641">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="d4332-642">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="d4332-642">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-643">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-643">Az.Network</span></span>
* <span data-ttu-id="d4332-644">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d4332-644">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="d4332-645">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-645">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d4332-646">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-646">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d4332-647">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-647">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="d4332-648">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="d4332-648">No new cmdlets are added.</span></span> <span data-ttu-id="d4332-649">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="d4332-649">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-651">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d4332-651">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-652">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-652">Az.Resources</span></span>
* <span data-ttu-id="d4332-653">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="d4332-653">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="d4332-654">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-654">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="d4332-655">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-655">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="d4332-656">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="d4332-656">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="d4332-657">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-657">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="d4332-658">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="d4332-658">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="d4332-659">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="d4332-659">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="d4332-660">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-660">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-661">Az.Sql</span></span>
* <span data-ttu-id="d4332-662">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="d4332-662">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="d4332-663">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="d4332-663">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="d4332-664">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="d4332-664">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d4332-665">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d4332-665">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d4332-666">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="d4332-666">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4332-667">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4332-667">Az.StorageSync</span></span>
* <span data-ttu-id="d4332-668">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="d4332-668">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="d4332-669">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-669">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4332-670">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-670">Highlights since the last major release</span></span>
* <span data-ttu-id="d4332-671">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d4332-671">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="d4332-672">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="d4332-672">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-673">Az.Accounts</span></span>
* <span data-ttu-id="d4332-674">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="d4332-674">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="d4332-675">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="d4332-675">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-676">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-676">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-677">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="d4332-677">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="d4332-678">**New-AzApiManagementProduct**\* и **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="d4332-678">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="d4332-679">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="d4332-679">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="d4332-680">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="d4332-680">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-681">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-681">Az.Compute</span></span>
* <span data-ttu-id="d4332-682">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d4332-682">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="d4332-683">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d4332-683">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="d4332-684">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-684">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="d4332-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="d4332-686">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-686">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-687">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-688">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-688">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d4332-689">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d4332-689">Az.DeploymentManager</span></span>
* <span data-ttu-id="d4332-690">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="d4332-690">Adds LIST operations for resources</span></span>
* <span data-ttu-id="d4332-691">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="d4332-691">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4332-692">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-692">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-693">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d4332-693">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-694">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-694">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-695">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d4332-695">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-696">Az.Network</span></span>
* <span data-ttu-id="d4332-697">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="d4332-697">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="d4332-698">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="d4332-698">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="d4332-699">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d4332-699">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d4332-700">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="d4332-700">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="d4332-701">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="d4332-701">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="d4332-702">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d4332-702">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="d4332-703">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4332-703">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="d4332-704">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="d4332-704">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="d4332-705">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-705">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4332-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="d4332-707">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4332-707">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="d4332-708">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d4332-708">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="d4332-709">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="d4332-709">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-710">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-710">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-711">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="d4332-711">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="d4332-712">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d4332-712">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="d4332-713">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="d4332-713">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="d4332-714">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="d4332-714">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-715">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-715">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-716">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="d4332-716">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="d4332-717">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4332-717">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-718">Az.Resources</span></span>
* <span data-ttu-id="d4332-719">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="d4332-719">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="d4332-720">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="d4332-720">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-721">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-721">Az.Sql</span></span>
<span data-ttu-id="d4332-722">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="d4332-722">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-723">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-723">Az.Storage</span></span>
* <span data-ttu-id="d4332-724">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d4332-724">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="d4332-725">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-725">New-AzStorageAccount</span></span>
* <span data-ttu-id="d4332-726">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="d4332-726">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="d4332-727">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4332-727">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-728">Az.Websites</span></span>
* <span data-ttu-id="d4332-729">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="d4332-729">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="d4332-730">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d4332-730">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="d4332-731">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-731">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-732">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-732">Az.Accounts</span></span>
* <span data-ttu-id="d4332-733">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="d4332-733">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4332-734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-734">Az.Cdn</span></span>
* <span data-ttu-id="d4332-735">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d4332-735">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-736">Az.Compute</span></span>
* <span data-ttu-id="d4332-737">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="d4332-737">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d4332-738">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4332-738">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4332-739">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-739">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d4332-740">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d4332-740">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d4332-741">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d4332-741">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4332-742">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-742">Get the Edge Storage Container</span></span>
* <span data-ttu-id="d4332-743">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d4332-743">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4332-744">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-744">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="d4332-745">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d4332-745">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4332-746">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-746">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="d4332-747">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="d4332-747">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4332-748">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-748">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="d4332-749">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="d4332-749">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d4332-750">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-750">Get the Edge Storage Account</span></span>
* <span data-ttu-id="d4332-751">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="d4332-751">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d4332-752">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-752">Create new Edge Storage Account</span></span>
* <span data-ttu-id="d4332-753">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="d4332-753">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d4332-754">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-754">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="d4332-755">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="d4332-755">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="d4332-756">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="d4332-756">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="d4332-757">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="d4332-757">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="d4332-758">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="d4332-758">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-759">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-760">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="d4332-760">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="d4332-761">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-761">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="d4332-762">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="d4332-762">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="d4332-763">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="d4332-763">Az.DevTestLabs</span></span>
* <span data-ttu-id="d4332-764">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-764">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4332-765">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-765">Az.EventHub</span></span>
* <span data-ttu-id="d4332-766">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="d4332-766">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4332-767">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-767">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-768">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-768">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d4332-769">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4332-769">Az.MachineLearning</span></span>
* <span data-ttu-id="d4332-770">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-770">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="d4332-771">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d4332-771">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4332-772">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="d4332-772">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="d4332-773">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d4332-773">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4332-774">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d4332-774">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4332-775">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="d4332-775">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4332-776">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="d4332-776">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="d4332-777">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="d4332-777">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-778">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-778">Az.Network</span></span>
* <span data-ttu-id="d4332-779">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="d4332-779">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-780">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-780">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-781">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-781">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="d4332-782">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-782">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d4332-783">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-783">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d4332-784">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-784">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-785">Az.Resources</span></span>
* <span data-ttu-id="d4332-786">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="d4332-786">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-787">Az.Sql</span></span>
* <span data-ttu-id="d4332-788">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d4332-788">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="d4332-789">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="d4332-789">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d4332-790">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d4332-790">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d4332-791">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="d4332-791">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-792">Az.Storage</span></span>
* <span data-ttu-id="d4332-793">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="d4332-793">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="d4332-794">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-794">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="d4332-795">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="d4332-795">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="d4332-796">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="d4332-796">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="d4332-797">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-797">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="d4332-798">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-798">General</span></span>
* <span data-ttu-id="d4332-799">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="d4332-799">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-800">Az.Accounts</span></span>
* <span data-ttu-id="d4332-801">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="d4332-801">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="d4332-802">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="d4332-802">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4332-803">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4332-803">Az.Batch</span></span>
* <span data-ttu-id="d4332-804">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="d4332-804">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-805">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-806">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-806">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4332-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-807">Az.FrontDoor</span></span>
* <span data-ttu-id="d4332-808">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="d4332-808">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="d4332-809">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="d4332-809">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d4332-810">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d4332-810">Az.HealthcareApis</span></span>
* <span data-ttu-id="d4332-811">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="d4332-811">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-812">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-812">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-813">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="d4332-813">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="d4332-814">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="d4332-814">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="d4332-815">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d4332-815">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-816">Az.Monitor</span></span>
* <span data-ttu-id="d4332-817">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="d4332-817">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="d4332-818">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="d4332-818">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="d4332-819">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="d4332-819">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-820">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-820">Az.Network</span></span>
* <span data-ttu-id="d4332-821">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="d4332-821">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-822">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-822">Az.Resources</span></span>
* <span data-ttu-id="d4332-823">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-823">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="d4332-824">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="d4332-824">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-825">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-825">Az.Sql</span></span>
* <span data-ttu-id="d4332-826">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d4332-826">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-827">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-827">Az.Storage</span></span>
* <span data-ttu-id="d4332-828">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="d4332-828">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="d4332-829">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="d4332-829">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="d4332-830">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d4332-830">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="d4332-831">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="d4332-831">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="d4332-832">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="d4332-832">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="d4332-833">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d4332-833">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="d4332-834">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="d4332-834">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="d4332-835">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d4332-835">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="d4332-836">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d4332-836">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="d4332-837">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="d4332-837">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="d4332-838">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="d4332-838">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="d4332-839">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="d4332-839">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="d4332-840">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="d4332-840">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="d4332-841">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-841">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4332-842">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-842">Highlights since the last major release</span></span>
* <span data-ttu-id="d4332-843">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4332-843">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="d4332-844">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4332-844">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-845">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-845">Az.Compute</span></span>
* <span data-ttu-id="d4332-846">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d4332-846">VM Reapply feature</span></span>
    - <span data-ttu-id="d4332-847">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-847">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="d4332-848">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="d4332-848">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="d4332-849">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4332-849">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="d4332-850">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-850">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="d4332-851">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4332-851">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4332-852">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="d4332-852">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="d4332-853">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="d4332-853">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="d4332-854">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d4332-854">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="d4332-855">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4332-855">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="d4332-856">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4332-856">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d4332-857">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d4332-857">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d4332-858">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="d4332-858">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4332-859">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="d4332-859">Get the Order</span></span>
* <span data-ttu-id="d4332-860">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="d4332-860">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4332-861">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="d4332-861">Create new Order</span></span>
* <span data-ttu-id="d4332-862">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="d4332-862">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4332-863">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="d4332-863">Remove the Order</span></span>
* <span data-ttu-id="d4332-864">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="d4332-864">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="d4332-865">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="d4332-865">Now creates Local Share</span></span>
* <span data-ttu-id="d4332-866">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="d4332-866">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="d4332-867">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="d4332-867">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="d4332-868">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="d4332-868">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="d4332-869">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d4332-869">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="d4332-870">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="d4332-870">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4332-871">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="d4332-871">Gets the information about Triggers</span></span>
* <span data-ttu-id="d4332-872">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="d4332-872">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4332-873">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="d4332-873">Create new Triggers</span></span>
* <span data-ttu-id="d4332-874">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="d4332-874">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4332-875">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="d4332-875">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-876">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-876">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-877">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-877">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="d4332-878">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="d4332-878">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-879">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-879">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-880">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="d4332-880">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4332-881">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-881">Az.EventHub</span></span>
* <span data-ttu-id="d4332-882">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="d4332-882">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4332-883">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-883">Az.FrontDoor</span></span>
* <span data-ttu-id="d4332-884">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-884">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="d4332-885">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-885">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="d4332-886">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="d4332-886">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="d4332-887">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d4332-887">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-888">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-888">Az.Network</span></span>
* <span data-ttu-id="d4332-889">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-889">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d4332-890">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d4332-890">Az.PrivateDns</span></span>
* <span data-ttu-id="d4332-891">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4332-891">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-892">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-892">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-893">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="d4332-893">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="d4332-894">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4332-894">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="d4332-895">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="d4332-895">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4332-896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4332-896">Az.RedisCache</span></span>
* <span data-ttu-id="d4332-897">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="d4332-897">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="d4332-898">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="d4332-898">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="d4332-899">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="d4332-899">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-900">Az.Resources</span></span>
- <span data-ttu-id="d4332-901">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="d4332-901">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="d4332-902">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="d4332-902">Updated create policy definition help example</span></span>
- <span data-ttu-id="d4332-903">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="d4332-903">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="d4332-904">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="d4332-904">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="d4332-905">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="d4332-905">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-906">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-906">Az.Sql</span></span>
* <span data-ttu-id="d4332-907">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-907">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="d4332-908">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="d4332-908">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="d4332-909">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-909">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="d4332-910">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-910">General</span></span>
* <span data-ttu-id="d4332-911">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4332-911">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-912">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-912">Az.Accounts</span></span>
* <span data-ttu-id="d4332-913">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="d4332-913">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d4332-914">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d4332-914">Az.Advisor</span></span>
* <span data-ttu-id="d4332-915">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="d4332-915">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4332-916">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4332-916">Az.Batch</span></span>
* <span data-ttu-id="d4332-917">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d4332-917">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="d4332-918">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d4332-918">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="d4332-919">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="d4332-919">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="d4332-920">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="d4332-920">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="d4332-921">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d4332-921">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="d4332-922">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d4332-922">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="d4332-923">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="d4332-923">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="d4332-924">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="d4332-924">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="d4332-925">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="d4332-925">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="d4332-926">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d4332-926">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d4332-927">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="d4332-927">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="d4332-928">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="d4332-928">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="d4332-929">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d4332-929">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d4332-930">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="d4332-930">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="d4332-931">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="d4332-931">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="d4332-932">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="d4332-932">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="d4332-933">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d4332-933">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="d4332-934">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d4332-934">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="d4332-935">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="d4332-935">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="d4332-936">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4332-936">This operation is no longer supported.</span></span>
* <span data-ttu-id="d4332-937">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d4332-937">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d4332-938">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d4332-938">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d4332-939">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="d4332-939">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="d4332-940">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="d4332-940">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="d4332-941">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="d4332-941">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="d4332-942">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="d4332-942">New non-verified images are also now returned.</span></span> <span data-ttu-id="d4332-943">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="d4332-943">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="d4332-944">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="d4332-944">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="d4332-945">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="d4332-945">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="d4332-946">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="d4332-946">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="d4332-947">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="d4332-947">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="d4332-948">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="d4332-948">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="d4332-949">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="d4332-949">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="d4332-950">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="d4332-950">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="d4332-951">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="d4332-951">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="d4332-952">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="d4332-952">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4332-953">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-953">Az.Cdn</span></span>
* <span data-ttu-id="d4332-954">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="d4332-954">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="d4332-955">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="d4332-955">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-956">Az.Compute</span></span>
* <span data-ttu-id="d4332-957">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="d4332-957">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="d4332-958">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d4332-958">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="d4332-959">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d4332-959">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="d4332-960">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-960">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4332-961">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-961">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="d4332-962">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="d4332-962">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="d4332-963">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4332-963">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4332-964">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d4332-964">Breaking changes</span></span>
    - <span data-ttu-id="d4332-965">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="d4332-965">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="d4332-966">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4332-966">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-967">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-967">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-968">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-968">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-969">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-969">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-970">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="d4332-970">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="d4332-971">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="d4332-971">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="d4332-972">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="d4332-972">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="d4332-973">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="d4332-973">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="d4332-974">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="d4332-974">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="d4332-975">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="d4332-975">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4332-976">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-976">Az.FrontDoor</span></span>
* <span data-ttu-id="d4332-977">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="d4332-977">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4332-978">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-978">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-979">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="d4332-979">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="d4332-980">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d4332-980">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="d4332-981">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="d4332-981">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="d4332-982">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="d4332-982">Removed five cmdlets:</span></span>
    - <span data-ttu-id="d4332-983">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4332-983">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4332-984">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4332-984">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4332-985">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4332-985">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4332-986">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4332-986">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="d4332-987">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4332-987">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="d4332-988">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="d4332-988">Added three cmdlets:</span></span>
    - <span data-ttu-id="d4332-989">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d4332-989">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d4332-990">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d4332-990">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d4332-991">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d4332-991">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="d4332-992">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="d4332-992">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="d4332-993">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="d4332-993">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="d4332-994">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="d4332-994">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="d4332-995">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d4332-995">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="d4332-996">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d4332-996">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="d4332-997">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="d4332-997">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="d4332-998">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="d4332-998">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="d4332-999">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="d4332-999">Added some scenario test cases.</span></span>
* <span data-ttu-id="d4332-1000">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="d4332-1000">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-1001">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1001">Az.IotHub</span></span>
* <span data-ttu-id="d4332-1002">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d4332-1002">Breaking changes:</span></span>
    - <span data-ttu-id="d4332-1003">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1003">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4332-1004">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-1004">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4332-1005">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1005">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4332-1006">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-1006">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4332-1007">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="d4332-1007">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="d4332-1008">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="d4332-1008">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="d4332-1009">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="d4332-1009">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="d4332-1010">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="d4332-1010">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="d4332-1011">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1011">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4332-1012">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-1012">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4332-1013">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1013">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4332-1014">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="d4332-1014">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1015">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1015">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1016">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1016">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="d4332-1017">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1017">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="d4332-1018">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1018">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="d4332-1019">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1019">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="d4332-1020">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1020">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="d4332-1021">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1021">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="d4332-1022">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1022">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="d4332-1023">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1023">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="d4332-1024">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="d4332-1024">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1025">Az.Resources</span></span>
* <span data-ttu-id="d4332-1026">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="d4332-1026">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1027">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1027">Az.Network</span></span>
* <span data-ttu-id="d4332-1028">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="d4332-1028">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="d4332-1029">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d4332-1029">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4332-1030">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1030">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1031">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1031">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1032">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1032">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1033">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1033">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1034">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-1034">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d4332-1035">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="d4332-1035">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="d4332-1036">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="d4332-1036">New cmdlet:</span></span>
        - <span data-ttu-id="d4332-1037">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d4332-1037">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="d4332-1038">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="d4332-1038">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="d4332-1039">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4332-1039">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="d4332-1040">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-1040">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="d4332-1041">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="d4332-1041">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="d4332-1042">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="d4332-1042">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="d4332-1043">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="d4332-1043">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="d4332-1044">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1044">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="d4332-1045">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1045">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-1046">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d4332-1046">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="d4332-1047">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4332-1047">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4332-1048">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4332-1048">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4332-1049">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4332-1049">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4332-1050">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1050">Set-AzVirtualHub</span></span>
* <span data-ttu-id="d4332-1051">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4332-1051">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="d4332-1052">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d4332-1052">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4332-1053">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="d4332-1053">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d4332-1054">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="d4332-1054">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d4332-1055">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d4332-1055">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="d4332-1056">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d4332-1056">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="d4332-1057">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-1057">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="d4332-1058">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1058">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-1059">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-1059">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="d4332-1060">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d4332-1060">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4332-1061">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d4332-1061">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4332-1062">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d4332-1062">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4332-1063">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d4332-1063">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4332-1064">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d4332-1064">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4332-1065">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d4332-1065">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="d4332-1066">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="d4332-1066">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="d4332-1067">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1067">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-1068">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d4332-1068">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="d4332-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d4332-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="d4332-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d4332-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="d4332-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d4332-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="d4332-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="d4332-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4332-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="d4332-1074">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d4332-1074">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4332-1075">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1075">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="d4332-1076">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1076">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="d4332-1077">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="d4332-1077">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="d4332-1078">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="d4332-1078">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="d4332-1079">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="d4332-1079">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4332-1080">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d4332-1080">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="d4332-1081">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d4332-1081">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="d4332-1082">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="d4332-1082">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="d4332-1083">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="d4332-1083">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="d4332-1084">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="d4332-1084">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="d4332-1085">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1085">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-1086">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4332-1086">New-AzIpGroup</span></span>
        - <span data-ttu-id="d4332-1087">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4332-1087">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="d4332-1088">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4332-1088">Get-AzIpGroup</span></span>
        - <span data-ttu-id="d4332-1089">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4332-1089">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-1090">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-1090">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-1091">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="d4332-1091">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1092">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1092">Az.Sql</span></span>
* <span data-ttu-id="d4332-1093">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1093">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="d4332-1094">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="d4332-1094">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="d4332-1095">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="d4332-1095">Removed deprecated aliases:</span></span>
* <span data-ttu-id="d4332-1096">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="d4332-1096">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="d4332-1097">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="d4332-1097">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="d4332-1098">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-1098">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d4332-1099">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="d4332-1099">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="d4332-1100">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="d4332-1100">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="d4332-1101">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-1101">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1102">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1102">Az.Storage</span></span>
* <span data-ttu-id="d4332-1103">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d4332-1103">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="d4332-1104">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1104">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d4332-1105">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1105">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d4332-1106">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="d4332-1106">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="d4332-1107">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4332-1107">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="d4332-1108">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4332-1108">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="d4332-1109">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1109">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d4332-1110">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-1110">General</span></span>
* <span data-ttu-id="d4332-1111">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4332-1111">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-1112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1112">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1113">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="d4332-1113">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-1114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-1114">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-1115">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1115">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d4332-1116">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="d4332-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-1117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-1117">Az.Automation</span></span>
* <span data-ttu-id="d4332-1118">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="d4332-1118">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4332-1119">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4332-1119">Az.Batch</span></span>
* <span data-ttu-id="d4332-1120">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1120">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1121">Az.Compute</span></span>
* <span data-ttu-id="d4332-1122">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="d4332-1122">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4332-1123">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="d4332-1123">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d4332-1124">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="d4332-1124">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="d4332-1125">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="d4332-1125">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-1126">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-1126">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-1127">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="d4332-1127">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d4332-1128">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="d4332-1128">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d4332-1129">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1129">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-1130">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-1130">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-1131">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="d4332-1131">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d4332-1132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d4332-1132">Az.HealthcareApis</span></span>
* <span data-ttu-id="d4332-1133">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1133">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d4332-1134">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="d4332-1134">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d4332-1135">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="d4332-1135">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d4332-1136">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="d4332-1136">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-1137">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1137">Az.IotHub</span></span>
* <span data-ttu-id="d4332-1138">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="d4332-1138">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d4332-1139">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1139">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-1140">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-1140">Az.Monitor</span></span>
* <span data-ttu-id="d4332-1141">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="d4332-1141">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d4332-1142">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="d4332-1142">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d4332-1143">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="d4332-1143">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d4332-1144">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4332-1144">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1145">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1145">Az.Network</span></span>
* <span data-ttu-id="d4332-1146">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d4332-1146">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d4332-1147">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="d4332-1147">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d4332-1148">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1148">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-1149">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-1149">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d4332-1150">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1150">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d4332-1151">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="d4332-1151">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d4332-1152">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1152">Updated cmdlets:</span></span>
        - <span data-ttu-id="d4332-1153">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1153">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4332-1154">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1154">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4332-1155">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1155">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d4332-1156">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="d4332-1156">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d4332-1157">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d4332-1157">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d4332-1158">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d4332-1158">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d4332-1159">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="d4332-1159">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4332-1160">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4332-1160">Az.RedisCache</span></span>
* <span data-ttu-id="d4332-1161">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="d4332-1161">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1162">Az.Sql</span></span>
* <span data-ttu-id="d4332-1163">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="d4332-1163">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1164">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1164">Az.Storage</span></span>
* <span data-ttu-id="d4332-1165">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1165">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d4332-1166">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="d4332-1166">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d4332-1167">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d4332-1167">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d4332-1168">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="d4332-1168">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d4332-1169">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1169">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4332-1170">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4332-1170">Az.StorageSync</span></span>
* <span data-ttu-id="d4332-1171">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="d4332-1171">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1172">Az.Websites</span></span>
* <span data-ttu-id="d4332-1173">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1173">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d4332-1174">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1174">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d4332-1175">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-1175">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-1176">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="d4332-1176">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d4332-1177">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-1177">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d4332-1178">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d4332-1178">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-1179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-1179">Az.Automation</span></span>
* <span data-ttu-id="d4332-1180">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="d4332-1180">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d4332-1181">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="d4332-1181">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d4332-1182">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="d4332-1182">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1183">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1183">Az.Compute</span></span>
* <span data-ttu-id="d4332-1184">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1184">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d4332-1185">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1185">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4332-1186">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="d4332-1186">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d4332-1187">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="d4332-1187">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d4332-1188">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="d4332-1188">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d4332-1189">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="d4332-1189">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d4332-1190">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="d4332-1190">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d4332-1191">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="d4332-1191">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d4332-1192">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-1192">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-1193">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-1193">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-1194">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="d4332-1194">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d4332-1195">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="d4332-1195">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4332-1196">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-1196">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-1197">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1197">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-1198">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1198">Az.IotHub</span></span>
* <span data-ttu-id="d4332-1199">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4332-1199">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d4332-1200">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="d4332-1200">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d4332-1201">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1201">New cmdlets are:</span></span>
    - <span data-ttu-id="d4332-1202">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="d4332-1202">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4332-1203">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="d4332-1203">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4332-1204">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="d4332-1204">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4332-1205">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="d4332-1205">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-1206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-1206">Az.Monitor</span></span>
* <span data-ttu-id="d4332-1207">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="d4332-1207">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d4332-1208">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="d4332-1208">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d4332-1209">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="d4332-1209">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d4332-1210">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="d4332-1210">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d4332-1211">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="d4332-1211">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d4332-1212">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="d4332-1212">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d4332-1213">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1213">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d4332-1214">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1214">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d4332-1215">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="d4332-1215">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d4332-1216">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="d4332-1216">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d4332-1217">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="d4332-1217">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d4332-1218">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="d4332-1218">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d4332-1219">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="d4332-1219">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d4332-1220">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="d4332-1220">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d4332-1221">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="d4332-1221">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d4332-1222">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="d4332-1222">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d4332-1223">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="d4332-1223">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d4332-1224">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="d4332-1224">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d4332-1225">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-1225">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d4332-1226">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="d4332-1226">Overall improved help files</span></span>
* <span data-ttu-id="d4332-1227">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="d4332-1227">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1228">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1228">Az.Network</span></span>
* <span data-ttu-id="d4332-1229">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="d4332-1229">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="d4332-1230">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1230">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d4332-1231">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="d4332-1231">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d4332-1232">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="d4332-1232">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d4332-1233">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="d4332-1233">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d4332-1234">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="d4332-1234">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d4332-1235">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="d4332-1235">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d4332-1236">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1236">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d4332-1237">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="d4332-1237">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d4332-1238">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="d4332-1238">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d4332-1239">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1239">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d4332-1240">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="d4332-1240">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d4332-1241">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1241">New cmdlets</span></span>
        - <span data-ttu-id="d4332-1242">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="d4332-1242">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d4332-1243">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="d4332-1243">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d4332-1244">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d4332-1244">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4332-1245">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="d4332-1245">New-VpnSite</span></span>
        - <span data-ttu-id="d4332-1246">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="d4332-1246">Update-VpnSite</span></span>
        - <span data-ttu-id="d4332-1247">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="d4332-1247">New-VpnConnection</span></span>
        - <span data-ttu-id="d4332-1248">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1248">Update-VpnConnection</span></span>
* <span data-ttu-id="d4332-1249">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="d4332-1249">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1250">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1251">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="d4332-1251">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d4332-1252">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1252">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1253">Az.Resources</span></span>
* <span data-ttu-id="d4332-1254">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="d4332-1254">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-1255">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-1255">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-1256">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="d4332-1256">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d4332-1257">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="d4332-1257">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d4332-1258">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d4332-1258">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4332-1259">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="d4332-1259">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4332-1260">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="d4332-1260">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4332-1261">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="d4332-1261">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d4332-1262">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d4332-1262">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4332-1263">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d4332-1263">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4332-1264">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="d4332-1264">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4332-1265">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="d4332-1265">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4332-1266">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="d4332-1266">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d4332-1267">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="d4332-1267">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4332-1268">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="d4332-1268">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4332-1269">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="d4332-1269">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4332-1270">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="d4332-1270">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d4332-1271">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d4332-1271">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4332-1272">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4332-1272">Az.SignalR</span></span>
* <span data-ttu-id="d4332-1273">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="d4332-1273">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1274">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1274">Az.Sql</span></span>
* <span data-ttu-id="d4332-1275">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="d4332-1275">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d4332-1276">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d4332-1276">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d4332-1277">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-1277">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d4332-1278">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="d4332-1278">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d4332-1279">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d4332-1279">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1280">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1280">Az.Storage</span></span>
* <span data-ttu-id="d4332-1281">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="d4332-1281">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d4332-1282">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="d4332-1282">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d4332-1283">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4332-1283">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d4332-1284">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4332-1284">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d4332-1285">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-1285">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d4332-1286">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4332-1286">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d4332-1287">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="d4332-1287">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d4332-1288">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d4332-1288">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4332-1289">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d4332-1289">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4332-1290">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="d4332-1290">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4332-1291">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="d4332-1291">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1292">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1292">Az.Websites</span></span>
* <span data-ttu-id="d4332-1293">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="d4332-1293">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d4332-1294">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="d4332-1294">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d4332-1295">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="d4332-1295">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d4332-1296">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1296">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d4332-1297">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-1297">General</span></span>
* <span data-ttu-id="d4332-1298">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="d4332-1298">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-1299">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1299">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1300">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="d4332-1300">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d4332-1301">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d4332-1301">Az.Aks</span></span>
* <span data-ttu-id="d4332-1302">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="d4332-1302">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d4332-1303">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="d4332-1303">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-1304">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-1304">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-1305">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="d4332-1305">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d4332-1306">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1306">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d4332-1307">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1307">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d4332-1308">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="d4332-1308">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d4332-1309">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="d4332-1309">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4332-1310">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4332-1310">Az.Batch</span></span>
* <span data-ttu-id="d4332-1311">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="d4332-1311">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4332-1312">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-1312">Az.Cdn</span></span>
* <span data-ttu-id="d4332-1313">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="d4332-1313">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1314">Az.Compute</span></span>
* <span data-ttu-id="d4332-1315">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1315">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d4332-1316">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4332-1316">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d4332-1317">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d4332-1317">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d4332-1318">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-1318">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d4332-1319">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d4332-1319">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d4332-1320">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-1320">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d4332-1321">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1321">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d4332-1322">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="d4332-1322">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-1323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-1323">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-1324">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="d4332-1324">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d4332-1325">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="d4332-1325">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d4332-1326">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="d4332-1326">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d4332-1327">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="d4332-1327">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-1328">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-1328">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-1329">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="d4332-1329">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4332-1330">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1330">Az.EventHub</span></span>
* <span data-ttu-id="d4332-1331">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-1331">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d4332-1332">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="d4332-1332">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d4332-1333">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="d4332-1333">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d4332-1334">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="d4332-1334">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d4332-1335">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d4332-1335">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d4332-1336">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="d4332-1336">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-1337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-1337">Az.Monitor</span></span>
* <span data-ttu-id="d4332-1338">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="d4332-1338">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1339">Az.Network</span></span>
* <span data-ttu-id="d4332-1340">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1340">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d4332-1341">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d4332-1341">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d4332-1342">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="d4332-1342">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d4332-1343">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d4332-1343">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d4332-1344">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="d4332-1344">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="d4332-1345">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1345">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d4332-1346">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="d4332-1346">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-1347">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1347">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-1348">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="d4332-1348">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d4332-1349">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="d4332-1349">Added example</span></span>
    - <span data-ttu-id="d4332-1350">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="d4332-1350">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d4332-1351">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d4332-1351">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d4332-1352">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="d4332-1352">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1353">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1354">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1354">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1355">Az.Resources</span></span>
* <span data-ttu-id="d4332-1356">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="d4332-1356">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d4332-1357">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="d4332-1357">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d4332-1358">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="d4332-1358">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d4332-1359">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d4332-1359">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4332-1360">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4332-1360">Az.ServiceBus</span></span>
* <span data-ttu-id="d4332-1361">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-1361">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d4332-1362">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="d4332-1362">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d4332-1363">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="d4332-1363">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-1364">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-1364">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-1365">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="d4332-1365">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d4332-1366">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d4332-1366">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d4332-1367">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="d4332-1367">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d4332-1368">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="d4332-1368">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d4332-1369">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="d4332-1369">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d4332-1370">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="d4332-1370">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1371">Az.Sql</span></span>
* <span data-ttu-id="d4332-1372">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="d4332-1372">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1373">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1373">Az.Storage</span></span>
* <span data-ttu-id="d4332-1374">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="d4332-1374">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d4332-1375">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="d4332-1375">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d4332-1376">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4332-1376">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d4332-1377">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4332-1377">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d4332-1378">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="d4332-1378">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d4332-1379">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4332-1379">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1380">Az.Websites</span></span>
* <span data-ttu-id="d4332-1381">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="d4332-1381">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d4332-1382">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1382">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-1383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1383">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1384">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="d4332-1384">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d4332-1385">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1385">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d4332-1386">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="d4332-1386">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-1387">Az.Automation</span></span>
* <span data-ttu-id="d4332-1388">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4332-1388">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-1389">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1389">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-1390">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-1390">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1391">Az.Compute</span></span>
* <span data-ttu-id="d4332-1392">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d4332-1392">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d4332-1393">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4332-1393">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d4332-1394">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="d4332-1394">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d4332-1395">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="d4332-1395">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-1396">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-1396">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-1397">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1397">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d4332-1398">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="d4332-1398">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4332-1399">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1399">Az.EventHub</span></span>
* <span data-ttu-id="d4332-1400">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="d4332-1400">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d4332-1401">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="d4332-1401">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-1402">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-1402">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-1403">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1403">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4332-1404">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4332-1404">Az.LogicApp</span></span>
* <span data-ttu-id="d4332-1405">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="d4332-1405">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d4332-1406">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="d4332-1406">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d4332-1407">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1407">Az.ManagedServices</span></span>
* <span data-ttu-id="d4332-1408">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="d4332-1408">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1409">Az.Network</span></span>
* <span data-ttu-id="d4332-1410">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="d4332-1410">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d4332-1411">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1411">New cmdlets</span></span>
        - <span data-ttu-id="d4332-1412">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d4332-1412">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4332-1413">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d4332-1413">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4332-1414">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1414">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1415">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1415">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1416">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1416">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1417">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1417">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4332-1418">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="d4332-1418">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d4332-1419">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d4332-1419">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d4332-1420">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1420">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d4332-1421">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1421">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d4332-1422">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1422">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d4332-1423">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1423">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d4332-1424">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="d4332-1424">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d4332-1425">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1425">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d4332-1426">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1426">Updated cmdlets</span></span>
        - <span data-ttu-id="d4332-1427">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1427">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4332-1428">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1428">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4332-1429">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1429">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d4332-1430">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1430">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d4332-1431">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-1431">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d4332-1432">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d4332-1432">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4332-1433">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1433">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d4332-1434">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1434">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d4332-1435">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d4332-1435">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d4332-1436">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="d4332-1436">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d4332-1437">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="d4332-1437">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d4332-1438">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="d4332-1438">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-1439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1439">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-1440">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="d4332-1440">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="d4332-1441">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1441">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1442">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1442">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1443">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1443">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d4332-1444">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1444">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d4332-1445">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1445">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d4332-1446">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1446">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d4332-1447">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1447">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d4332-1448">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1448">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d4332-1449">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1449">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d4332-1450">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1450">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d4332-1451">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1451">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d4332-1452">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="d4332-1452">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1453">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1453">Az.Resources</span></span>
- <span data-ttu-id="d4332-1454">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-1454">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d4332-1455">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d4332-1455">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4332-1456">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4332-1456">Az.ServiceBus</span></span>
* <span data-ttu-id="d4332-1457">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="d4332-1457">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d4332-1458">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="d4332-1458">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1459">Az.Sql</span></span>
* <span data-ttu-id="d4332-1460">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="d4332-1460">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d4332-1461">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d4332-1461">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d4332-1462">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1462">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1463">Az.Storage</span></span>
* <span data-ttu-id="d4332-1464">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1464">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4332-1465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4332-1465">Az.StorageSync</span></span>
* <span data-ttu-id="d4332-1466">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="d4332-1466">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d4332-1467">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="d4332-1467">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1468">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1468">Az.Websites</span></span>
* <span data-ttu-id="d4332-1469">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="d4332-1469">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d4332-1470">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="d4332-1470">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d4332-1471">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="d4332-1471">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d4332-1472">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1472">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-1473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1473">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1474">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="d4332-1474">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d4332-1475">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1475">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d4332-1476">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="d4332-1476">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d4332-1477">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d4332-1477">Az.Advisor</span></span>
* <span data-ttu-id="d4332-1478">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="d4332-1478">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d4332-1479">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="d4332-1479">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4332-1480">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-1480">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-1481">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="d4332-1481">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d4332-1482">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d4332-1482">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d4332-1483">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="d4332-1483">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d4332-1484">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="d4332-1484">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d4332-1485">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="d4332-1485">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d4332-1486">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d4332-1486">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d4332-1487">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1487">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-1488">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-1488">Az.Automation</span></span>
* <span data-ttu-id="d4332-1489">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1489">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1490">Az.Compute</span></span>
* <span data-ttu-id="d4332-1491">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="d4332-1491">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-1492">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-1493">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="d4332-1493">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4332-1494">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4332-1494">Az.EventGrid</span></span>
* <span data-ttu-id="d4332-1495">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d4332-1495">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-1496">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1496">Az.IotHub</span></span>
* <span data-ttu-id="d4332-1497">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="d4332-1497">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1498">Az.Network</span></span>
* <span data-ttu-id="d4332-1499">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="d4332-1499">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d4332-1500">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="d4332-1500">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-1501">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1501">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-1502">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d4332-1502">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d4332-1503">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="d4332-1503">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-1504">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1504">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-1505">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="d4332-1505">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1506">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1507">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="d4332-1507">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1508">Az.Resources</span></span>
    - <span data-ttu-id="d4332-1509">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="d4332-1509">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d4332-1510">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="d4332-1510">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d4332-1511">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-1511">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d4332-1512">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="d4332-1512">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4332-1513">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4332-1513">Az.ServiceBus</span></span>
* <span data-ttu-id="d4332-1514">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="d4332-1514">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1515">Az.Sql</span></span>
* <span data-ttu-id="d4332-1516">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1516">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d4332-1517">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="d4332-1517">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d4332-1518">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4332-1518">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4332-1519">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4332-1519">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4332-1520">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4332-1520">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4332-1521">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4332-1521">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d4332-1522">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4332-1522">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d4332-1523">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4332-1523">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d4332-1524">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d4332-1524">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1525">Az.Storage</span></span>
* <span data-ttu-id="d4332-1526">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="d4332-1526">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d4332-1527">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4332-1527">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d4332-1528">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="d4332-1528">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d4332-1529">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d4332-1529">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d4332-1530">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="d4332-1530">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d4332-1531">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1531">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d4332-1532">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1532">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d4332-1533">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="d4332-1533">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d4332-1534">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4332-1534">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d4332-1535">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4332-1535">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4332-1536">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4332-1536">Az.StorageSync</span></span>
* <span data-ttu-id="d4332-1537">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="d4332-1537">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d4332-1538">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1538">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-1539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1539">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1540">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="d4332-1540">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d4332-1541">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="d4332-1541">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d4332-1542">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="d4332-1542">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d4332-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d4332-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d4332-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="d4332-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1545">Az.Compute</span></span>
* <span data-ttu-id="d4332-1546">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-1546">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d4332-1547">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-1547">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d4332-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d4332-1548">Az.Dns</span></span>
* <span data-ttu-id="d4332-1549">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="d4332-1549">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4332-1550">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4332-1550">Az.EventGrid</span></span>
* <span data-ttu-id="d4332-1551">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d4332-1551">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d4332-1552">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1552">New cmdlets:</span></span>
    - <span data-ttu-id="d4332-1553">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4332-1553">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4332-1554">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1554">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4332-1555">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4332-1555">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4332-1556">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1556">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d4332-1557">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4332-1557">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4332-1558">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1558">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4332-1559">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d4332-1559">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d4332-1560">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1560">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4332-1561">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d4332-1561">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d4332-1562">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="d4332-1562">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d4332-1563">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d4332-1563">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d4332-1564">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1564">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d4332-1565">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d4332-1565">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d4332-1566">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1566">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="d4332-1567">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d4332-1567">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d4332-1568">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1568">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d4332-1569">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-1569">Updated cmdlets:</span></span>
    - <span data-ttu-id="d4332-1570">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d4332-1570">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d4332-1571">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1571">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d4332-1572">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1572">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d4332-1573">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d4332-1573">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d4332-1574">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="d4332-1574">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d4332-1575">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="d4332-1575">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d4332-1576">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="d4332-1576">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d4332-1577">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1577">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d4332-1578">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="d4332-1578">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="d4332-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d4332-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d4332-1580">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1580">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d4332-1581">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d4332-1581">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d4332-1582">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1582">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d4332-1583">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1583">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4332-1584">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-1584">Az.FrontDoor</span></span>
* <span data-ttu-id="d4332-1585">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d4332-1585">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d4332-1586">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="d4332-1586">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d4332-1587">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4332-1587">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d4332-1588">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1588">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1589">Az.Network</span></span>
* <span data-ttu-id="d4332-1590">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1590">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d4332-1591">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1591">New cmdlets</span></span>
        - <span data-ttu-id="d4332-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d4332-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d4332-1593">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="d4332-1593">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d4332-1594">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1594">New cmdlets</span></span>
        - <span data-ttu-id="d4332-1595">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d4332-1595">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d4332-1596">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="d4332-1596">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d4332-1597">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1597">New cmdlets</span></span>
        - <span data-ttu-id="d4332-1598">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4332-1598">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4332-1599">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4332-1599">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4332-1600">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4332-1600">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4332-1601">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-1601">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d4332-1602">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-1602">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d4332-1603">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d4332-1603">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d4332-1604">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1604">New cmdlets</span></span>
        - <span data-ttu-id="d4332-1605">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4332-1605">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4332-1606">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4332-1606">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4332-1607">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4332-1607">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4332-1608">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d4332-1608">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d4332-1609">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1609">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d4332-1610">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1610">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d4332-1611">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1611">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d4332-1612">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="d4332-1612">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d4332-1613">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="d4332-1613">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d4332-1614">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="d4332-1614">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d4332-1615">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-1615">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d4332-1616">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="d4332-1616">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d4332-1617">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-1617">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d4332-1618">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="d4332-1618">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d4332-1619">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d4332-1619">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d4332-1620">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="d4332-1620">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d4332-1621">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="d4332-1621">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d4332-1622">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1622">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d4332-1623">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d4332-1623">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d4332-1624">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1624">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d4332-1625">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1625">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d4332-1626">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-1626">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d4332-1627">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="d4332-1627">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="d4332-1628">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1628">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="d4332-1629">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d4332-1629">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d4332-1630">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d4332-1630">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d4332-1631">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d4332-1631">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-1632">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1632">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-1633">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d4332-1633">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1634">Az.Resources</span></span>
* <span data-ttu-id="d4332-1635">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="d4332-1635">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d4332-1636">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="d4332-1636">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d4332-1637">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="d4332-1637">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d4332-1638">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1638">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-1639">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-1640">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d4332-1640">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1641">Az.Sql</span></span>
* <span data-ttu-id="d4332-1642">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="d4332-1642">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d4332-1643">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="d4332-1643">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d4332-1644">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="d4332-1644">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d4332-1645">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4332-1645">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4332-1646">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4332-1646">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4332-1647">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4332-1647">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4332-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d4332-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d4332-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d4332-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1650">Az.Storage</span></span>
* <span data-ttu-id="d4332-1651">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1651">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d4332-1652">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1652">New-AzStorageAccount</span></span>
* <span data-ttu-id="d4332-1653">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1653">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d4332-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1655">Az.Websites</span></span>
* <span data-ttu-id="d4332-1656">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d4332-1656">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d4332-1657">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="d4332-1657">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d4332-1658">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1658">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d4332-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-1659">Az.Cdn</span></span>
* <span data-ttu-id="d4332-1660">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="d4332-1660">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1661">Az.Compute</span></span>
* <span data-ttu-id="d4332-1662">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="d4332-1662">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d4332-1663">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-1663">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4332-1664">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1664">Az.EventHub</span></span>
* <span data-ttu-id="d4332-1665">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="d4332-1665">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d4332-1666">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="d4332-1666">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1667">Az.Network</span></span>
* <span data-ttu-id="d4332-1668">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="d4332-1668">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d4332-1669">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-1669">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-1670">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1670">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-1671">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="d4332-1671">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1672">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1673">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="d4332-1673">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4332-1674">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4332-1674">Az.ServiceBus</span></span>
* <span data-ttu-id="d4332-1675">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="d4332-1675">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-1676">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-1676">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-1677">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="d4332-1677">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d4332-1678">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d4332-1678">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1679">Az.Sql</span></span>
* <span data-ttu-id="d4332-1680">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1680">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d4332-1681">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="d4332-1681">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d4332-1682">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="d4332-1682">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d4332-1683">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="d4332-1683">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1684">Az.Websites</span></span>
* <span data-ttu-id="d4332-1685">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="d4332-1685">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d4332-1686">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1686">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d4332-1687">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-1687">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-1688">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1688">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d4332-1689">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1689">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d4332-1690">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1690">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d4332-1691">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="d4332-1691">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d4332-1692">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="d4332-1692">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d4332-1693">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="d4332-1693">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d4332-1694">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1694">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d4332-1695">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1695">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d4332-1696">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d4332-1696">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d4332-1697">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1697">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d4332-1698">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1698">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d4332-1699">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="d4332-1699">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d4332-1700">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="d4332-1700">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d4332-1701">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1701">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d4332-1702">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1702">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d4332-1703">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1703">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d4332-1704">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1704">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d4332-1705">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1705">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d4332-1706">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4332-1706">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="d4332-1707">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="d4332-1707">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d4332-1708">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-1708">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d4332-1709">**Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="d4332-1709">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d4332-1710">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="d4332-1710">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d4332-1711">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d4332-1711">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="d4332-1712">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="d4332-1712">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d4332-1713">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="d4332-1713">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d4332-1714">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="d4332-1714">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d4332-1715">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d4332-1715">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d4332-1716">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d4332-1716">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d4332-1717">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-1717">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d4332-1718">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d4332-1718">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="d4332-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d4332-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d4332-1720">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1720">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d4332-1721">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="d4332-1721">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d4332-1722">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1722">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d4332-1723">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="d4332-1723">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d4332-1724">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1724">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d4332-1725">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="d4332-1725">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d4332-1726">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="d4332-1726">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d4332-1727">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="d4332-1727">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d4332-1728">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1728">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d4332-1729">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-1729">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d4332-1730">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="d4332-1730">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d4332-1731">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d4332-1732">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="d4332-1732">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d4332-1733">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1733">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d4332-1734">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-1734">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d4332-1735">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1735">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d4332-1736">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="d4332-1736">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d4332-1737">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="d4332-1737">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d4332-1738">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1738">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d4332-1739">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="d4332-1739">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d4332-1740">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="d4332-1740">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d4332-1741">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="d4332-1741">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d4332-1742">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="d4332-1742">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d4332-1743">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-1743">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d4332-1744">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d4332-1744">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d4332-1745">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d4332-1746">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d4332-1747">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d4332-1747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d4332-1748">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d4332-1748">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d4332-1749">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1749">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d4332-1750">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1750">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d4332-1751">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d4332-1751">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d4332-1752">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-1752">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d4332-1753">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d4332-1753">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d4332-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d4332-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d4332-1755">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="d4332-1755">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d4332-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d4332-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d4332-1757">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-1757">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d4332-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d4332-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d4332-1759">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="d4332-1759">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d4332-1760">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="d4332-1760">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d4332-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d4332-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d4332-1762">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="d4332-1762">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="d4332-1763">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-1763">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d4332-1764">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="d4332-1764">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-1765">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-1765">Az.Automation</span></span>
* <span data-ttu-id="d4332-1766">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="d4332-1766">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d4332-1767">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="d4332-1767">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d4332-1768">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="d4332-1768">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d4332-1769">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="d4332-1769">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d4332-1770">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="d4332-1770">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d4332-1771">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="d4332-1771">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d4332-1772">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="d4332-1772">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1773">Az.Compute</span></span>
* <span data-ttu-id="d4332-1774">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-1774">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d4332-1775">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4332-1775">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-1776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-1776">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-1777">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-1777">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-1778">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-1778">Az.Monitor</span></span>
* <span data-ttu-id="d4332-1779">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="d4332-1779">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1780">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1780">Az.Network</span></span>
* <span data-ttu-id="d4332-1781">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1781">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d4332-1782">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="d4332-1782">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4332-1783">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="d4332-1783">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d4332-1784">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="d4332-1784">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1785">Az.Resources</span></span>
* <span data-ttu-id="d4332-1786">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="d4332-1786">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1787">Az.Sql</span></span>
* <span data-ttu-id="d4332-1788">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4332-1788">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d4332-1789">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1789">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1790">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1791">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="d4332-1791">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-1792">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1792">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-1793">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="d4332-1793">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d4332-1794">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d4332-1794">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1795">Az.Compute</span></span>
* <span data-ttu-id="d4332-1796">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d4332-1796">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d4332-1797">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d4332-1797">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d4332-1798">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-1798">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d4332-1799">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d4332-1799">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d4332-1800">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d4332-1800">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d4332-1801">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4332-1801">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="d4332-1802">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="d4332-1802">Breaking changes</span></span>
    - <span data-ttu-id="d4332-1803">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d4332-1803">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d4332-1804">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d4332-1804">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d4332-1805">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d4332-1805">Az.DeploymentManager</span></span>
* <span data-ttu-id="d4332-1806">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="d4332-1806">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d4332-1807">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d4332-1807">Az.Dns</span></span>
* <span data-ttu-id="d4332-1808">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="d4332-1808">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d4332-1809">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1809">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d4332-1810">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="d4332-1810">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4332-1811">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-1811">Az.FrontDoor</span></span>
* <span data-ttu-id="d4332-1812">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="d4332-1812">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d4332-1813">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="d4332-1813">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d4332-1814">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-1814">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-1815">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="d4332-1815">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d4332-1816">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4332-1816">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d4332-1817">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4332-1817">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d4332-1818">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="d4332-1818">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d4332-1819">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="d4332-1819">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d4332-1820">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="d4332-1820">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d4332-1821">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="d4332-1821">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-1822">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-1822">Az.Monitor</span></span>
* <span data-ttu-id="d4332-1823">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="d4332-1823">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="d4332-1824">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d4332-1824">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d4332-1825">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d4332-1825">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d4332-1826">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d4332-1826">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d4332-1827">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d4332-1827">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d4332-1828">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d4332-1828">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d4332-1829">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d4332-1829">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d4332-1830">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1830">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4332-1831">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1831">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4332-1832">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1832">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4332-1833">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1833">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4332-1834">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4332-1834">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4332-1835">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="d4332-1835">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d4332-1836">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="d4332-1836">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1837">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1837">Az.Network</span></span>
* <span data-ttu-id="d4332-1838">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="d4332-1838">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d4332-1839">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1839">New cmdlets</span></span>
        - <span data-ttu-id="d4332-1840">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-1840">New-AzNatGateway</span></span>
        - <span data-ttu-id="d4332-1841">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-1841">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d4332-1842">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-1842">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d4332-1843">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-1843">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d4332-1844">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="d4332-1844">Updated cmdlets</span></span>
        - <span data-ttu-id="d4332-1845">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d4332-1845">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d4332-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d4332-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d4332-1847">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="d4332-1847">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d4332-1848">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1848">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d4332-1849">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1849">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-1850">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1850">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-1851">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1851">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d4332-1852">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d4332-1852">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d4332-1853">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="d4332-1853">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1854">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1854">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1855">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4332-1855">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d4332-1856">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4332-1856">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d4332-1857">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4332-1857">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d4332-1858">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="d4332-1858">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d4332-1859">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="d4332-1859">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d4332-1860">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="d4332-1860">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d4332-1861">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d4332-1861">Az.Relay</span></span>
* <span data-ttu-id="d4332-1862">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1862">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4332-1863">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4332-1863">Az.ServiceBus</span></span>
* <span data-ttu-id="d4332-1864">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d4332-1864">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1865">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1865">Az.Storage</span></span>
* <span data-ttu-id="d4332-1866">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="d4332-1866">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d4332-1867">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="d4332-1867">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d4332-1868">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d4332-1868">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d4332-1869">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1869">New-AzStorageAccount</span></span>
* <span data-ttu-id="d4332-1870">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="d4332-1870">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d4332-1871">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1871">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d4332-1872">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1872">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d4332-1873">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-1873">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1874">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1874">Az.Websites</span></span>
* <span data-ttu-id="d4332-1875">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="d4332-1875">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d4332-1876">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="d4332-1876">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d4332-1877">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1877">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4332-1878">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-1878">Highlights since the last major release</span></span>
* <span data-ttu-id="d4332-1879">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="d4332-1879">General availability of `Az` module</span></span>
* <span data-ttu-id="d4332-1880">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4332-1880">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4332-1881">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4332-1881">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4332-1882">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d4332-1882">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4332-1883">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d4332-1883">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4332-1884">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="d4332-1884">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4332-1885">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="d4332-1885">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-1886">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1886">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1887">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="d4332-1887">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4332-1888">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4332-1888">Az.Batch</span></span>
* <span data-ttu-id="d4332-1889">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4332-1890">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-1890">Az.Cdn</span></span>
* <span data-ttu-id="d4332-1891">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1891">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-1892">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1892">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-1893">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1894">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1894">Az.Compute</span></span>
* <span data-ttu-id="d4332-1895">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="d4332-1895">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d4332-1896">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1896">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4332-1897">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d4332-1897">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-1898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-1898">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-1899">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d4332-1899">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-1900">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-1900">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-1901">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4332-1902">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4332-1902">Az.EventGrid</span></span>
* <span data-ttu-id="d4332-1903">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d4332-1903">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4332-1904">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1904">Az.EventHub</span></span>
* <span data-ttu-id="d4332-1905">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d4332-1905">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4332-1906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4332-1906">Az.HDInsight</span></span>
* <span data-ttu-id="d4332-1907">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-1908">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-1908">Az.IotHub</span></span>
* <span data-ttu-id="d4332-1909">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1909">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-1910">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-1910">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-1911">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4332-1912">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d4332-1912">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d4332-1913">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4332-1913">Az.MachineLearning</span></span>
* <span data-ttu-id="d4332-1914">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1914">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d4332-1915">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d4332-1915">Az.Media</span></span>
* <span data-ttu-id="d4332-1916">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1916">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-1917">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-1917">Az.Monitor</span></span>
  * <span data-ttu-id="d4332-1918">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="d4332-1918">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d4332-1919">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d4332-1919">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d4332-1920">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d4332-1920">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d4332-1921">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4332-1921">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d4332-1922">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4332-1922">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d4332-1923">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4332-1923">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d4332-1924">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-1924">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-1925">Az.Network</span></span>
* <span data-ttu-id="d4332-1926">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4332-1927">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d4332-1927">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d4332-1928">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d4332-1928">Az.NotificationHubs</span></span>
* <span data-ttu-id="d4332-1929">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-1930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-1930">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-1931">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d4332-1932">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d4332-1932">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d4332-1933">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1933">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-1934">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1934">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-1935">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1935">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4332-1936">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1936">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d4332-1937">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1937">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d4332-1938">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="d4332-1938">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4332-1939">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4332-1939">Az.RedisCache</span></span>
* <span data-ttu-id="d4332-1940">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1940">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1941">Az.Resources</span></span>
* <span data-ttu-id="d4332-1942">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d4332-1942">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1943">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1943">Az.Sql</span></span>
* <span data-ttu-id="d4332-1944">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="d4332-1944">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d4332-1945">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4332-1946">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1946">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d4332-1947">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="d4332-1947">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d4332-1948">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1948">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d4332-1949">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d4332-1949">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d4332-1950">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="d4332-1950">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-1951">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-1951">Az.Websites</span></span>
* <span data-ttu-id="d4332-1952">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="d4332-1952">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d4332-1953">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="d4332-1953">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4332-1954">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1954">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d4332-1955">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d4332-1955">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d4332-1956">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-1956">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4332-1957">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-1957">Highlights since the last major release</span></span>
* <span data-ttu-id="d4332-1958">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="d4332-1958">General availability of `Az` module</span></span>
* <span data-ttu-id="d4332-1959">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4332-1959">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4332-1960">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4332-1960">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4332-1961">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d4332-1961">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4332-1962">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d4332-1962">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4332-1963">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="d4332-1963">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4332-1964">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="d4332-1964">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4332-1965">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-1965">Az.Accounts</span></span>
* <span data-ttu-id="d4332-1966">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="d4332-1966">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4332-1967">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4332-1967">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4332-1968">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d4332-1968">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d4332-1969">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="d4332-1969">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-1970">Az.Automation</span></span>
* <span data-ttu-id="d4332-1971">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="d4332-1971">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d4332-1972">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="d4332-1972">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d4332-1973">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1973">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-1974">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-1974">Az.Compute</span></span>
* <span data-ttu-id="d4332-1975">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="d4332-1975">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4332-1976">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1976">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d4332-1977">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4332-1977">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4332-1978">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="d4332-1978">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-1979">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-1979">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-1980">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="d4332-1980">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d4332-1981">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-1981">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-1982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-1982">Az.Resources</span></span>
* <span data-ttu-id="d4332-1983">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="d4332-1983">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d4332-1984">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-1984">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d4332-1985">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="d4332-1985">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d4332-1986">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="d4332-1986">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d4332-1987">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="d4332-1987">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d4332-1988">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="d4332-1988">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-1989">Az.Sql</span></span>
* <span data-ttu-id="d4332-1990">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-1990">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-1991">Az.Storage</span></span>
* <span data-ttu-id="d4332-1992">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-1992">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d4332-1993">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4332-1993">New-AzStorageContext</span></span>
* <span data-ttu-id="d4332-1994">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="d4332-1994">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d4332-1995">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d4332-1995">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d4332-1996">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d4332-1996">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d4332-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d4332-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d4332-1999">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="d4332-1999">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d4332-2000">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4332-2000">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d4332-2001">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4332-2001">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d4332-2002">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4332-2002">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d4332-2003">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4332-2003">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d4332-2004">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2004">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4332-2005">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="d4332-2005">Highlights since the last major release</span></span>
* <span data-ttu-id="d4332-2006">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="d4332-2006">General availability of `Az` module</span></span>
* <span data-ttu-id="d4332-2007">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4332-2007">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4332-2008">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4332-2008">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4332-2009">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="d4332-2009">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4332-2010">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d4332-2010">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4332-2011">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="d4332-2011">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4332-2012">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="d4332-2012">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-2013">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-2013">Az.Automation</span></span>
* <span data-ttu-id="d4332-2014">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="d4332-2014">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d4332-2015">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="d4332-2015">Dynamic grouping</span></span>
    * <span data-ttu-id="d4332-2016">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="d4332-2016">Pre-Post script</span></span>
    * <span data-ttu-id="d4332-2017">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2017">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2018">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2018">Az.Compute</span></span>
* <span data-ttu-id="d4332-2019">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="d4332-2019">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d4332-2020">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-2020">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-2021">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-2021">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-2022">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d4332-2022">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-2023">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2023">Az.Network</span></span>
* <span data-ttu-id="d4332-2024">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2024">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d4332-2025">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d4332-2025">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-2026">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2026">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-2027">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4332-2027">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d4332-2028">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="d4332-2028">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2029">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2029">Az.Resources</span></span>
* <span data-ttu-id="d4332-2030">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-2030">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d4332-2031">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="d4332-2031">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-2032">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2032">Az.Sql</span></span>
* <span data-ttu-id="d4332-2033">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="d4332-2033">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-2034">Az.Storage</span></span>
* <span data-ttu-id="d4332-2035">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-2035">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d4332-2036">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-2036">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4332-2037">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-2037">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4332-2038">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4332-2038">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4332-2039">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d4332-2039">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d4332-2040">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d4332-2040">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d4332-2041">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d4332-2041">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-2042">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-2042">Az.Websites</span></span>
* <span data-ttu-id="d4332-2043">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="d4332-2043">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="d4332-2044">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2044">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-2045">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-2045">Az.Accounts</span></span>
* <span data-ttu-id="d4332-2046">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="d4332-2046">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d4332-2047">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="d4332-2047">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-2048">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-2048">Az.Automation</span></span>
* <span data-ttu-id="d4332-2049">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2049">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d4332-2050">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2050">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d4332-2051">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="d4332-2051">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4332-2052">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-2052">Az.Cdn</span></span>
* <span data-ttu-id="d4332-2053">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="d4332-2053">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2054">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2054">Az.Compute</span></span>
* <span data-ttu-id="d4332-2055">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="d4332-2055">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-2056">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-2056">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-2057">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="d4332-2057">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4332-2058">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4332-2058">Az.LogicApp</span></span>
* <span data-ttu-id="d4332-2059">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="d4332-2059">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-2060">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2060">Az.Network</span></span>
* <span data-ttu-id="d4332-2061">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="d4332-2061">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-2062">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2062">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-2063">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2063">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d4332-2064">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="d4332-2064">SDK Update</span></span>
* <span data-ttu-id="d4332-2065">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="d4332-2065">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d4332-2066">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="d4332-2066">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2067">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2067">Az.Resources</span></span>
* <span data-ttu-id="d4332-2068">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="d4332-2068">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d4332-2069">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="d4332-2069">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d4332-2070">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="d4332-2070">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d4332-2071">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="d4332-2071">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d4332-2072">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="d4332-2072">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d4332-2073">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="d4332-2073">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-2074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2074">Az.Sql</span></span>
* <span data-ttu-id="d4332-2075">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="d4332-2075">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d4332-2076">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="d4332-2076">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-2077">Az.Storage</span></span>
* <span data-ttu-id="d4332-2078">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="d4332-2078">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d4332-2079">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2079">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d4332-2080">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2080">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4332-2081">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="d4332-2081">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-2082">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-2082">Az.Automation</span></span>
* <span data-ttu-id="d4332-2083">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-2083">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d4332-2084">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-2084">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d4332-2085">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-2085">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-2087">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4332-2087">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2088">Az.Compute</span></span>
* <span data-ttu-id="d4332-2089">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="d4332-2089">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d4332-2090">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="d4332-2090">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d4332-2091">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d4332-2091">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d4332-2092">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d4332-2092">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-2093">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-2093">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-2094">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="d4332-2094">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4332-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4332-2095">Az.EventHub</span></span>
* <span data-ttu-id="d4332-2096">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="d4332-2096">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-2097">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-2097">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-2098">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="d4332-2098">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4332-2099">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4332-2099">Az.LogicApp</span></span>
* <span data-ttu-id="d4332-2100">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="d4332-2100">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d4332-2101">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-2101">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d4332-2102">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="d4332-2102">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d4332-2103">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="d4332-2103">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4332-2104">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="d4332-2104">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4332-2105">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="d4332-2105">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4332-2106">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="d4332-2106">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d4332-2107">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="d4332-2107">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d4332-2108">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d4332-2108">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4332-2109">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d4332-2109">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4332-2110">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="d4332-2110">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4332-2111">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4332-2111">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d4332-2112">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-2112">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4332-2113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-2113">Az.Monitor</span></span>
* <span data-ttu-id="d4332-2114">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="d4332-2114">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-2115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2115">Az.Network</span></span>
* <span data-ttu-id="d4332-2116">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="d4332-2116">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-2117">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-2117">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4332-2118">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="d4332-2118">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d4332-2119">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d4332-2119">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="d4332-2120">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="d4332-2120">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2121">Az.Resources</span></span>
* <span data-ttu-id="d4332-2122">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="d4332-2122">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d4332-2123">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="d4332-2123">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d4332-2124">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="d4332-2124">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d4332-2125">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="d4332-2125">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-2126">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2126">Az.Sql</span></span>
* <span data-ttu-id="d4332-2127">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d4332-2127">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d4332-2128">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="d4332-2128">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-2129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-2129">Az.Websites</span></span>
* <span data-ttu-id="d4332-2130">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="d4332-2130">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d4332-2131">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2131">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-2132">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-2132">Az.Accounts</span></span>
* <span data-ttu-id="d4332-2133">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d4332-2133">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4332-2134">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2134">Az.AnalysisServices</span></span>
<span data-ttu-id="d4332-2135">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="d4332-2135">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2136">Az.Compute</span></span>
* <span data-ttu-id="d4332-2137">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="d4332-2137">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d4332-2138">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="d4332-2138">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d4332-2139">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="d4332-2139">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-2140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2140">Az.RecoveryServices</span></span>
<span data-ttu-id="d4332-2141">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="d4332-2141">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2142">Az.Resources</span></span>
* <span data-ttu-id="d4332-2143">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2143">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="d4332-2144">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="d4332-2144">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d4332-2145">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="d4332-2145">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="d4332-2146">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="d4332-2146">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2147">Az.Sql</span></span>
* <span data-ttu-id="d4332-2148">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4332-2148">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d4332-2149">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2149">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d4332-2150">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="d4332-2150">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d4332-2151">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2151">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-2152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-2152">Az.Accounts</span></span>
* <span data-ttu-id="d4332-2153">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="d4332-2153">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4332-2154">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2154">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4332-2155">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="d4332-2155">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-2156">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2156">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4332-2157">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="d4332-2157">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d4332-2158">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2158">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-2159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-2159">Az.Accounts</span></span>
* <span data-ttu-id="d4332-2160">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="d4332-2160">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4332-2161">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4332-2162">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="d4332-2162">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d4332-2163">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d4332-2163">Az.Aks</span></span>
* <span data-ttu-id="d4332-2164">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2164">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4332-2165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-2165">Az.Automation</span></span>
* <span data-ttu-id="d4332-2166">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="d4332-2166">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d4332-2167">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2167">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4332-2168">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4332-2168">Az.Cdn</span></span>
* <span data-ttu-id="d4332-2169">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2169">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2170">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2170">Az.Compute</span></span>
* <span data-ttu-id="d4332-2171">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="d4332-2171">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d4332-2172">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4332-2172">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d4332-2173">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4332-2173">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d4332-2174">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4332-2174">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d4332-2175">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2175">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4332-2176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4332-2176">Az.DataFactory</span></span>
* <span data-ttu-id="d4332-2177">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-2177">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-2178">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-2178">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-2179">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="d4332-2179">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d4332-2180">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="d4332-2180">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d4332-2181">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2181">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-2182">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-2182">Az.IotHub</span></span>
* <span data-ttu-id="d4332-2183">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d4332-2183">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4332-2184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-2184">Az.KeyVault</span></span>
* <span data-ttu-id="d4332-2185">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2185">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-2186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2186">Az.Network</span></span>
* <span data-ttu-id="d4332-2187">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2187">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2188">Az.Resources</span></span>
* <span data-ttu-id="d4332-2189">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="d4332-2189">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d4332-2190">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2190">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d4332-2191">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4332-2191">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d4332-2192">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="d4332-2192">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d4332-2193">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="d4332-2193">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d4332-2194">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-2194">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d4332-2195">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="d4332-2195">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-2196">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-2196">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-2197">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="d4332-2197">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d4332-2198">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d4332-2198">Fix some error messages.</span></span>
* <span data-ttu-id="d4332-2199">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="d4332-2199">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d4332-2200">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="d4332-2200">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4332-2201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4332-2201">Az.SignalR</span></span>
* <span data-ttu-id="d4332-2202">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2202">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-2203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2203">Az.Sql</span></span>
* <span data-ttu-id="d4332-2204">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2204">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4332-2205">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d4332-2205">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d4332-2206">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="d4332-2206">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d4332-2207">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="d4332-2207">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-2208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-2208">Az.Storage</span></span>
* <span data-ttu-id="d4332-2209">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2209">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4332-2210">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="d4332-2210">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d4332-2211">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d4332-2211">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d4332-2212">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d4332-2212">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d4332-2213">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d4332-2213">Az.TrafficManager</span></span>
* <span data-ttu-id="d4332-2214">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2214">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-2215">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-2215">Az.Websites</span></span>
* <span data-ttu-id="d4332-2216">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2216">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4332-2217">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="d4332-2217">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d4332-2218">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="d4332-2218">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d4332-2219">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2219">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4332-2220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-2220">Az.Accounts</span></span>
* <span data-ttu-id="d4332-2221">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="d4332-2221">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2222">Az.Compute</span></span>
* <span data-ttu-id="d4332-2223">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="d4332-2223">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d4332-2224">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="d4332-2224">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d4332-2225">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d4332-2225">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-2227">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="d4332-2227">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d4332-2228">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2228">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4332-2229">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4332-2229">Az.EventGrid</span></span>
* <span data-ttu-id="d4332-2230">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d4332-2230">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d4332-2231">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d4332-2231">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d4332-2232">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="d4332-2232">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d4332-2233">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="d4332-2233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d4332-2234">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="d4332-2234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d4332-2235">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d4332-2235">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d4332-2236">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="d4332-2236">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d4332-2237">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="d4332-2237">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d4332-2238">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="d4332-2238">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d4332-2239">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d4332-2239">Dead letter endpoint.</span></span>
* <span data-ttu-id="d4332-2240">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d4332-2240">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d4332-2241">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="d4332-2241">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4332-2242">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4332-2242">Az.IotHub</span></span>
* <span data-ttu-id="d4332-2243">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="d4332-2243">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4332-2244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4332-2244">Az.LogicApp</span></span>
* <span data-ttu-id="d4332-2245">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="d4332-2245">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2246">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2246">Az.Resources</span></span>
* <span data-ttu-id="d4332-2247">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="d4332-2247">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d4332-2248">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="d4332-2248">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d4332-2249">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4332-2249">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d4332-2250">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="d4332-2250">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d4332-2251">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="d4332-2251">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d4332-2252">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="d4332-2252">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4332-2253">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4332-2253">Az.SignalR</span></span>
* <span data-ttu-id="d4332-2254">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d4332-2254">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-2255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2255">Az.Sql</span></span>
* <span data-ttu-id="d4332-2256">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="d4332-2256">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4332-2257">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-2257">Az.Storage</span></span>
* <span data-ttu-id="d4332-2258">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="d4332-2258">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d4332-2259">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4332-2259">New-AzStorageContext</span></span>
* <span data-ttu-id="d4332-2260">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d4332-2260">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d4332-2261">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d4332-2261">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-2262">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-2262">Az.Websites</span></span>
* <span data-ttu-id="d4332-2263">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="d4332-2263">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d4332-2264">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d4332-2264">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d4332-2265">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2265">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d4332-2266">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-2266">General</span></span>

- <span data-ttu-id="d4332-2267">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="d4332-2267">General Availability of Az Module</span></span>
- <span data-ttu-id="d4332-2268">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="d4332-2268">Online help for each module</span></span>
- <span data-ttu-id="d4332-2269">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="d4332-2269">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d4332-2270">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2270">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d4332-2271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4332-2271">Az.Accounts</span></span>
- <span data-ttu-id="d4332-2272">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="d4332-2272">Changed from Az.Profile</span></span>
- <span data-ttu-id="d4332-2273">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="d4332-2273">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d4332-2274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-2274">Az.ApiManagement</span></span>
- <span data-ttu-id="d4332-2275">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="d4332-2275">Fixes for #7002</span></span>
- <span data-ttu-id="d4332-2276">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d4332-2277">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4332-2277">Az.Batch</span></span>
- <span data-ttu-id="d4332-2278">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="d4332-2278">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d4332-2279">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="d4332-2279">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d4332-2280">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d4332-2281">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d4332-2281">Az.Billing</span></span>
- <span data-ttu-id="d4332-2282">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="d4332-2282">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d4332-2283">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2283">Az.CognitivServices</span></span>
- <span data-ttu-id="d4332-2284">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="d4332-2284">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d4332-2285">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d4332-2285">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d4332-2286">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4332-2286">Az.ContainerInstance</span></span>
- <span data-ttu-id="d4332-2287">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="d4332-2287">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d4332-2288">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d4332-2288">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d4332-2289">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2289">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d4332-2290">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-2290">Az.DataLakeStore</span></span>
- <span data-ttu-id="d4332-2291">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2291">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d4332-2292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4332-2292">Az.Monitor</span></span>
- <span data-ttu-id="d4332-2293">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2293">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d4332-2294">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4332-2294">Az.KeyVault</span></span>
- <span data-ttu-id="d4332-2295">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="d4332-2295">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d4332-2296">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4332-2296">Az.MachineLearning</span></span>
- <span data-ttu-id="d4332-2297">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d4332-2297">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d4332-2298">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d4332-2298">Az.Media</span></span>
- <span data-ttu-id="d4332-2299">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4332-2299">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d4332-2300">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2300">Az.Network</span></span>
<span data-ttu-id="d4332-2301">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="d4332-2301">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d4332-2302">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-2302">New cmdlets added:</span></span>
        - <span data-ttu-id="d4332-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4332-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4332-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4332-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4332-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4332-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4332-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4332-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4332-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4332-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4332-2308">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d4332-2308">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d4332-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d4332-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d4332-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4332-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d4332-2311">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4332-2311">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d4332-2312">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4332-2312">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d4332-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4332-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d4332-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4332-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d4332-2315">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-2315">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d4332-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d4332-2317">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d4332-2317">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d4332-2318">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d4332-2318">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d4332-2319">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4332-2319">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d4332-2320">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4332-2320">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d4332-2321">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4332-2321">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d4332-2322">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d4332-2322">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d4332-2323">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d4332-2324">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-2324">Az.OperationalInsights</span></span>
- <span data-ttu-id="d4332-2325">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d4332-2326">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4332-2326">Az.Profile</span></span>
- <span data-ttu-id="d4332-2327">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="d4332-2327">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-2328">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2328">Az.RecoveryServices</span></span>
- <span data-ttu-id="d4332-2329">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2329">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d4332-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2330">Az.Resources</span></span>
- <span data-ttu-id="d4332-2331">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2331">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d4332-2332">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-2332">Az.ServiceFabric</span></span>
- <span data-ttu-id="d4332-2333">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="d4332-2333">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d4332-2334">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2334">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d4332-2335">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d4332-2335">Az.SIgnalR</span></span>
- <span data-ttu-id="d4332-2336">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d4332-2336">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d4332-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2337">Az.Sql</span></span>
- <span data-ttu-id="d4332-2338">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="d4332-2338">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d4332-2339">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2339">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d4332-2340">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d4332-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-2341">Az.Storage</span></span>
- <span data-ttu-id="d4332-2342">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2342">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d4332-2343">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-2343">Az.Websites</span></span>
- <span data-ttu-id="d4332-2344">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="d4332-2344">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d4332-2345">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2345">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d4332-2346">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-2346">General</span></span>

* <span data-ttu-id="d4332-2347">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="d4332-2347">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d4332-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2348">Az.Compute</span></span>

* <span data-ttu-id="d4332-2349">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="d4332-2349">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d4332-2350">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-2350">Az.DataLakeStore</span></span>

* <span data-ttu-id="d4332-2351">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="d4332-2351">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d4332-2352">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4332-2352">Az.FrontDoor</span></span>

* <span data-ttu-id="d4332-2353">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="d4332-2353">Fixed some broken links</span></span>
    - <span data-ttu-id="d4332-2354">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-2354">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d4332-2355">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="d4332-2355">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d4332-2356">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2356">Az.RecoveryServices</span></span>

* <span data-ttu-id="d4332-2357">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2357">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d4332-2358">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="d4332-2358">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d4332-2359">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2359">Az.Resources</span></span>

* <span data-ttu-id="d4332-2360">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="d4332-2360">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d4332-2361">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2361">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d4332-2362">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2362">Az.Sql</span></span>

* <span data-ttu-id="d4332-2363">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="d4332-2363">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d4332-2364">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d4332-2364">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d4332-2365">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="d4332-2365">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d4332-2366">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4332-2366">Az.Storage</span></span>

* <span data-ttu-id="d4332-2367">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-2367">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d4332-2368">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="d4332-2368">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d4332-2369">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4332-2369">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d4332-2370">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="d4332-2370">Support Static Website configuration</span></span>
    - <span data-ttu-id="d4332-2371">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4332-2371">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d4332-2372">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4332-2372">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d4332-2373">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-2373">Az.Websites</span></span>

* <span data-ttu-id="d4332-2374">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4332-2374">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="d4332-2375">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="d4332-2375">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d4332-2376">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2376">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d4332-2377">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2377">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d4332-2378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4332-2378">Az.ApiManagement</span></span>
* <span data-ttu-id="d4332-2379">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2379">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d4332-2380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4332-2380">Az.Automation</span></span>
* <span data-ttu-id="d4332-2381">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="d4332-2381">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d4332-2382">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="d4332-2382">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d4332-2383">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="d4332-2383">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d4332-2384">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="d4332-2384">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d4332-2385">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="d4332-2385">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d4332-2386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2386">Az.Compute</span></span>
* <span data-ttu-id="d4332-2387">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="d4332-2387">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d4332-2388">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2388">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d4332-2389">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4332-2389">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4332-2390">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2390">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d4332-2391">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d4332-2391">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d4332-2392">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="d4332-2392">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d4332-2393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2393">Az.Network</span></span>
* <span data-ttu-id="d4332-2394">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="d4332-2394">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d4332-2395">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2395">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d4332-2396">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d4332-2396">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="d4332-2397">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4332-2397">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d4332-2398">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d4332-2398">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d4332-2399">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="d4332-2399">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d4332-2400">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="d4332-2400">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d4332-2401">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d4332-2401">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d4332-2402">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="d4332-2402">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d4332-2403">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2403">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d4332-2404">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d4332-2404">Az.Relay</span></span>
* <span data-ttu-id="d4332-2405">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="d4332-2405">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d4332-2406">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2406">Az.Resources</span></span>
* <span data-ttu-id="d4332-2407">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="d4332-2407">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d4332-2408">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="d4332-2408">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d4332-2409">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="d4332-2409">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d4332-2410">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-2410">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-2411">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="d4332-2411">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d4332-2412">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2412">Az.Sql</span></span>
* <span data-ttu-id="d4332-2413">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2413">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d4332-2414">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d4332-2414">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4332-2415">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d4332-2415">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4332-2416">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d4332-2416">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4332-2417">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="d4332-2417">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4332-2418">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d4332-2418">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4332-2419">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d4332-2419">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4332-2420">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d4332-2420">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4332-2421">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="d4332-2421">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d4332-2422">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="d4332-2422">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d4332-2423">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="d4332-2423">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d4332-2424">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2424">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d4332-2425">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4332-2425">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d4332-2426">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4332-2426">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d4332-2427">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4332-2427">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d4332-2428">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4332-2428">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d4332-2429">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="d4332-2429">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d4332-2430">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2430">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d4332-2431">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d4332-2431">General</span></span>
* <span data-ttu-id="d4332-2432">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="d4332-2432">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d4332-2433">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4332-2433">Az.Profile</span></span>
* <span data-ttu-id="d4332-2434">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="d4332-2434">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d4332-2435">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="d4332-2435">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d4332-2436">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d4332-2436">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d4332-2437">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="d4332-2437">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d4332-2438">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d4332-2438">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d4332-2439">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="d4332-2439">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d4332-2440">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="d4332-2440">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-2441">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2441">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-2442">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d4332-2442">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2443">Az.Compute</span></span>
* <span data-ttu-id="d4332-2444">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d4332-2444">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d4332-2445">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d4332-2445">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d4332-2446">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="d4332-2446">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-2447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-2447">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-2448">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="d4332-2448">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d4332-2449">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="d4332-2449">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d4332-2450">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d4332-2450">Az.Insights</span></span>
* <span data-ttu-id="d4332-2451">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="d4332-2451">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d4332-2452">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="d4332-2452">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d4332-2453">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="d4332-2453">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d4332-2454">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="d4332-2454">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-2455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2455">Az.Network</span></span>
* <span data-ttu-id="d4332-2456">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="d4332-2456">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d4332-2457">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4332-2457">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d4332-2458">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d4332-2458">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d4332-2459">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4332-2459">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d4332-2460">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d4332-2460">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d4332-2461">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4332-2461">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d4332-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4332-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4332-2463">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4332-2463">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4332-2464">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="d4332-2464">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2465">Az.Resources</span></span>
* <span data-ttu-id="d4332-2466">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="d4332-2466">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d4332-2467">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="d4332-2467">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4332-2468">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4332-2468">Az.ServiceBus</span></span>
* <span data-ttu-id="d4332-2469">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="d4332-2469">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4332-2470">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4332-2470">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4332-2471">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="d4332-2471">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d4332-2472">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d4332-2472">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d4332-2473">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d4332-2473">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d4332-2474">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d4332-2474">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d4332-2475">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d4332-2475">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d4332-2476">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2476">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d4332-2477">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4332-2477">Az.Profile</span></span>
* <span data-ttu-id="d4332-2478">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="d4332-2478">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d4332-2479">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="d4332-2479">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2480">Az.Compute</span></span>
* <span data-ttu-id="d4332-2481">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="d4332-2481">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d4332-2482">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="d4332-2482">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4332-2483">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4332-2483">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4332-2484">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="d4332-2484">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d4332-2485">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d4332-2485">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d4332-2486">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d4332-2486">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d4332-2487">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d4332-2487">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d4332-2488">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d4332-2488">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-2489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2489">Az.Network</span></span>
* <span data-ttu-id="d4332-2490">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="d4332-2490">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d4332-2491">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="d4332-2491">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2492">Az.Resources</span></span>
* <span data-ttu-id="d4332-2493">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="d4332-2493">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d4332-2494">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="d4332-2494">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d4332-2495">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2495">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d4332-2496">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="d4332-2496">Azure.Storage</span></span>
* <span data-ttu-id="d4332-2497">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="d4332-2497">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d4332-2498">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4332-2498">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d4332-2499">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4332-2499">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d4332-2500">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="d4332-2500">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d4332-2501">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d4332-2501">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4332-2502">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4332-2502">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4332-2503">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d4332-2503">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4332-2504">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4332-2504">Az.Compute</span></span>
* <span data-ttu-id="d4332-2505">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="d4332-2505">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d4332-2506">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4332-2506">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d4332-2507">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2507">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d4332-2508">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d4332-2508">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d4332-2509">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="d4332-2509">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4332-2510">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4332-2510">Az.Network</span></span>
* <span data-ttu-id="d4332-2511">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d4332-2511">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d4332-2512">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="d4332-2512">new cmdlets added</span></span>
    - <span data-ttu-id="d4332-2513">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4332-2513">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4332-2514">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4332-2514">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4332-2515">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4332-2515">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4332-2516">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4332-2516">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4332-2517">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-2517">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d4332-2518">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-2518">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d4332-2519">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="d4332-2519">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d4332-2520">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d4332-2520">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d4332-2521">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d4332-2521">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4332-2522">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4332-2522">Az.RedisCache</span></span>
* <span data-ttu-id="d4332-2523">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="d4332-2523">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d4332-2524">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="d4332-2524">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4332-2525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4332-2525">Az.Resources</span></span>
* <span data-ttu-id="d4332-2526">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4332-2526">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d4332-2527">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="d4332-2527">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4332-2528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4332-2528">Az.Sql</span></span>
* <span data-ttu-id="d4332-2529">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="d4332-2529">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4332-2530">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4332-2530">Az.Websites</span></span>
* <span data-ttu-id="d4332-2531">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="d4332-2531">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d4332-2532">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="d4332-2532">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d4332-2533">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="d4332-2533">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d4332-2534">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="d4332-2534">Initial Release</span></span>
